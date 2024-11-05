---
layout: post
title:  "Introduction"

---
What Do Cross-language Dependencies Tell Us About Software Ecosystem Health?


In large-scale software development, multilingual projects, those involving multiple interacting programming languages, have become increasingly common in both industry and the open-source community. Research indicates that cross-language dependencies in these projects can increase the likelihood of risks, such as functionality defects and security vulnerabilities. While most existing studies focus on cross-language dependency analysis between host languages and specific guest languages, such as C/C++, prior works have rarely explored how host languages interact with other guest languages or the broader impact of these cross-language dependencies on the software ecosystems. 



To address the above limitations, in this paper, we develop a technique, *Diplomatist*, to identify and analyze cross-language dependencies between host languages, such as Java, and guest languages, including JavaScript, Python, Ruby, PHP, and C/C++. *Diplomatist* automatically analyzes *cross-language invocation APIs* and constructs a large-scale knowledge repository to standardize the code features for identifying library versions across various guest languages, allowing the tracing of guest language libraries invoked by host languages. Evaluation shows that *Diplomatist* achieved an average precision of 88.9% and a recall of 91.5% on a high-quality benchmark, indicating its high accuracy in detecting cross-language dependencies. It is found that 435,258 Java libraries, indirect or transitively depend on libraries from other ecosystems. To evaluate the usefulness of *Diplomatist*, we conduct a case study to examine the impact of the risks introduced due to cross-language dependencies on programming language ecosystems, by analyzing a full-picture of the cross-language dependency graph. The results indicate that fragile projects or libraries introduce security issues from other ecosystems by cross-language dependencies, affecting 13,739 downstream projects in the *Maven* ecosystem. We utilized *Diplomatist* to provide remediation suggestions to relevant project developers. Issue reports of some subjects have been confirmed by developers.