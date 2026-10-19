# Colin McNamara

I'm exploring how mixtures of models can enhance human, system, and agentic cognition through semantic routing, as we augment ourselves with fleets of digital entities.

Right now I'm learning these bleeding-edge codebases from the data plane up. Much of that work makes `/v1/messages` (Anthropic) a first-class citizen alongside `/v1/chat/completions` (OpenAI). In practice that means finding bugs, fixing them upstream so every user gets the fix, and learning how it all works along the way. Austin, Texas.

- Member of the **Data Plane & Networking** work group in [vLLM Semantic Router](https://vllm-sr.ai/community/work-groups)
- Run **[AIMUG](https://aimug.org)**, the AI Middleware Users Group: 2,200+ members, free monthly meetups in Austin and online
- Field CTO at [AHEAD](https://www.ahead.com), where I work with enterprise customers on AI infrastructure

## Security

| Project | Advisory | Severity | Finding |
|---|---|---|---|
| vLLM Semantic Router | [GHSA-xr66-pq9r-2c8j](https://github.com/vllm-project/semantic-router/security/advisories/GHSA-xr66-pq9r-2c8j) | High | The Router's Istio EnvoyFilter reused the `ext_proc` filter name, so a client header could bypass the Router. Reported and [fixed](https://github.com/vllm-project/semantic-router/commit/363a1765da64b4dc8fd922396d715e12dfd958ed). |

## Merged upstream

| Project | PR | Fix |
|---|---|---|
| NVIDIA Switchyard | [#884](https://github.com/NVIDIA-NeMo/Switchyard/pull/884) | Return HTTP 502 for buffered Chat `abort`, `error` and `repetition` finish reasons |
| vLLM Semantic Router | [#4901](https://github.com/vllm-project/semantic-router/pull/4901) | Accept vLLM's integer error code in Chat stream decoding |
| vLLM Semantic Router | [#4931](https://github.com/vllm-project/semantic-router/pull/4931) | Decode a Chat target's opening delta immediately (co-author) |
| vLLM Semantic Router | [#4658](https://github.com/vllm-project/semantic-router/pull/4658) | Decode Chat reasoning before the answer, so streamed Messages finish |
| vLLM Semantic Router | [#4539](https://github.com/vllm-project/semantic-router/pull/4539) | Accept vLLM Chat `stop_reason` strings over 128 bytes |
| vLLM Semantic Router | [#4391](https://github.com/vllm-project/semantic-router/pull/4391) | Keep vLLM's matched stop sequence for Anthropic clients |
| vLLM Semantic Router | [#4266](https://github.com/vllm-project/semantic-router/pull/4266) | Hold the full-duplex header reply until the body is routed |
| vLLM | [#55325](https://github.com/vllm-project/vllm/pull/55325) | Set `stop_sequence` in the streaming `message_delta` event |

[All my PRs in these projects, merged and in review](https://github.com/search?q=is%3Apr+author%3Acolinmcnamara+repo%3Avllm-project%2Fvllm+repo%3Avllm-project%2Fsemantic-router+repo%3ANVIDIA-NeMo%2FSwitchyard&type=pullrequests)

## Projects

- **[gh-upstream-watch](https://github.com/colinmcnamara/gh-upstream-watch)**: read-only alerts for upstream work that name the next action when a maintainer gate, a competing PR or a review moves. On [PyPI](https://pypi.org/project/gh-upstream-watch/).
- **[two-routers-one-loop](https://github.com/colinmcnamara/two-routers-one-loop)**: reproducible tests for two routing decisions in one Kubernetes gateway path: vLLM Semantic Router picks the model, llm-d's endpoint picker picks the pod.
- **[jev-first-look](https://github.com/colinmcnamara/jev-first-look)**: scripts and raw results from a first hands-on look at TypeSafe AI's Jev decision model.

## Talks and writing

- [Mixture of models and semantic routing](https://aimug.org/talks/mixture-of-models-and-semantic-routing/) (AIMUG) and [every talk I've given there](https://aimug.org/speakers/colin-mcnamara/)
- [The Router Was Right](https://colinmcnamara.com/blog/the-router-was-right)
- [The Engine Is the Other Half of the Model](https://colinmcnamara.com/blog/engine-other-half-of-the-model)
- [A Model That Refuses to Talk](https://colinmcnamara.com/blog/jev-system-one-decision-models)
- More at [colinmcnamara.com](https://colinmcnamara.com)
