---
layout: single
title: "Toolformer (2023-02-10)"
categories: [paper]
tag: [Language Models, Self-supervised Learning, External Tools, API, Zero-shot Learning]
toc: true
toc_sticky: true
toc_label: Contents
---

Recent research proposes Toolformer, a model that can teach itself to use external tools via simple APIs in a self-supervised way. Augmented Language Models (ALMs) can use external modules to expand their context processing ability and learn to reason and use tools while still performing natural language tasks. However, tool-use agents face challenges in deciding when and how to use external tools, and require significant human supervision. Progress has been made on self-supervised learning of tool use with language models, but interactive tool use has not been explored yet.

# Toolformer: Language Models Can Teach Themselves to Use Tools
[arxiv](https://arxiv.org/pdf/2302.04761.pdf)
- LMs are good at solving new tasks with just a few examples but struggle with some basic tasks. Toolformer is a model that can teach itself to use external tools via simple APIs and achieve better performance on downstream tasks without sacrificing its core language modeling abilities.

1️⃣ The underlying assumption of this paper is that language models can be taught to use external tools through simple APIs, and that this approach can improve their zero-shot performance on downstream tasks.

2️⃣ The methodology used in this paper is the development of a new model called Toolformer, which is trained to decide which APIs to call, when to call them, what arguments to pass, and how to best incorporate the results into future token prediction. The model is trained in a self-supervised way, requiring only a handful of demonstrations for each API. The researchers incorporate a range of tools into the model, including a calculator, a Q&A system, two search engines, a translation system, and a calendar.

3️⃣ The implications of this research are that language models can be enhanced to perform better on a variety of downstream tasks by incorporating external tools via simple APIs. This could have significant applications in natural language processing and artificial intelligence, particularly in cases where complex information retrieval or processing is required.

## Augmented Language Models: a Survey
- This survey discusses Augmented Language Models (ALMs), which augment LMs with reasoning and tool use abilities. ALMs can use external modules to expand their context processing ability, and can learn to reason and use tools while still performing natural language tasks. ALMs have the potential to address limitations of traditional LMs such as interpretability, consistency, and scalability.

> Recently, Schick et al. (2023) proposed Toolformer, a model that teaches itself to use tools in a self-supervised way. This is achieved by ﬁrst using the few-shot abilities of an existing LM to sample a large amount of potential tool uses. For instance, the model can call a calculator API to augment its context, e.g., “Out of 1400 participants, 400 (or [Calculator(400 / 1400)→ 0.29] 29% passed the test.” Then, the model is ﬁne-tuned on its own generations, ﬁltering them based on whether they reduce perplexity for future tokens generations. This method enables using several tools (e.g., a calendar, a calculator, or an information retrieval system). However, it was tested in a limited setup of using a single tool at once, since examples of tool use were independently sampled. We believe that studying how this approach could be extended to more complex multi-step tool uses is a promising research direction for a generalist LM-based agent.

## Foundation Models for Decision Making: Problems, Methods, and Opportunities
- Tool-use agents face challenges in deciding when and how to use external tools, and require significant human supervision. Language models can struggle with the prompt formats and require rule-based parsers to clean up communication with external tools. Some progress has been made on self-supervised learning of tool use with language models, but interactive tool use has not been explored yet.