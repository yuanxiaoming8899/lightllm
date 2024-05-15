<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div align="center" dir="auto">
  <themed-picture data-catalyst-inline="true" data-catalyst=""><picture>
    <img alt="轻型法学硕士" src="/ModelTC/lightllm/raw/main/assets/lightllm.drawio.png" width="90%" style="visibility:visible;max-width:100%;">
  </picture></themed-picture>
</div>
<hr>
<div align="center" dir="auto">
<p dir="auto"><a href="https://github.com/ModelTC/lightllm/blob/main/docs/TokenAttention.md"><img src="https://camo.githubusercontent.com/d1465870dd0edfb9b32cd6ed333a1262a3c4c9af207be616580d4e8ca3cdc6ad/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f646f63732d6c61746573742d626c7565" alt="文档" data-canonical-src="https://img.shields.io/badge/docs-latest-blue" style="max-width: 100%;"></a>
<a href="https://github.com/ModelTC/lightllm/actions/workflows/docker-publish.yml"><img src="https://github.com/ModelTC/lightllm/actions/workflows/docker-publish.yml/badge.svg" alt="码头工人" style="max-width: 100%;"></a>
<a href="https://github.com/ModelTC/lightllm"><img src="https://camo.githubusercontent.com/249317bec98840a7d256b6390d4624b1a3a8c9e2257cfd0a8202654e64db245f/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f4d6f64656c54432f6c696768746c6c6d3f7374796c653d736f6369616c" alt="星星" data-canonical-src="https://img.shields.io/github/stars/ModelTC/lightllm?style=social" style="max-width: 100%;"></a>
<a href="https://discord.gg/WzzfwVSguU" rel="nofollow"><img src="https://camo.githubusercontent.com/7e1fb576aa7b5dce76076d4b3c979a379f8f138f448e00a19f75815a63c79f88/68747470733a2f2f696d672e736869656c64732e696f2f646973636f72642f313133393833353331323539323339323231343f6c6f676f3d646973636f7264266c6f676f436f6c6f723d7768697465" alt="不和谐横幅" data-canonical-src="https://img.shields.io/discord/1139835312592392214?logo=discord&amp;logoColor=white" style="max-width: 100%;"></a>
<a href="https://github.com/ModelTC/lightllm/blob/main/LICENSE"><img src="https://camo.githubusercontent.com/40142c253e709931aed7e885f3f85b8f52f52824a91778e2bfb6c221f7b6a2f3/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f6c6963656e73652f4d6f64656c54432f6c696768746c6c6d" alt="执照" data-canonical-src="https://img.shields.io/github/license/ModelTC/lightllm" style="max-width: 100%;"></a></p>
</div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LightLLM 是一个基于 Python 的 LLM（大型语言模型）推理和服务框架，以其轻量级设计、易于扩展和高速性能而著称。 LightLLM 利用了众多备受推崇的开源实现的优势，包括但不限于 FasterTransformer、TGI、vLLM 和 FlashAttention。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">特征</font></font></h2><a id="user-content-features" class="anchor" aria-label="永久链接：特点" href="#features"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">三进程异步协作：分词、模型推理、去分词异步进行，GPU利用率大幅提升。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Nopad（Unpad）：提供跨多个模型的nopad注意力操作支持，以有效处理长度差异较大的请求。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">动态批处理：启用请求的动态批处理调度</font></font></li>
<li><a href="https://github.com/Dao-AILab/flash-attention"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">FlashAttention</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：结合 FlashAttention 来提高推理过程中的速度并减少 GPU 内存占用。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">张量并行性：利用多个 GPU 上的张量并行性来实现更快的推理。</font></font></li>
<li><a href="/ModelTC/lightllm/blob/main/docs/TokenAttention.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Token Attention</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：实现了 token-wise 的 KV 缓存内存管理机制，实现推理过程中的零内存浪费。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">高性能Router：与Token Attention配合，精心管理每个Token的GPU内存，从而优化系统吞吐量。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Int8KV 缓存：此功能将令牌的容量增加到几乎两倍。只有骆驼支持。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持型号列表</font></font></h2><a id="user-content-supported-model-list" class="anchor" aria-label="永久链接：支持的型号列表" href="#supported-model-list"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><a href="https://huggingface.co/bigscience/bloom" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">盛开</font></font></a></li>
<li><a href="https://github.com/facebookresearch/llama"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">骆驼</font></font></a></li>
<li><a href="https://huggingface.co/meta-llama" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">骆驼V2</font></font></a></li>
<li><a href="https://github.com/bigcode-project/starcoder"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">星码器</font></font></a></li>
<li><a href="https://github.com/QwenLM/Qwen-7B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Qwen-7b</font></font></a></li>
<li><a href="https://github.com/THUDM/ChatGLM2-6B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">聊天GLM2-6b</font></font></a></li>
<li><a href="https://github.com/baichuan-inc/Baichuan-7B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百川7b</font></font></a></li>
<li><a href="https://github.com/baichuan-inc/Baichuan2"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百川2-7b</font></font></a></li>
<li><a href="https://github.com/baichuan-inc/Baichuan2"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百川2-13b</font></font></a></li>
<li><a href="https://github.com/baichuan-inc/Baichuan-13B"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">百川13b</font></font></a></li>
<li><a href="https://github.com/InternLM/InternLM"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">实习生LM-7b</font></font></a></li>
<li><a href="https://huggingface.co/01-ai/Yi-34B" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">伊34b</font></font></a></li>
<li><a href="https://huggingface.co/Qwen/Qwen-VL" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Qwen-VL</font></font></a></li>
<li><a href="https://huggingface.co/Qwen/Qwen-VL-Chat" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Qwen-VL-聊天</font></font></a></li>
<li><a href="https://huggingface.co/liuhaotian/llava-v1.5-7b" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">拉瓦-7b</font></font></a></li>
<li><a href="https://huggingface.co/liuhaotian/llava-v1.5-13b" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">拉瓦-13b</font></font></a></li>
<li><a href="/ModelTC/lightllm/blob/main"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">混合</font></font></a></li>
<li><a href="https://huggingface.co/stabilityai/stablelm-2-1_6b" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">稳定</font></font></a></li>
<li><a href="https://huggingface.co/openbmb/MiniCPM-2B-sft-bf16" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最小每千次展示费用</font></font></a></li>
</ul>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启动Qwen-7b时，需要设置参数“--eos_id 151643 --trust_remote_code”。</font></font></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ChatGLM2需要设置参数'--trust_remote_code'。</font></font></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Baichuan和Baichuan2需要设置参数'--trust_remote_code'。</font></font></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">InternLM需要设置参数'--trust_remote_code'。</font></font></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Stablelm 需要设置参数“--trust_remote_code”。</font></font></p>
</blockquote>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">开始使用</font></font></h2><a id="user-content-get-started" class="anchor" aria-label="永久链接：开始吧" href="#get-started"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要求</font></font></h3><a id="user-content-requirements" class="anchor" aria-label="永久链接：要求" href="#requirements"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该代码已使用 Pytorch&gt;=1.3、CUDA 11.8 和 Python 3.9 进行了测试。要安装必要的依赖项，请参阅提供的</font></font><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">requirements.txt</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并按照以下说明进行操作</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>pip install -r requirements.txt</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install -r requirements.txt" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">容器</font></font></h3><a id="user-content-container" class="anchor" aria-label="永久链接：容器" href="#container"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您可以使用官方的Docker容器更轻松地运行模型。为此，请按照下列步骤操作：</font></font></p>
<ul dir="auto">
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从 GitHub 容器注册表中拉取容器：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>docker pull ghcr.io/modeltc/lightllm:main</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="docker pull ghcr.io/modeltc/lightllm:main" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行具有 GPU 支持和端口映射的容器：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>docker run -it --gpus all -p 8080:8080                  \
        --shm-size 1g -v your_local_path:/data/         \
        ghcr.io/modeltc/lightllm:main /bin/bash</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="docker run -it --gpus all -p 8080:8080                  \
        --shm-size 1g -v your_local_path:/data/         \
        ghcr.io/modeltc/lightllm:main /bin/bash" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或者，您可以自己构建容器：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>docker build -t <span class="pl-k">&lt;</span>image_name<span class="pl-k">&gt;</span> <span class="pl-c1">.</span>
docker run -it --gpus all -p 8080:8080                  \
        --shm-size 1g -v your_local_path:/data/         \
        <span class="pl-k">&lt;</span>image_name<span class="pl-k">&gt;</span> /bin/bash</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="docker build -t <image_name> .
docker run -it --gpus all -p 8080:8080                  \
        --shm-size 1g -v your_local_path:/data/         \
        <image_name> /bin/bash" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">您还可以使用帮助程序脚本来启动容器和服务器：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python tools/quick_launch_docker.py --help</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python tools/quick_launch_docker.py --help" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
</li>
<li>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">注意：如果您使用多个 GPU，则可能需要通过添加命令来增加共享内存</font></font><code>--shm-size</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">大小</font></font><code>docker run</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装</font></font></h3><a id="user-content-installation" class="anchor" aria-label="永久链接：安装" href="#installation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从源代码安装</font></font></li>
</ul>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python setup.py install</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python setup.py install" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装 Triton 包</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该代码已在一系列 GPU 上进行了测试，包括 V100、A100、A800、4090 和 H800。如果您在 A100、A800 等上运行代码，我们建议使用 triton==2.1.0。</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>pip install triton==2.1.0 --no-deps</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install triton==2.1.0 --no-deps" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您在H800或V100上运行代码，我们建议使用triton-nightly，triton-nightly具有明显的CPU瓶颈，导致低并发级别下的高解码延迟。您可以观察</font></font><a href="https://github.com/openai/triton/issues/3619" data-hovercard-type="issue" data-hovercard-url="/triton-lang/triton/issues/3619/hovercard"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">这个问题</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">并</font></font><a href="https://github.com/openai/triton/pull/3638" data-hovercard-type="pull_request" data-hovercard-url="/triton-lang/triton/pull/3638/hovercard"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">修复PR</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。您可以尝试自己修改并编译源代码来解决这个问题。</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>pip install -U --index-url https://aiinfra.pkgs.visualstudio.com/PublicPackages/_packaging/Triton-Nightly/pypi/simple/ triton-nightly --no-deps</pre><div class="zeroclipboard-container">
    
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">奔跑的骆驼</font></font></h3><a id="user-content-run-llama" class="anchor" aria-label="永久链接：奔跑骆驼" href="#run-llama"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">借助高效的路由器和 TokenAttention，LightLLM 可以部署为服务并实现最先进的吞吐量性能。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启动服务器：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python -m lightllm.server.api_server --model_dir /path/llama-7B     \
                                     --host 0.0.0.0                 \
                                     --port 8080                    \
                                     --tp 1                         \
                                     --max_total_token_num 120000</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python -m lightllm.server.api_server --model_dir /path/llama-7B     \
                                     --host 0.0.0.0                 \
                                     --port 8080                    \
                                     --tp 1                         \
                                     --max_total_token_num 120000" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该参数</font></font><code>max_total_token_num</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">受部署环境的GPU显存影响。该参数值越大，可以处理更多的并发请求，从而提高系统的并发度。更多启动参数请参考</font></font><a href="/ModelTC/lightllm/blob/main/lightllm/server/api_server.py"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">api_server.py</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font><a href="/ModelTC/lightllm/blob/main/docs/ApiServerArgs.md"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">ApiServerArgs.md</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要在 shell 中发起查询：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>curl http://127.0.0.1:8080/generate     \
    -X POST                             \
    -d <span class="pl-s"><span class="pl-pds">'</span>{"inputs":"What is AI?","parameters":{"max_new_tokens":17, "frequency_penalty":1}}<span class="pl-pds">'</span></span> \
    -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="curl http://127.0.0.1:8080/generate     \
    -X POST                             \
    -d '{&quot;inputs&quot;:&quot;What is AI?&quot;,&quot;parameters&quot;:{&quot;max_new_tokens&quot;:17, &quot;frequency_penalty&quot;:1}}' \
    -H 'Content-Type: application/json'" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">从 Python 查询：</font></font></p>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">time</span>
<span class="pl-k">import</span> <span class="pl-s1">requests</span>
<span class="pl-k">import</span> <span class="pl-s1">json</span>

<span class="pl-s1">url</span> <span class="pl-c1">=</span> <span class="pl-s">'http://localhost:8080/generate'</span>
<span class="pl-s1">headers</span> <span class="pl-c1">=</span> {<span class="pl-s">'Content-Type'</span>: <span class="pl-s">'application/json'</span>}
<span class="pl-s1">data</span> <span class="pl-c1">=</span> {
    <span class="pl-s">'inputs'</span>: <span class="pl-s">'What is AI?'</span>,
    <span class="pl-s">"parameters"</span>: {
        <span class="pl-s">'do_sample'</span>: <span class="pl-c1">False</span>,
        <span class="pl-s">'ignore_eos'</span>: <span class="pl-c1">False</span>,
        <span class="pl-s">'max_new_tokens'</span>: <span class="pl-c1">1024</span>,
    }
}
<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">requests</span>.<span class="pl-en">post</span>(<span class="pl-s1">url</span>, <span class="pl-s1">headers</span><span class="pl-c1">=</span><span class="pl-s1">headers</span>, <span class="pl-s1">data</span><span class="pl-c1">=</span><span class="pl-s1">json</span>.<span class="pl-en">dumps</span>(<span class="pl-s1">data</span>))
<span class="pl-k">if</span> <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span> <span class="pl-c1">==</span> <span class="pl-c1">200</span>:
    <span class="pl-en">print</span>(<span class="pl-s1">response</span>.<span class="pl-en">json</span>())
<span class="pl-k">else</span>:
    <span class="pl-en">print</span>(<span class="pl-s">'Error:'</span>, <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span>, <span class="pl-s1">response</span>.<span class="pl-s1">text</span>)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import time
import requests
import json

url = 'http://localhost:8080/generate'
headers = {'Content-Type': 'application/json'}
data = {
    'inputs': 'What is AI?',
    &quot;parameters&quot;: {
        'do_sample': False,
        'ignore_eos': False,
        'max_new_tokens': 1024,
    }
}
response = requests.post(url, headers=headers, data=json.dumps(data))
if response.status_code == 200:
    print(response.json())
else:
    print('Error:', response.status_code, response.text)" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行多模式模型</font></font></h3><a id="user-content-run-multimodal-models" class="anchor" aria-label="永久链接：运行多模式模型" href="#run-multimodal-models"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h5 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">运行QWen-VL</font></font></h5><a id="user-content-run-qwen-vl" class="anchor" aria-label="永久链接：运行 QWen-VL" href="#run-qwen-vl"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python -m lightllm.server.api_server \
    --host 0.0.0.0                 \
    --port 8080                    \
    --tp 1                         \
    --max_total_token_num 12000    \
    --trust_remote_code            \
    --enable_multimodal            \
    --cache_capacity 1000          \
    --model_dir /path/of/Qwen-VL or /path/of/Qwen-VL-Chat</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python -m lightllm.server.api_server \
    --host 0.0.0.0                 \
    --port 8080                    \
    --tp 1                         \
    --max_total_token_num 12000    \
    --trust_remote_code            \
    --enable_multimodal            \
    --cache_capacity 1000          \
    --model_dir /path/of/Qwen-VL or /path/of/Qwen-VL-Chat" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h5 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">奔跑拉瓦</font></font></h5><a id="user-content-run-llava" class="anchor" aria-label="永久链接：奔跑拉瓦" href="#run-llava"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python -m lightllm.server.api_server \
    --host 0.0.0.0                 \
    --port 8080                    \
    --tp 1                         \
    --max_total_token_num 12000    \
    --trust_remote_code            \
    --enable_multimodal            \
    --cache_capacity 1000          \
    --model_dir /path/of/llava-v1.5-7b or /path/of/llava-v1.5-13b</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="python -m lightllm.server.api_server \
    --host 0.0.0.0                 \
    --port 8080                    \
    --tp 1                         \
    --max_total_token_num 12000    \
    --trust_remote_code            \
    --enable_multimodal            \
    --cache_capacity 1000          \
    --model_dir /path/of/llava-v1.5-7b or /path/of/llava-v1.5-13b" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h5 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来自 QWen-VL 的查询</font></font></h5><a id="user-content-query-from-qwen-vl" class="anchor" aria-label="永久链接：来自 QWen-VL 的查询" href="#query-from-qwen-vl"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">time</span>
<span class="pl-k">import</span> <span class="pl-s1">requests</span>
<span class="pl-k">import</span> <span class="pl-s1">json</span>
<span class="pl-k">import</span> <span class="pl-s1">base64</span>

<span class="pl-s1">url</span> <span class="pl-c1">=</span> <span class="pl-s">'http://localhost:8080/generate'</span>
<span class="pl-s1">headers</span> <span class="pl-c1">=</span> {<span class="pl-s">'Content-Type'</span>: <span class="pl-s">'application/json'</span>}

<span class="pl-s1">uri</span> <span class="pl-c1">=</span> <span class="pl-s">"/local/path/of/image"</span> <span class="pl-c"># or "/http/path/of/image"</span>
<span class="pl-k">if</span> <span class="pl-s1">uri</span>.<span class="pl-en">startswith</span>(<span class="pl-s">"http"</span>):
    <span class="pl-s1">images</span> <span class="pl-c1">=</span> [{<span class="pl-s">"type"</span>: <span class="pl-s">"url"</span>, <span class="pl-s">"data"</span>: <span class="pl-s1">uri</span>}]
<span class="pl-k">else</span>:
    <span class="pl-k">with</span> <span class="pl-en">open</span>(<span class="pl-s1">uri</span>, <span class="pl-s">'rb'</span>) <span class="pl-k">as</span> <span class="pl-s1">fin</span>:
        <span class="pl-s1">b64</span> <span class="pl-c1">=</span> <span class="pl-s1">base64</span>.<span class="pl-en">b64encode</span>(<span class="pl-s1">fin</span>.<span class="pl-en">read</span>()).<span class="pl-en">decode</span>(<span class="pl-s">"utf-8"</span>)
    <span class="pl-s1">images</span><span class="pl-c1">=</span>[{<span class="pl-s">'type'</span>: <span class="pl-s">"base64"</span>, <span class="pl-s">"data"</span>: <span class="pl-s1">b64</span>}]

<span class="pl-s1">data</span> <span class="pl-c1">=</span> {
    <span class="pl-s">"inputs"</span>: <span class="pl-s">"&lt;img&gt;&lt;/img&gt;Generate the caption in English with grounding:"</span>,
    <span class="pl-s">"parameters"</span>: {
        <span class="pl-s">"max_new_tokens"</span>: <span class="pl-c1">200</span>,
        <span class="pl-c"># The space before &lt;|endoftext|&gt; is important, the server will remove the first bos_token_id, but QWen tokenizer does not has bos_token_id</span>
        <span class="pl-s">"stop_sequences"</span>: [<span class="pl-s">" &lt;|endoftext|&gt;"</span>],
    },
    <span class="pl-s">"multimodal_params"</span>: {
        <span class="pl-s">"images"</span>: <span class="pl-s1">images</span>,
    }
}

<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">requests</span>.<span class="pl-en">post</span>(<span class="pl-s1">url</span>, <span class="pl-s1">headers</span><span class="pl-c1">=</span><span class="pl-s1">headers</span>, <span class="pl-s1">data</span><span class="pl-c1">=</span><span class="pl-s1">json</span>.<span class="pl-en">dumps</span>(<span class="pl-s1">data</span>))
<span class="pl-k">if</span> <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span> <span class="pl-c1">==</span> <span class="pl-c1">200</span>:
    <span class="pl-en">print</span>(<span class="pl-s1">response</span>.<span class="pl-en">json</span>())
<span class="pl-k">else</span>:
    <span class="pl-en">print</span>(<span class="pl-s">'Error:'</span>, <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span>, <span class="pl-s1">response</span>.<span class="pl-s1">text</span>)</pre><div class="zeroclipboard-container">
  
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h5 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来自 QWen-VL-Chat 的查询</font></font></h5><a id="user-content-query-from-qwen-vl-chat" class="anchor" aria-label="永久链接：来自 QWen-VL-Chat 的查询" href="#query-from-qwen-vl-chat"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">json</span>
<span class="pl-k">import</span> <span class="pl-s1">requests</span>
<span class="pl-k">import</span> <span class="pl-s1">base64</span>

<span class="pl-k">def</span> <span class="pl-en">run_once</span>(<span class="pl-s1">query</span>, <span class="pl-s1">uris</span>):
    <span class="pl-s1">images</span> <span class="pl-c1">=</span> []
    <span class="pl-k">for</span> <span class="pl-s1">uri</span> <span class="pl-c1">in</span> <span class="pl-s1">uris</span>:
        <span class="pl-k">if</span> <span class="pl-s1">uri</span>.<span class="pl-en">startswith</span>(<span class="pl-s">"http"</span>):
            <span class="pl-s1">images</span>.<span class="pl-en">append</span>({<span class="pl-s">"type"</span>: <span class="pl-s">"url"</span>, <span class="pl-s">"data"</span>: <span class="pl-s1">uri</span>})
        <span class="pl-k">else</span>:
            <span class="pl-k">with</span> <span class="pl-en">open</span>(<span class="pl-s1">uri</span>, <span class="pl-s">'rb'</span>) <span class="pl-k">as</span> <span class="pl-s1">fin</span>:
                <span class="pl-s1">b64</span> <span class="pl-c1">=</span> <span class="pl-s1">base64</span>.<span class="pl-en">b64encode</span>(<span class="pl-s1">fin</span>.<span class="pl-en">read</span>()).<span class="pl-en">decode</span>(<span class="pl-s">"utf-8"</span>)
            <span class="pl-s1">images</span>.<span class="pl-en">append</span>({<span class="pl-s">'type'</span>: <span class="pl-s">"base64"</span>, <span class="pl-s">"data"</span>: <span class="pl-s1">b64</span>})

    <span class="pl-s1">data</span> <span class="pl-c1">=</span> {
        <span class="pl-s">"inputs"</span>: <span class="pl-s1">query</span>,
        <span class="pl-s">"parameters"</span>: {
            <span class="pl-s">"max_new_tokens"</span>: <span class="pl-c1">200</span>,
            <span class="pl-c"># The space before &lt;|endoftext|&gt; is important, the server will remove the first bos_token_id, but QWen tokenizer does not has bos_token_id</span>
            <span class="pl-s">"stop_sequences"</span>: [<span class="pl-s">" &lt;|endoftext|&gt;"</span>, <span class="pl-s">" &lt;|im_start|&gt;"</span>, <span class="pl-s">" &lt;|im_end|&gt;"</span>],
        },
        <span class="pl-s">"multimodal_params"</span>: {
            <span class="pl-s">"images"</span>: <span class="pl-s1">images</span>,
        }
    }

    <span class="pl-c"># url = "http://127.0.0.1:8080/generate_stream"</span>
    <span class="pl-s1">url</span> <span class="pl-c1">=</span> <span class="pl-s">"http://127.0.0.1:8080/generate"</span>
    <span class="pl-s1">headers</span> <span class="pl-c1">=</span> {<span class="pl-s">'Content-Type'</span>: <span class="pl-s">'application/json'</span>}
    <span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">requests</span>.<span class="pl-en">post</span>(<span class="pl-s1">url</span>, <span class="pl-s1">headers</span><span class="pl-c1">=</span><span class="pl-s1">headers</span>, <span class="pl-s1">data</span><span class="pl-c1">=</span><span class="pl-s1">json</span>.<span class="pl-en">dumps</span>(<span class="pl-s1">data</span>))
    <span class="pl-k">if</span> <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span> <span class="pl-c1">==</span> <span class="pl-c1">200</span>:
        <span class="pl-en">print</span>(<span class="pl-s">" + result: ({})"</span>.<span class="pl-en">format</span>(<span class="pl-s1">response</span>.<span class="pl-en">json</span>()))
    <span class="pl-k">else</span>:
        <span class="pl-en">print</span>(<span class="pl-s">' + error: {}, {}'</span>.<span class="pl-en">format</span>(<span class="pl-s1">response</span>.<span class="pl-s1">status_code</span>, <span class="pl-s1">response</span>.<span class="pl-s1">text</span>))

<span class="pl-s">"""</span>
<span class="pl-s">multi-img, multi-round:</span>
<span class="pl-s"></span>
<span class="pl-s">&lt;|im_start|&gt;system</span>
<span class="pl-s">You are a helpful assistant.&lt;|im_end|&gt;</span>
<span class="pl-s">&lt;|im_start|&gt;user</span>
<span class="pl-s">&lt;img&gt;&lt;/img&gt;</span>
<span class="pl-s">&lt;img&gt;&lt;/img&gt;</span>
<span class="pl-s">上面两张图片分别是哪两个城市？请对它们进行对比。&lt;|im_end|&gt;</span>
<span class="pl-s">&lt;|im_start|&gt;assistant</span>
<span class="pl-s">根据提供的信息，两张图片分别是重庆和北京。&lt;|im_end|&gt;</span>
<span class="pl-s">&lt;|im_start|&gt;user</span>
<span class="pl-s">这两座城市分别在什么地方？&lt;|im_end|&gt;</span>
<span class="pl-s">&lt;|im_start|&gt;assistant</span>
<span class="pl-s">"""</span>
<span class="pl-en">run_once</span>(
    <span class="pl-s1">uris</span> <span class="pl-c1">=</span> [
        <span class="pl-s">"assets/mm_tutorial/Chongqing.jpeg"</span>,
        <span class="pl-s">"assets/mm_tutorial/Beijing.jpeg"</span>,
    ],
    <span class="pl-s1">query</span> <span class="pl-c1">=</span> <span class="pl-s">"&lt;|im_start|&gt;system<span class="pl-cce">\n</span>You are a helpful assistant.&lt;|im_end|&gt;<span class="pl-cce">\n</span>&lt;|im_start|&gt;user<span class="pl-cce">\n</span>&lt;img&gt;&lt;/img&gt;<span class="pl-cce">\n</span>&lt;img&gt;&lt;/img&gt;<span class="pl-cce">\n</span>上面两张图片分别是哪两个城市？请对它们进行对比。&lt;|im_end|&gt;<span class="pl-cce">\n</span>&lt;|im_start|&gt;assistant<span class="pl-cce">\n</span>根据提供的信息，两张图片分别是重庆和北京。&lt;|im_end|&gt;<span class="pl-cce">\n</span>&lt;|im_start|&gt;user<span class="pl-cce">\n</span>这两座城市分别在什么地方？&lt;|im_end|&gt;<span class="pl-cce">\n</span>&lt;|im_start|&gt;assistant<span class="pl-cce">\n</span>"</span>
)</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="import json
import requests
import base64

def run_once(query, uris):
    images = []
    for uri in uris:
        if uri.startswith(&quot;http&quot;):
            images.append({&quot;type&quot;: &quot;url&quot;, &quot;data&quot;: uri})
        else:
            with open(uri, 'rb') as fin:
                b64 = base64.b64encode(fin.read()).decode(&quot;utf-8&quot;)
            images.append({'type': &quot;base64&quot;, &quot;data&quot;: b64})

    data = {
        &quot;inputs&quot;: query,
        &quot;parameters&quot;: {
            &quot;max_new_tokens&quot;: 200,
            # The space before <|endoftext|> is important, the server will remove the first bos_token_id, but QWen tokenizer does not has bos_token_id
            &quot;stop_sequences&quot;: [&quot; <|endoftext|>&quot;, &quot; <|im_start|>&quot;, &quot; <|im_end|>&quot;],
        },
        &quot;multimodal_params&quot;: {
            &quot;images&quot;: images,
        }
    }

    # url = &quot;http://127.0.0.1:8080/generate_stream&quot;
    url = &quot;http://127.0.0.1:8080/generate&quot;
    headers = {'Content-Type': 'application/json'}
    response = requests.post(url, headers=headers, data=json.dumps(data))
    if response.status_code == 200:
        print(&quot; + result: ({})&quot;.format(response.json()))
    else:
        print(' + error: {}, {}'.format(response.status_code, response.text))

      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h5 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">来自 Llava 的查询</font></font></h5><a id="user-content-query-from-llava" class="anchor" aria-label="永久链接：来自 Llava 的查询" href="#query-from-llava"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="highlight highlight-source-python notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-k">import</span> <span class="pl-s1">time</span>
<span class="pl-k">import</span> <span class="pl-s1">requests</span>
<span class="pl-k">import</span> <span class="pl-s1">json</span>
<span class="pl-k">import</span> <span class="pl-s1">base64</span>

<span class="pl-s1">url</span> <span class="pl-c1">=</span> <span class="pl-s">'http://localhost:8080/generate'</span>
<span class="pl-s1">headers</span> <span class="pl-c1">=</span> {<span class="pl-s">'Content-Type'</span>: <span class="pl-s">'application/json'</span>}

<span class="pl-s1">uri</span> <span class="pl-c1">=</span> <span class="pl-s">"/local/path/of/image"</span> <span class="pl-c"># or "/http/path/of/image"</span>
<span class="pl-k">if</span> <span class="pl-s1">uri</span>.<span class="pl-en">startswith</span>(<span class="pl-s">"http"</span>):
    <span class="pl-s1">images</span> <span class="pl-c1">=</span> [{<span class="pl-s">"type"</span>: <span class="pl-s">"url"</span>, <span class="pl-s">"data"</span>: <span class="pl-s1">uri</span>}]
<span class="pl-k">else</span>:
    <span class="pl-k">with</span> <span class="pl-en">open</span>(<span class="pl-s1">uri</span>, <span class="pl-s">'rb'</span>) <span class="pl-k">as</span> <span class="pl-s1">fin</span>:
        <span class="pl-s1">b64</span> <span class="pl-c1">=</span> <span class="pl-s1">base64</span>.<span class="pl-en">b64encode</span>(<span class="pl-s1">fin</span>.<span class="pl-en">read</span>()).<span class="pl-en">decode</span>(<span class="pl-s">"utf-8"</span>)
    <span class="pl-s1">images</span><span class="pl-c1">=</span>[{<span class="pl-s">'type'</span>: <span class="pl-s">"base64"</span>, <span class="pl-s">"data"</span>: <span class="pl-s1">b64</span>}]

<span class="pl-s1">data</span> <span class="pl-c1">=</span> {
    <span class="pl-s">"inputs"</span>: <span class="pl-s">"A chat between a curious human and an artificial intelligence assistant. The assistant gives helpful, detailed, and polite answers to the human's questions. USER: &lt;image&gt;<span class="pl-cce">\n</span>Please explain the picture. ASSISTANT:"</span>,
    <span class="pl-s">"parameters"</span>: {
        <span class="pl-s">"max_new_tokens"</span>: <span class="pl-c1">200</span>,
    },
    <span class="pl-s">"multimodal_params"</span>: {
        <span class="pl-s">"images"</span>: <span class="pl-s1">images</span>,
    }
}

<span class="pl-s1">response</span> <span class="pl-c1">=</span> <span class="pl-s1">requests</span>.<span class="pl-en">post</span>(<span class="pl-s1">url</span>, <span class="pl-s1">headers</span><span class="pl-c1">=</span><span class="pl-s1">headers</span>, <span class="pl-s1">data</span><span class="pl-c1">=</span><span class="pl-s1">json</span>.<span class="pl-en">dumps</span>(<span class="pl-s1">data</span>))
<span class="pl-k">if</span> <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span> <span class="pl-c1">==</span> <span class="pl-c1">200</span>:
    <span class="pl-en">print</span>(<span class="pl-s1">response</span>.<span class="pl-en">json</span>())
<span class="pl-k">else</span>:
    <span class="pl-en">print</span>(<span class="pl-s">'Error:'</span>, <span class="pl-s1">response</span>.<span class="pl-s1">status_code</span>, <span class="pl-s1">response</span>.<span class="pl-s1">text</span>)</pre><div class="zeroclipboard-container">
    

data = {
    &quot;inputs&quot;: &quot;A chat between a curious human and an artificial intelligence assistant. The assistant gives helpful, detailed, and polite answers to the human's questions. USER: <image>\nPlease explain the picture. ASSISTANT:&quot;,
    &quot;parameters&quot;: {
        &quot;max_new_tokens&quot;: 200,
    },
    &quot;multimodal_params&quot;: {
        &quot;images&quot;: images,
    }
}

response = requests.post(url, headers=headers, data=json.dumps(data))
if response.status_code == 200:
    print(response.json())
else:
    print('Error:', response.status_code, response.text)" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">附加启动参数：</font></font><code>--enable_multimodal</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">, </font></font><code>--cache_capacity</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">, 越大则</font></font><code>--cache_capacity</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">需要越大</font></font><code>shm-size</code></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持</font><font style="vertical-align: inherit;">视觉模型在gpu 0上运行</font></font><code>--tp &gt; 1</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">时</font></font><code>tp &gt; 1</code><font style="vertical-align: inherit;"></font></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Qwen-VL 的特殊图像标签是</font></font><code>&lt;img&gt;&lt;/img&gt;</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">（</font></font><code>&lt;image&gt;</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">对于 Llava）， 的长度</font></font><code>data["multimodal_params"]["images"]</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">应与标签的数量相同，数量可以是 0, 1, 2, ...</font></font></p>
</blockquote>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">输入图像格式：类似字典的列表</font></font><code>{'type': 'url'/'base64', 'data': xxx}</code></p>
</blockquote>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">表现</font></font></h2><a id="user-content-performance" class="anchor" aria-label="永久链接：性能" href="#performance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">服务表现</font></font></h3><a id="user-content-service-performance" class="anchor" aria-label="永久链接：服务绩效" href="#service-performance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们使用具有 80G GPU 内存的 A800 在 LLaMA-7B 上比较了 LightLLM 和 vLLM==0.1.2 的服务性能。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">首先，准备数据如下：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>wget https://huggingface.co/datasets/anon8231489123/ShareGPT_Vicuna_unfiltered/resolve/main/ShareGPT_V3_unfiltered_cleaned_split.json</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="wget https://huggingface.co/datasets/anon8231489123/ShareGPT_Vicuna_unfiltered/resolve/main/ShareGPT_V3_unfiltered_cleaned_split.json" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启动服务：</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre>python -m lightllm.server.api_server --model_dir /path/llama-7b --tp 1 --max_total_token_num 121060 --tokenizer_mode auto</pre><div class="zeroclipboard-container">
   
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">性能对比结果如下：</font></font></p>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">法学硕士</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">轻型法学硕士</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">总时间：361.79 秒</font></font><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">吞吐量：5.53 个请求/秒</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">总时间：188.85 秒</font></font><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">吞吐量：10.59 个请求/秒</font></font></td>
</tr>
</tbody>
</table>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">静态推理性能</font></font></h3><a id="user-content-static-inference-performance" class="anchor" aria-label="永久链接：静态推理性能" href="#static-inference-performance"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为了调试，我们为各种模型提供静态性能测试脚本。例如，您可以通过以下方式评估 LLaMA 模型的推理性能</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c1">cd</span> test/model
python test_llama.py</pre><div class="zeroclipboard-container">
 
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">常问问题</font></font></h3><a id="user-content-faq" class="anchor" aria-label="永久链接：常见问题解答" href="#faq"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LLaMA 标记生成器无法加载。
</font></font><ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">考虑通过运行命令来解决此问题</font></font><code>pip install protobuf==3.20.0</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
</ul>
</li>
<li><code>error   : PTX .version 7.4 does not support .target sm_89</code>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">启动与</font></font><code>bash tools/resolve_ptx_version python -m lightllm.server.api_server ... </code></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">社区</font></font></h2><a id="user-content-community" class="anchor" aria-label="永久链接：社区" href="#community"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如需更多信息和讨论，</font></font><a href="https://discord.gg/WzzfwVSguU" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请加入我们的不和谐服务器</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执照</font></font></h2><a id="user-content-license" class="anchor" aria-label="永久链接：许可证" href="#license"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">该存储库是在</font></font><a href="/ModelTC/lightllm/blob/main/LICENSE"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Apache-2.0</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">许可证下发布的。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">致谢</font></font></h2><a id="user-content-acknowledgement" class="anchor" aria-label="永久链接：致谢" href="#acknowledgement"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在开发 LightLLM 时，我们从以下项目中学到了很多东西。</font></font></p>
<ul dir="auto">
<li><a href="https://github.com/NVIDIA/FasterTransformer"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">更快的变压器</font></font></a></li>
<li><a href="https://github.com/huggingface/text-generation-inference"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文本生成推理</font></font></a></li>
<li><a href="https://github.com/vllm-project/vllm"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">法学硕士</font></font></a></li>
<li><a href="https://github.com/Dao-AILab/flash-attention"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">闪光注意1&amp;2</font></font></a></li>
<li><a href="https://github.com/openai/triton"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">OpenAI Triton</font></font></a></li>
</ul>
</article></div>
