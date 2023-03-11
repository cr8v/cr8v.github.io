---
layout: single
title: "Toolformer (2023-02-10)"
categories: [Daily Digest]
tag: [toolformer, LLM]
toc: true
toc_sticky: true
toc_label: Contents
---

Recent research proposes Toolformer, a model that can teach itself to use external tools via simple APIs in a self-supervised way. Augmented Language Models (ALMs) can use external modules to expand their context processing ability and learn to reason and use tools while still performing natural language tasks. However, tool-use agents face challenges in deciding when and how to use external tools, and require significant human supervision. Progress has been made on self-supervised learning of tool use with language models, but interactive tool use has not been explored yet.

# Toolformer: Language Models Can Teach Themselves to Use Tools
- [arxiv](https://arxiv.org/pdf/2302.04761.pdf)
- Language modeling, External tool integration, Self-supervised learning, Zero-shot learning, Downstream tasks
- LMs are goot at solving new tasks with just a few examples but struggle with some basic tasks. Toolformer is a model that can teach itself to use external tools via simple APIs and achieve better performance on downstream tasks without sacrificing its core language modeling abilities.

## Augmented Language Models: a Survey
- This survey discusses Augmented Language Models (ALMs), which augment LMs with reasoning and tool use abilities. ALMs can use external modules to expand their context processing ability, and can learn to reason and use tools while still performing natural language tasks. ALMs have the potential to address limitations of traditional LMs such as interpretability, consistency, and scalability.

"Recently, Schick et al. (2023) proposed Toolformer, a model that teaches itself to use tools in a self-supervised way. This is achieved by ﬁrst using the few-shot abilities of an existing LM to sample a large amount of potential tool uses. For instance, the model can call a calculator API to augment its context, e.g., “Out of 1400 participants, 400 (or [Calculator(400 / 1400)→ 0.29] 29% passed the test.” Then, the model is ﬁne-tuned on its own generations, ﬁltering them based on whether they reduce perplexity for future tokens generations. This method enables using several tools (e.g., a calendar, a calculator, or an information retrieval system). However, it was tested in a limited setup of using a single tool at once, since examples of tool use were independently sampled. We believe that studying how this approach could be extended to more complex multi-step tool uses is a promising research direction for a generalist LM-based agent."

## Foundation Models for Decision Making: Problems, Methods, and Opportunities
Tool-use agents face challenges in deciding when and how to use external tools, and require significant human supervision. Language models can struggle with the prompt formats and require rule-based parsers to clean up communication with external tools. Some progress has been made on self-supervised learning of tool use with language models, but interactive tool use has not been explored yet.