---
layout: default
title: Project Reflections
---

# Mingrui Zhuang

**UCSD email:** m1zhuang@ucsd.edu

**Section:** D26 - Trustworthy Large Language Models

**Mentor:** Professor Lily Weng

## Quarter 2 Project Reflections

**What is the most interesting topic covered in your domain this quarter?**

The topic I find most interesting is failure diagnosis and adaptive correction in retrieval-augmented generation (RAG). An incorrect answer can arise from many aspects, such as the retrieved passages lack necessary information, contain distracting information, or are used incorrectly by the model. We need different responses for these situations. Particularly, I'm interested in whether explicitly naming the failure helps a system select a better correction when compared with selecting a correction directly at comparable inference cost. This connects the goal of making language models more reliable with the practical question of how to use limited computation effectively.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to investigate a RAG repair system that learns to balance answer accuracy and computation without requiring explicit error-type labels or manually annotated best repair actions. Our small pilot has not shown a clear benefit from providing an error label under the tested conditions, which motivates exploring direct repair decisions further. Building on the current learned action selector, I would study whether a controller can also learn when to preserve an answer, request additional verification, or perform a repair. It would learn from feedback about answer quality and the cost of its decisions. I would compare accuracy, latency, token use, and unnecessary repairs across controlled evidence conditions.

**What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**

A change, or next step, I would make is to expand the small pilot experiment into a larger held-out evaluation to get more samples and better compair between repair policies. I also need more data and detailed control to measure inference costs and results for each evidence condition. I think the current evidence condition can't create a enough ambiguous situation to confuse LLM. With the original reproduction's reference-containment scoring, I would also report normalized exact match and token-level F1.

**What other techniques would you be interested in using in your project?**

I would like to understand contextual bandit methods such as LinUCB more deeply, particularly how feedback about answer quality and computation can guide repair decisions. From our original proposed pipeline, I am also interested in selective reranking and claim-level verification that mentioned in our previous pipeline. I would investigate when these extra steps are useful enough to justify their cost and when the system should stop repairing. I do not yet have much experience with these techniques, so I would need to begin with simple implementations and evaluate each component separately before combining them.
