---
theme: default
layout: cover
colorSchema: light
background: /library.jpg
title: AI Masterclass 2025
info: |
  AI Masterclass 
  2025
drawings:
  enabled: false
transition: slide-up
mdc: true
hideInToc: true
---

# AI Masterclass 2025
May 12-16, Trinity College Dublin

<!-- 
- Thank you for coming!
- Super excited to be here in Dublin!
- Thank you Red Hat and IMB for organizing this event
- Thank you Michael Johnston and Dominik Dalhem
 -->
---
layout: statement
title: Welcome!
hideInToc: true
---

# Welcome!

<!-- 
- Thank you for coming!
- Super excited to be here in Dublin!
- Thank you Red Hat and IMB for organizing this event
- Thank you Michael Johnston and Dominik Dalhem
 -->

---
title: This is me
hideInToc: true
---

# This is me
Diego Maniloff
<div class="flex justify-center mb-8">
  <img src="/images/die_serious.jpeg" class="w-48" />
</div>

<div class="text-4xl text-center font-mono">
dmanilof@redhat.com
</div>

<div class="absolute bottom-10 left-0 right-0">
  <div class="flex justify-center items-center gap-8">
    <img src="/images/unata.png" class="h-10 object-contain" />
    <img src="/images/instacart.svg" class="h-6 object-contain" />
    <img src="/images/nextdoor.png" class="h-8 object-contain" />
    <img src="/images/huggingface.png" class="h-12 object-contain" />
    <img src="/images/redhat.svg" class="h-7 object-contain" />
  </div>
</div>

<!-- 
- I've been a machine learning engineer for a while
- Born and raised in Argentina, been living in Toronto for over 10 years
- Was part of a small startup in Toronto
- Now at Red Hat Trustworthy AI team
-->

---
title: Not a typo
hideInToc: true
---

# Not a typo
Diego Maniloff

<div class="flex justify-center mb-8">
  <img src="/images/die_silly.jpg" class="w-48" />
</div>

<div class="flex justify-center mb-8">
<div class="text-4xl font-mono">
dmanilof@redhat.com
</div>
</div>

<div class="absolute bottom-10 left-0 right-0">
  <div class="flex justify-center items-center gap-8">
    <img src="/images/unata.png" class="h-10 object-contain" />
    <img src="/images/instacart.svg" class="h-6 object-contain" />
    <img src="/images/nextdoor.png" class="h-8 object-contain" />
    <img src="/images/huggingface.png" class="h-12 object-contain" />
    <img src="/images/redhat.svg" class="h-7 object-contain" />
  </div>
</div>

---
title: Masterclass Outline
hideInToc: true
---
# Masterclass Outline
From scratch to an advanced RAG agent with guardrails

````md magic-move {lines: true}
```python {*|4|*}
# Unit 1
agent = Agent(
    llama_stack_client,
    model="my-model",
    instructions="You are a helpful assistant that can use tools to answer questions.",
    tools=["basic-rag-tool"],
)
```

```python {*|6|*}
# Unit 2
agent = Agent(
    llama_stack_client,
    model="my-model",
    instructions="You are a helpful assistant that can use tools to answer questions.",
    tools=["basic-rag-tool", "advanced-rag-tool"],
)
```

```python {*|7-8|*}
# Unit 3
agent = Agent(
    llama_stack_client,
    model="my-model",
    instructions="You are a helpful assistant that can use tools to answer questions.",
    tools=["basic-rag-tool", "advanced-rag-tool"],
    input_shields=["guardrails::my-filter"],
    output_shields=["guardrails::my-filter"],
)
```
````
<!-- 

[click] start with a simple model and run inference, some basic tools like rag
[click]
[click]
[click] then add advanced rag tools
[click]
[click]
[click] then add safety guardrails and eval

 -->

---
title: Unit 1
layout: section
hideInToc: true
---

# Unit 1 <br> Introduction to Llama Stack

---
title: Unit 1 Goals
hideInToc: true
---

# Unit 1 Goals
- Understand the core concepts of Llama Stack
- Get our development environment working
- Prepare for Units 2 and 3
- Start your Masterclass Project

---
title: Intros
layout: section
hideInToc: true
---
# 👋🏼 Intros
<!--  
- intro yourself & talk about your research & potential project
-->

---
layout: two-cols
hideInToc: true
title: What we're doing today
---
# What we're doing today

<Transform :scale="0.90">

<Toc minDepth="1" maxDepth="1" />
</Transform>

::right::

### Format
1. 📽️📽️📽️, then 🎹 
2. 📽️📽️, then 🎹 🎹
3. 📽️, then 🎹 🎹 🎹

<!--
- we'll take rounds of slides and exercises
- the idea is to learn by doing
-->

---
title: Don't worry!
hideInToc: true
---

# Don't worry, we'll take breaks!
- 8:30 - 9am: Breakfast
- 10am: Morning coffee break
- 12-1pm: Lunch
- 2:30pm: Afternoon coffee break



---
title: Why Llama Stack?
layout: fact
---

What is Llama Stack and why is it a good idea?


---
title: AI System Design, I'm good thanks
layout: image-right
image: /images/drake-no.jpg
backgroundSize: 60%
hideInToc: true
---

# AI System Design
<br>
<br>

<v-clicks>

*I just need model inference, `curl https://api.openai.com/v1/chat/completions` and I'm done*
</v-clicks>

<!-- 
- Can't resist a Drake meme
- Ok so let's say you're tasked with building an AI system
- You might be tempted to think that you just need a model
 -->
---
title: AI System Design, Oh wait!
hideInToc: true
---

# AI System Design

<v-clicks>

- ~~I just need model inference, `curl https://api.openai.com/v1/chat/completions` and I'm done~~
- That's not very useful. Let's connect the model to our data. **We need retrieval.**
- Hmm, but exactly how useful is this? **We need evaluation and metrics.**
- But wait! Will it leak private information? **We need safety guardrails and content filtering.**
- ...
- **We need agents**
- **We need tool calling**
- **We need monitoring**
- ...
- How do we deploy this whole thing?
</v-clicks>

<!--
- but you will quickly realize that you need more
- much more
-->

---
title: Why Llama Stack?
layout: fact
hideInToc: true
---

What is Llama Stack and why is it a good idea?
<v-switch>
<template #1> 
  
# Opinionated Organization 

</template>
<template #2> 
  
# Helpful Organization 

</template>
<template #3> 

# Organization 

</template>
</v-switch>

<!-- 
- let's go back to our original question
- we just saw there's a lot of stuff going on
- so, we need a way to get all that stuff organized
[click]
- llama stack provides an opinionated approach to that organization
- you can have multiple components, integrate with different vendors, and support production deployments.
[click]
- now, notice that when i say opinionated, i mean it in a positive way. it's helpful because there's so much going on.
[click]
- and so in the spirit of starting with the "why", this is one of the main messages of my talk, and one of the reasons why LS is getting attention from the community and the industry.
- "LLama Stack provides a way to organize our AI Systems"
 -->

---
title: I need this
layout: image-right
image: /images/drake-yes.jpg
backgroundSize: 60%
hideInToc: true
---

# Organization

What's there to organize?
- Inference
- Retrieval
- Evaluation
- Safety
- Agents
- Tool calling
- Monitoring
- Deployment
- ... and more!


---
layout: section
title: 🎹 Dev Environment
hideInToc: true
---
# 🎹 Dev Environment

<!-- 
# First slide with 🎹 emoji
- Explain what will happen in these sections
- You will show commands, leave up on the screen, go around the room
- Then, regroup to show
 -->
---
title: Environment Setup
---
# Environment Setup
Setting up the local development environment

Run the ollama server
```bash
ollama pull llama3.2:3b-instruct-fp16
ollama serve
```

Clone the masterclass repo
```bash
git clone https://github.com/trustyai-explainability/ai-masterclass-2025.git
cd ai-masterclass-2025
```

Build and run the stack
```bash
uv run --with "llama-stack" llama stack build --config=distributions/masterclass-minimal/build.yaml
```
```bash
source masterclass_minimal/bin/activate
llama stack run distributions/masterclass-minimal/run.yaml
```

<div class="absolute left-30px bottom-30px text-sm">
<div class="flex gap-4">
  <a href="https://ollama.com/" target="_blank">
    <img src="https://ollama.com/public/ollama.png" class="h-8 object-contain" />
  </a>

  <a href="https://docs.astral.sh/uv/" target="_blank">
    <img src="https://docs.astral.sh/uv/assets/logo-letter.svg" class="h-8 object-contain" />
  </a>
  <a href="https://github.com/trustyai-explainability/ai-masterclass-2025" target="_blank" class="h-10 object-contain">
    <carbon:logo-github />
  </a>

</div>
</div>

<!-- 

- Show the repo (click octocat logo)
- Show commands
- Make sure ollama is running
- Go around the room to make sure everyone is good
- Leave this slide up until everyone is done

[PAUSE]
 -->

---
title: What happened?
hideInToc: true
---

# Environment Setup
What happened?

<div class="grid grid-cols-[70%_30%] gap-4">
  <div>

```bash
$ tree distributions
distributions
├── masterclass-agents
│   ├── build.yaml
│   └── run.yaml
└── masterclass-minimal
    ├── build.yaml
    └── run.yaml
```
  </div>
  <div>
    Distribution config files (from our repo)
  </div>
</div>

<div class="grid grid-cols-[70%_30%] gap-4">
  <div>

```bash
$ ls -l masterclass_minimal
total 16
-rw-r--r--   1 diego  staff    43B May  9 09:27 CACHEDIR.TAG
drwxr-xr-x  39 diego  staff   1.2K May  9 09:27 bin
drwxr-xr-x   3 diego  staff    96B May  9 09:27 lib
-rw-r--r--   1 diego  staff   176B May  9 09:27 pyvenv.cfg
```
  </div>
  <div>
    Pyton virtual environment (generated by the build command)
  </div>
</div>


<div class="grid grid-cols-[70%_30%] gap-4">
  <div>

```bash
$ tree ~/.llama/distributions/masterclass_minimal
/Users/diego/.llama/distributions/masterclass_minimal
├── kvstore.db
├── masterclass_minimal-build.yaml
├── masterclass_minimal-run.yaml
└── trace_store.db
```
  </div>
  <div>
    Distribution directory (generated by the build command)
  </div>
</div>

---
layout: section
title: Our Own (tiny) Stack
hideInToc: true
---
# Our Own (tiny) Stack


---
title: Our Own (tiny) Stack
layout: two-cols
layoutClass: gap-3
---

# Our Own Stack
🙌🏼 We just ran our first stack!

```bash
cat distributions/masterclass-minimal/run.yaml
```

::right::

<Transform :scale="0.95">

<!-- <<< ../distributions/masterclass-minimal/run.yaml yaml  -->
```yaml
version: "2"
image_name: masterclass_minimal
apis:
  - inference
  - telemetry
providers:
  inference:
    - provider_id: ollama
      provider_type: remote::ollama
      config:
        url: ${env.OLLAMA_URL:http://localhost:11434}
  telemetry:
    - provider_id: meta-reference
      provider_type: inline::meta-reference
      config:
        service_name: ${env.OTEL_SERVICE_NAME:}
      sinks: ${env.TELEMETRY_SINKS:console,sqlite}
      sqlite_db_path: ${env.SQLITE_STORE_DIR:~/.llama/distributions/masterclass_minimal}/trace_store.db
models:
  - metadata: {}
    model_id: meta-llama/Llama-3.2-3B-Instruct
    provider_id: ollama
    model_type: llm
    provider_model_id: llama3.2:3b-instruct-fp16 # from ollama list
server:
  host: localhost
  port: 8321
```
</Transform>

---
layout: section
title: Core Concepts
---
# Core Concepts

---
title: Core Concepts (api, provider, resource, distribution)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---
# Core Concepts
- Api
- Provider
- Resource
- Distributions

<v-click>

> An API is a collection of endpoints.
</v-click> 

<v-click>

> Providers implement APIs ...
</v-click>

<v-click>

> ... and provide resources.
</v-click>

<v-click>

> A distribution is a collection of specific providers (+ config).
</v-click>

<div class="absolute left-30px bottom-30px text-sm">
  <a href="https://llama-stack.readthedocs.io/en/latest/concepts/index.html" target="_blank">https://llama-stack.readthedocs.io/en/latest/concepts/index.html</a>
</div>

::right::

<Transform :scale="0.95">

<!-- <<< ../distributions/masterclass-minimal/run.yaml yaml  -->
```yaml
version: "2"
image_name: masterclass_minimal
apis:
  - inference
  - telemetry
providers:
  inference:
    - provider_id: ollama
      provider_type: remote::ollama
      config:
        url: ${env.OLLAMA_URL:http://localhost:11434}
  telemetry:
    - provider_id: meta-reference
      provider_type: inline::meta-reference
      config:
        service_name: ${env.OTEL_SERVICE_NAME:}
      sinks: ${env.TELEMETRY_SINKS:console,sqlite}
      sqlite_db_path: ${env.SQLITE_STORE_DIR:~/.llama/distributions/masterclass_minimal}/trace_store.db
models:
  - metadata: {}
    model_id: meta-llama/Llama-3.2-3B-Instruct
    provider_id: ollama
    model_type: llm
    provider_model_id: llama3.2:3b-instruct-fp16 # from ollama list
server:
  host: localhost
  port: 8321
```
</Transform>

---
title: Core Concepts (mapping of APIs to resources)
hideInToc: true
---

# Core Concepts

APIs map to resources

<div class="table-container">
  <table>
    <tbody>
      <tr>
        <td>Inference, Eval and Post Training</td>
        <td>Model</td>
      </tr>
      <tr>
        <td>Safety</td>
        <td>Shield</td>
      </tr>
      <tr>
        <td>Tool Runtime</td>
        <td>ToolGroup</td>
      </tr>
      <tr>
        <td>DatasetIO</td>
        <td>Dataset</td>
      </tr>
      <tr>
        <td>VectorIO</td>
        <td>VectorDB</td>
      </tr>
      <tr>
        <td>Scoring</td>
        <td>ScoringFunction</td>
      </tr>
      <tr>
        <td>Eval</td>
        <td>Model and Benchmark</td>
      </tr>
    </tbody>
  </table>
</div>

<style>
.table-container {
  width: 100%;
  margin: 1em 0;
}

.table-container table {
  width: 100%;
  border-collapse: collapse;
}

.table-container td {
  padding: 0.5em 1em;
  border: 1px solid #ddd;
}

.table-container tr:nth-child(even) {
  background-color: #f5f5f5;
}

.table-container tr:hover {
  background-color: #eee;
}
</style>

<div class="absolute left-30px bottom-30px text-sm">
  <a href="https://llama-stack.readthedocs.io/en/latest/concepts/index.html" target="_blank">https://llama-stack.readthedocs.io/en/latest/concepts/index.html</a>
</div>

---
layout: section
title: 🎹 Let's use our stack
---
# 🎹 Let's use our stack


---
title: Let's use our stack (from the CLI)
hideInToc: true
---

# Let's use our stack
From the CLI

```bash
llama-stack-client --help
```

```bash
llama-stack-client providers list
```

```bash
llama-stack-client models list
```

```bash
llama-stack-client inference chat-completion --message "hi"
```

```bash
ChatCompletionResponse(
    completion_message=CompletionMessage(
      content='How can I assist you today?', 
      role='assistant', 
      stop_reason='end_of_turn', 
      tool_calls=[]
    ),
    logprobs=None,
    metrics=[
      Metric(metric='prompt_tokens', value=12.0, unit=None), 
      Metric(metric='completion_tokens', value=17.0, unit=None), 
      Metric(metric='total_tokens', value=29.0, unit=None)
    ]
)
```



---
title: Let's use our stack (from the Python client)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---

# Let's use our stack
From the Python client


```python
import rich
from llama_stack_client import LlamaStackClient

client = LlamaStackClient(base_url="http://0.0.0.0:8321")
models = client.models.list()
rich.print(models)
```

```python
[
    Model(
        identifier='meta-llama/Llama-3.2-3B-Instruct',
        metadata={},
        api_model_type='llm',
        provider_id='ollama',
        provider_resource_id='llama3.2:3b-instruct-fp16',
        type='model',
        model_type='llm'
    )
]
```

[client.ipynb](https://github.com/trustyai-explainability/ai-masterclass-2025/blob/main/unit-1/notebooks/client.ipynb)

::right::

```python
import rich

response = client.inference.chat_completion(
    model_id="meta-llama/Llama-3.2-3B-Instruct",
    messages=[
        {"role": "system", "content": "You are a friendly assistant."},
        {"role": "user", "content": "Write a two-sentence poem about llama."},
    ],
)
rich.print(response)
```

```python
ChatCompletionResponse(
    completion_message=CompletionMessage(
        content='Here is a short poem about a llama:\n\nWith soft fur and gentle eyes so bright,\nThe llama roams, a peaceful sight.',
        role='assistant',
        stop_reason='end_of_turn',
        tool_calls=[]
    ),
    logprobs=None,
    metrics=[
        Metric(metric='prompt_tokens', value=30.0, unit=None),
        Metric(metric='completion_tokens', value=37.0, unit=None),
        Metric(metric='total_tokens', value=67.0, unit=None)
    ]
)
```

<!-- streaming, error handling, etc -->
<!-- more ideas for out of the box: structured decoding and tracing via opentelemetry -->

---
title: Let's use our stack (from the REST API)
layout: image-right
image: /images/batteries-included.png 
backgroundSize: contain
hideInToc: true
---

# Let's use our stack  
From the REST API

http://localhost:8321/docs

```bash
curl -X POST http://localhost:8321/v1/inference/chat-completion \
  -H "Content-Type: application/json" \
  -d '{"model_id": "meta-llama/Llama-3.2-3B-Instruct", "messages": [{"role": "user", "content": "What is RAG?"}]}'
```


---
layout: section
title: 🎹 Let's break our stack
---

# 🎹 Let's break our stack


---
title: Add stuff to our stack (openai)
hideInToc: true
---

# Add stuff to our stack
*Let's brake some things ...*

- Add an OpenAI provider in the provider section
```yaml
  - provider_id: openai
    provider_type: remote::openai
    config:
      api_key: ${env.OPENAI_API_KEY:}
```

- Add an OpenAI model in the model section
```yaml
  - model_id: openai/gpt-4o
    provider_id: openai
    provider_model_id: openai/gpt-4o
```


---
title: Add stuff to our stack (tool runtime)
hideInToc: true
---

# Add stuff to our stack
*Let's brake more things ...*

- Add a tool runtime provider
```bash
$ llama stack list-providers | grep -i tool
│ tool_runtime  │ inline::rag-runtime             │ blobfile,chardet,pypdf,tqdm,numpy,scikit-learn,scipy,nltk,sentencepiece,transformers                                       │
│ tool_runtime  │ remote::bing-search             │ requests                                                                                                                   │
│ tool_runtime  │ remote::brave-search            │ requests                                                                                                                   │
│ tool_runtime  │ remote::model-context-protocol  │ mcp                                                                                                                        │
│ tool_runtime  │ remote::tavily-search           │ requests                                                                                                                   │
│ tool_runtime  │ remote::wolfram-alpha           │ requests                        
```

---
title: Add stuff to our stack (agents api)
hideInToc: true
---

# Add stuff to our stack
*Let's brake even more things ...*

- Add the agents Api
```yaml{6}
version: "2"
image_name: masterclass_minimal
apis:
  - inference
  - telemetry
  - agents
providers:
[...]  
```

---
layout: section
title: The providers registry
hideInToc: true
---
# The providers registry

---
title: The providers registry (pip dependencies)
hideInToc: true
---

# The providers registry
Different providers have different dependencies

```python
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/distribution/stack.py", line 226, in construct_stack
    impls = await resolve_impls(run_config, provider_registry or get_provider_registry(run_config), dist_registry)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/distribution/resolver.py", line 136, in resolve_impls
    return await instantiate_providers(sorted_providers, router_apis, dist_registry)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/distribution/resolver.py", line 254, in instantiate_providers
    impl = await instantiate_provider(provider, deps, inner_impls, dist_registry)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/distribution/resolver.py", line 340, in instantiate_provider
    impl = await fn(*args)
           ^^^^^^^^^^^^^^^
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/providers/remote/inference/openai/__init__.py", line 17, in get_adapter_impl
    from .openai import OpenAIInferenceAdapter
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/providers/remote/inference/openai/openai.py", line 7, in <module>
    from llama_stack.providers.utils.inference.litellm_openai_mixin import LiteLLMOpenAIMixin
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/providers/utils/inference/litellm_openai_mixin.py", line 10, in <module>
    import litellm
ModuleNotFoundError: No module named 'litellm'
```

---
title: The providers registry (pip dependencies)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---

# The providers registry

Different providers have different dependencies

```python
  File "/Users/diego/src/ai-masterclass-2025/masterclass_minimal/lib/python3.12/site-packages/llama_stack/providers/utils/inference/litellm_openai_mixin.py", line 10, in <module>
    import litellm
ModuleNotFoundError: No module named 'litellm'
```
::right::
[llama-stack/llama_stack/providers/registry/inference.py](https://github.com/meta-llama/llama-stack/blob/272d3359ee6084bdbb901543fae0df851b95ecd3/llama_stack/providers/registry/inference.py#L179-L188)
<Transform :scale="0.9">
```python{8}{lines:true}
def available_providers() -> list[ProviderSpec]:
    return [
        [...],
        remote_provider_spec(
            api=Api.inference,
            adapter=AdapterSpec(
                adapter_type="openai",
                pip_packages=["litellm"],
                module="llama_stack.providers.remote.inference.openai",
                config_class="llama_stack.providers.remote.inference.openai.OpenAIConfig",
                provider_data_validator="llama_stack.providers.remote.inference.openai.config.OpenAIProviderDataValidator",
            ),
        ),
    ]
```
</Transform>
---
title: The providers registry (api dependencies)
hideInToc: true
---

# The providers registry

Apis can depend on other apis


```python
Traceback (most recent call last):
  [...]
  File "/Users/diego/.local/share/uv/python/cpython-3.12.7-macos-aarch64-none/lib/python3.12/asyncio/runners.py", line 194, in run
    return runner.run(main)
           ^^^^^^^^^^^^^^^^
  File "/Users/diego/.local/share/uv/python/cpython-3.12.7-macos-aarch64-none/lib/python3.12/asyncio/runners.py", line 118, in run
    return self._loop.run_until_complete(task)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/diego/.local/share/uv/python/cpython-3.12.7-macos-aarch64-none/lib/python3.12/asyncio/base_events.py", line 687, in run_until_complete
    return future.result()
           ^^^^^^^^^^^^^^^
  File "/Users/diego/src/llama-stack/llama_stack/distribution/stack.py", line 226, in construct_stack
    impls = await resolve_impls(run_config, provider_registry or get_provider_registry(run_config), dist_registry)
            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/diego/src/llama-stack/llama_stack/distribution/resolver.py", line 136, in resolve_impls
    return await instantiate_providers(sorted_providers, router_apis, dist_registry)
           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/diego/src/llama-stack/llama_stack/distribution/resolver.py", line 245, in instantiate_providers
    deps = {a: impls[a] for a in provider.spec.api_dependencies}
               ~~~~~^^^
KeyError: <Api.safety: 'safety'>
```

---
title: The providers registry (api dependencies)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---

# The providers registry

Apis can depend on other apis


```python
Traceback (most recent call last):
  [...]
  File "/Users/diego/src/llama-stack/llama_stack/distribution/resolver.py", line 245, in instantiate_providers
    deps = {a: impls[a] for a in provider.spec.api_dependencies}
               ~~~~~^^^
KeyError: <Api.safety: 'safety'>
```

```bash
cat ~/src/llama-stack/llama_stack/providers/registry/agents.py
```

::right::
[llama-stack/llama_stack/providers/registry/agents.py](https://github.com/meta-llama/llama-stack/blob/272d3359ee6084bdbb901543fae0df851b95ecd3/llama_stack/providers/registry/agents.py#L30-L38)
```python{15-22}{lines:true}
def available_providers() -> list[ProviderSpec]:
    return [
        InlineProviderSpec(
            api=Api.agents,
            provider_type="inline::meta-reference",
            pip_packages=[
                "matplotlib",
                "pillow",
                "pandas",
                "scikit-learn",
            ]
            + kvstore_dependencies(),
            module="llama_stack.providers.inline.agents.meta_reference",
            config_class="llama_stack.providers.inline.agents.meta_reference.MetaReferenceAgentsImplConfig",
            api_dependencies=[
                Api.inference,
                Api.safety,
                Api.vector_io,
                Api.vector_dbs,
                Api.tool_runtime,
                Api.tool_groups,
            ],
        ),
    ]
```

---
title: External Providers
hideInToc: true
---
# External Providers
Providers that live outside of the main codebase


Llama Stack supports two types of external providers:

- Remote Providers: Providers that communicate with external services (e.g., cloud APIs)
- Inline Providers: Providers that run locally within the Llama Stack process

```yaml
external_providers_dir: /etc/llama-stack/providers.d/
```

```yaml 
adapter:
  adapter_type: custom_ollama
  pip_packages:
  - ollama
  - aiohttp
  config_class: llama_stack_ollama_provider.config.OllamaImplConfig
  module: llama_stack_ollama_provider
api_dependencies: []
optional_api_dependencies: []
```

https://llama-stack.readthedocs.io/en/latest/providers/external.html

---
title: Takeaways
---

# Takeaways

#### Concepts
- Llama Stack is a way to organize your LLM applications
- Providers are the main building blocks of Llama Stack
- You can group providers and resources into distributions

<br>

#### Dev gotchas
- There's a lot going on! Even in our minimal disto
- Providers have their own (pip) dependencies
- Apis can depend on other apis
- The build command specifies the providers list so you can create a virtual 
environment with the right dependencies

---
layout: section
title: Alternative Dev Environment Setup
hideInToc: true
---

# (Optional) <br> Alternative Dev Env Setup

---
title: Optional Dev Environment Setup (pyproject.toml)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---

# Alternative Env Setup
Single virtualenv

- Our repo has a pyproject.toml file for `uv`
```bash
cd ~/src
git clone https://github.com/trustyai-explainability/ai-masterclass-2025.git # already done 
git clone https://github.com/meta-llama/llama-stack.git # the llama stack repo
```

```bash
cat pyproject.toml
```

```bash
uv sync
source .venv/bin/activate
```

- You can then incrementally update your venv via `--print-deps` and `uv add`
```bash
llama stack build \
  --config distributions/masterclass-minimal/build.yaml \
  --image-type venv \
  --print-deps
```

```bash
uv add [...]
```

::right::

- As you `uv add` stuff, your `pyproject.toml` will update itself
- The llama-stack dependency is configured a local path and editable

```toml {7-12}{lines:true}
[project]
name = "ai-masterclass-2025"
version = "0.1.0"
description = "AI Masterclass 2025 (for the dev setup option)"
readme = "README.md"
requires-python = ">=3.12"
dependencies = [
    "llama-stack",
]

[tool.uv.sources]
llama-stack = { path = "../llama-stack", editable = true }
```

---
title: Optional Dev Environment Setup (launch.json)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---

# Alternative Env Setup
VSCode / Cursor integration

- Our repo also has a `launch.json` file for the VSCode debugger
- Your can use this to run the stack with the debugger attached, and set breakpoints in the stack code

```bash
cat .vscode/launch.json
```

::right::

<Transform :scale="0.8">
```json {*}{lines:true}
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "LS debug -- minimal-run.yaml",
      "type": "python",
      "request": "launch",
      "module": "llama_stack.cli.llama",
      "args": ["stack", "run", "distributions/masterclass-minimal/run.yaml"],
      "console": "integratedTerminal",
      "justMyCode": false,
      "cwd": "${workspaceFolder}",
      "envFile": "${workspaceFolder}/.env",
      "env": {
        "PYTHONPATH": "${workspaceFolder}"
      }
    },
    {
      "name": "LS debug -- agents-run.yaml",
      "type": "python",
      "request": "launch",
      "module": "llama_stack.cli.llama",
      "args": ["stack", "run", "distributions/masterclass-agents/run.yaml"],
      "console": "integratedTerminal",
      "justMyCode": false,
      "cwd": "${workspaceFolder}",
      "envFile": "${workspaceFolder}/.env",
      "env": {
        "PYTHONPATH": "${workspaceFolder}",
      }
    }
  ]
}
```
</Transform>


---
layout: section
title: 🎹 Implement RAG from scratch
---
# 🎹 Implement RAG from scratch
<!-- rag from scratch, and rag via agent as the prequel to agents -->

---
title: Implement RAG from scratch (exercise)
hideInToc: true
---

# Implement RAG from scratch
- Update or create a new distribution
  - [masterclass-agents/run.yaml](https://github.com/trustyai-explainability/ai-masterclass-2025/blob/main/unit-1/distributions/masterclass-agents/run.yaml)
- Register a vector database from the client
- Implement a basic RAG pipeline in a notebook
  - Insert a few documents
  - Query them
  - Generate response with context
- (No Agents for now)

<!-- 
## very vague exercise
- on purpose
- hints in run.yaml
- read the docs
- [PAUSE]
careful! pause here! next slide reveals solution 
-->

---
title: Implement RAG from scratch (solution)
layout: two-cols
layoutClass: gap-3
hideInToc: true
---

# Implement RAG from scratch

```python
vector_db_id = "my-vector-db"
client.vector_dbs.register(
    vector_db_id=vector_db_id,
    embedding_model="all-MiniLM-L6-v2",
    embedding_dimension=384,
)
```

```python
client.tool_runtime.rag_tool.insert(
    documents=documents,
    vector_db_id=vector_db_id,
    chunk_size_in_tokens=512,
)
```

```python
client.tool_runtime.rag_tool.query(
    content=prompt, vector_db_ids=[vector_db_id]
)
```

```python
db_response = client.vector_io.query(
    vector_db_id=vector_db_id,
    query=prompt,
)
```

::right::

```python
f"""
Please answer the given query using the context below.

QUERY:
{prompt}

CONTEXT:
{prompt_context}
"""
```
```python
response = client.inference.chat_completion(
    messages=messages,
    model_id="meta-llama/Llama-3.2-3B-Instruct",
)
```

---
title: Implement RAG from scratch (Agent version & solution)
hideInToc: true
---

# Implement RAG from scratch (Agent version)

```python
rag_agent = Agent(
    client, 
    model="meta-llama/Llama-3.2-3B-Instruct",
    instructions="You are a helpful assistant",
    tools = [
        {
          "name": "builtin::rag/knowledge_search",
          "args" : {
            "vector_db_ids": [vector_db_id],
          }
        }
    ],
)
```

[rag.ipynb](https://github.com/trustyai-explainability/ai-masterclass-2025/blob/main/unit-1/notebooks/rag.ipynb)


---
layout: section
---

# Agents

---
title: What is an agent?
layout: quote 
hideInToc: true
---

# What is an agent?
Some definitions

From [Hugging Face's Agents Course](https://huggingface.co/learn/agents-course/unit1/what-are-agents):

> *An Agent is a system that leverages an AI model to interact with its environment in order to achieve a user-defined objective. It combines reasoning, planning, and the execution of actions (often via external tools) to fulfill tasks.*

From [Anthropic's Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents):

> - *Workflows are systems where LLMs and tools are orchestrated through predefined code paths.*

> - *Agents, on the other hand, are systems where LLMs dynamically direct their own processes and tool usage, maintaining control over how they accomplish tasks.*




---
title: Tools
hideInToc: true
---
# Tools
From [Hugging Face's Agents Course](https://huggingface.co/learn/agents-course)

- LLMs can only receive text inputs and generate text outputs. They have no way to call tools on their own. 
- When we talk about providing tools to an Agent, we mean teaching the LLM about the existence of these tools and instructing it to generate text-based invocations when needed. 
- From the user’s perspective, it appears as if the LLM directly interacted with the tool, but in reality, it was the Agent that handled the entire execution process in the background.
- How do we give tools to an LLM?

![tool-prompt](/images/tool-prompt.png)


---
title: Agents on Llama Stack
layout: two-cols
layoutClass: gap-3
---

# Agents on Llama Stack
Basic concepts

- Agent Configuration
  - Model
  - Instructions
  - Tools
  - Shields
- Session
  - conversation thread with an agent
- Turn
  - a single interaction within a session
- Step
  - individual actions within a turn (inference, tool execution, shield calls, etc)
  

::right::

```python
agent = Agent(
    llama_stack_client,
    model="my-model",
    instructions="You are a helpful assistant that can use tools to answer questions.",
    tools=["my-tool", "my-other-tool"],
    input_shields=["guardrails::my-filter"],
    output_shields=["guardrails::my-filter"],
)
```

```python
session_id = agent.create_session("test-session")
```

```python
response = agent.create_turn(
  messages=[{"role": "user", "content": prompt}],
  session_id=session_id,
)
```


---
title: Execution model
layout: two-cols
---

# Agents on Llama Stack
Execution model

1. Initial Safety Check
2. Inference Loop
   - Augment with context
   - Generate a response, potentially with tool calls and safety checks
   - Repeat
3. Final Safety Check


::right::
![Llama Stack execution model](/images/ls-exec-loop.png)

---
title: Execution model, details
hideInToc: true
---

# Execution model, details

[llama_stack/providers/inline/agents/meta_reference/agent_instance.py](https://github.com/meta-llama/llama-stack/blob/272d3359ee6084bdbb901543fae0df851b95ecd3/llama_stack/providers/inline/agents/meta_reference/agent_instance.py#L320)

```python
   async def run(self, session_id, turn_id, input_messages, sampling_params, stream, documents):
       # 1. Input Safety Checks
       if len(self.input_shields) > 0:
           # Run input safety shields
           async for res in self.run_multiple_shields_wrapper(...):
               yield res

       # 2. Main Agent Execution
       async for res in self._run(...):
           if isinstance(res, CompletionMessage):
               final_response = res
               break
           else:
               yield res

       # 3. Output Safety Checks
       if len(self.output_shields) > 0:
           # Run output safety shields
           async for res in self.run_multiple_shields_wrapper(...):
               yield res
```
---
layout: section
title: 🎹 An agent that can find its location
---
# 🎹 An agent that can find its location

<!-- 
- so how do we create a tool?
- how do we use it in an agent?
- this is our first agent, so we will do it together
 -->

---
title: An agent that can find its location
hideInToc: true
---
# An agent that can find its location
A tool to get a user's location

```python
from llama_stack_client.lib.agents.client_tool import client_tool

@client_tool
def get_location(query: str = "location"):
    """
    Provide the location upon request.

    :param query: The query from user
    :returns: Information about user location
    """
    import geocoder
    
    try:
        g = geocoder.ip('me')
        if g.ok:
            return f"Your current location is: {g.city}, {g.state}, {g.country}"
        else:
            return "Unable to determine your location"
    except Exception as e:
        return f"Error getting location: {str(e)}"
```

<!-- 
- this is our first agent, so we will do it together
 -->

---
title: An agent that can find its location
hideInToc: true
---
# An agent that can find its location
Create an agent to use the `get_location` tool

```python
agent = Agent(
    client, 
    model="meta-llama/Llama-3.2-3B-Instruct",
    instructions="You are a helpful assistant.",
    tools=[get_location],
)
```

```python
user_prompts = ["Where am I?"]
session_id = agent.create_session("test-session")
for prompt in user_prompts:
    rich.print(f"User> {prompt}")

    response = agent.create_turn(
        messages=[{"role": "user", "content": prompt}],
        session_id=session_id,
        stream=True,
    )
    for log in AgentEventLogger().log(response):
        log.print()
```

[tool.ipynb](https://github.com/trustyai-explainability/ai-masterclass-2025/blob/main/unit-1/notebooks/tool.ipynb)

<!-- 
- this is our first agent, so we will do it together
- pause to let people catch up
 -->

---
title: Supported Models
hideInToc: true
---
# Supported Models
Verify your  `identifier` and `provider_resource_id`
```
$ llama-stack-client models list

Available Models

┏━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━┳━━━━━━━━━━━━━┓
┃ model_type   ┃ identifier                           ┃ provider_resource_id         ┃ metadata  ┃ provider_id ┃
┡━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━╇━━━━━━━━━━━━━┩
│ llm          │ meta-llama/Llama-3.2-3B-Instruct     │ llama3.2:3b-instruct-fp16    │           │ ollama      │
└──────────────┴──────────────────────────────────────┴──────────────────────────────┴───────────┴─────────────┘

Total models: 1
```

- When using an agent with tools, the prompt gets modified depending on the model family. 
- [Supported models](https://llama-stack.readthedocs.io/en/latest/distributions/self_hosted_distro/ollama.html)
- [llama_stack/providers/remote/inference/ollama/models.py](https://github.com/meta-llama/llama-stack/blob/main/llama_stack/providers/remote/inference/ollama/models.py)

---
layout: section
title: 🎹 An agent that can search the web
---
# 🎹 An agent that can search the web

---
title: An agent that can search the web (exercise)
hideInToc: true
---
# An agent that can search the web

```python
agent = Agent(
    client,
    model="meta-llama/Llama-3.2-3B-Instruct",
    instructions="You are a helpful assistant.",
    tools=["builtin::websearch"],
)
```

- Give your previous agent a tool to search the web
- Combine it with the `get_location` tool
- Use it to provide answers that are relevant to the user's location
- Pick from the Brave API or the Tavily API (https://tavily.com/)

<!-- 
- [PAUSE]
- this one has no solution
-->

---
layout: section
title: 🎹 An agent that can read files
---
# 🎹 An agent that can read files

---
title: Model Context Protocol
hideInToc: true
layout: two-cols
layoutClass: gap-3 
---
# Model Context Protocol
https://modelcontextprotocol.io/introduction

> MCP is an open protocol that standardizes how applications provide context to LLMs.

<br>

- Hosts are LLM applications that initiate connections
- Clients maintain 1:1 connections with servers, inside the host application
- Servers provide context, tools, and prompts to clients
- Transport
  - Stdio
  - HTTP/SSE
::right::
<Transform :scale="0.9">

![MCP architecture](/images/mcp-arch.png)
</Transform>

---
title: Model Context Protocol
hideInToc: true
---
# Model Context Protocol
Spin up a local MCP server

```bash
npx -y supergateway --port 8000 --stdio 'npx -y @modelcontextprotocol/server-filesystem my-local-files'
```

```bash
[supergateway] Starting...
[supergateway] Supergateway is supported by Supermachine (hosted MCPs) - https://supermachine.ai
[supergateway]   - outputTransport: sse
[supergateway]   - Headers: (none)
[supergateway]   - port: 8000
[supergateway]   - stdio: npx -y @modelcontextprotocol/server-filesystem my-local-files
[supergateway]   - ssePath: /sse
[supergateway]   - messagePath: /message
[supergateway]   - CORS: disabled
[supergateway]   - Health endpoints: (none)
[supergateway] Listening on port 8000
[supergateway] SSE endpoint: http://localhost:8000/sse
[supergateway] POST messages: http://localhost:8000/message
[supergateway] Child stderr: Secure MCP Filesystem Server running on stdio

[supergateway] Child stderr: Allowed directories: [ '/Users/diego/src/ai-masterclass-2025/my-local-files' ]
```

---
title: Model Context Protocol
hideInToc: true
layout: image-right
image: /images/mcp-inspector.png
backgroundSize: contain
---
# Model Context Protocol
Inspect the MCP server
```bash
npx -y @modelcontextprotocol/inspector
Starting MCP inspector...
⚙️ Proxy server listening on port 6277
🔍 MCP Inspector is up and running at http://127.0.0.1:6274 🚀
```

---
title: An agent that can read files (exercise)
hideInToc: true
---
# An agent that can read files

```python
agent = Agent(
    client,
    model="meta-llama/Llama-3.2-3B-Instruct",
    instructions="You are a helpful assistant.",
    tools=["mcp::filesystem"],
)
```

- Create a local directory with your files for testing
- Setup the filesystem MCP server
- Add a MCP provider to your stack
- Create an MCP agent

<!-- 
- [PAUSE]
-->

---
title: An agent that can read files (solution)
hideInToc: true
---
# An agent that can read files

[mcp.ipynb](https://github.com/trustyai-explainability/ai-masterclass-2025/blob/main/unit-1/notebooks/mcp.ipynb)

---
layout: section
title: 🎹 A “reasoning and acting” (ReAct) agent
---
# 🎹 A “reasoning and acting” (ReAct) agent

---
title: A “reasoning and acting” (ReAct) agent
hideInToc: true
---
# A “reasoning and acting” (ReAct) agent
ReAct agents are more flexible and can handle more complex tasks

[llama_stack_client/lib/agents/react/prompts.py](https://github.com/meta-llama/llama-stack-client-python/blob/62bd12799d8a4a0261d200d1c869e2be98c38770/src/llama_stack_client/lib/agents/react/prompts.py)

```
You are an expert assistant who can solve any task using tool calls. 
You will be given a task to solve as best you can.
To do so, you have been given access to the following tools: <<tool_names>>

You must always respond in the following JSON format:
{
    "thought": $THOUGHT_PROCESS,
    "action": {
        "tool_name": $TOOL_NAME,
        "tool_params": $TOOL_PARAMS
    },
    "answer": $ANSWER
}
[...]
This Thought/Action/Observation can repeat N times, you should take several steps when needed.
[...]
You can use the result of the previous action as input for the next action.
```

---
title: A “reasoning and acting” (ReAct) agent
hideInToc: true
---
# A “reasoning and acting” (ReAct) agent
ReAct agents are more flexible and can handle more complex tasks

Learn more about ReAct agents:
  - https://www.ibm.com/think/topics/react-agent
  - [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)

---
title: A “reasoning and acting” (ReAct) agent (exercise)
hideInToc: true
---
# A “reasoning and acting” (ReAct) agent

```python
from llama_stack_client.lib.agents.react.agent import ReActAgent
```

- Compare a basic agent with a chain of prompts vs a ReAct agent
- Should be able to ask "Are there any weather-related risks in my area?" 
  - figure out it first needs to call the `get_location` tool;
  - and then use the `builtin::websearch` tool.


<!-- 
- [PAUSE]
-->
---
title: A “reasoning and acting” (ReAct) agent (solution)
hideInToc: true
---
# A “reasoning and acting” (ReAct) agent

[react.ipynb](https://github.com/trustyai-explainability/ai-masterclass-2025/blob/main/unit-1/notebooks/react.ipynb)

---
layout: statement
title: Thank You!
hideInToc: true
---
# Thank You!

