# XAI Privacy

We build tools to audit and improve the **legal compliance of large language models** through explainable AI and causal inference.

## Why this work

LLMs are increasingly deployed in high-stakes settings: finance, healthcare, employment, housing, and government services. Their opaque processing of personal data makes it hard to verify whether they comply with privacy and anti-discrimination law. Existing XAI methods like LIME and SHAP can show *correlation* between inputs and outputs, but laws such as the California Consumer Privacy Act require *causation*: data processing must be "reasonably necessary" for a stated purpose.

We are developing a **Compliance Audit Framework** that uses causal inference to verify LLM adherence to two foundational legal principles: **data minimization** and **purpose limitation**.

## Research agenda

Our work spans four connected research areas:

1. **Compliance Audit Benchmark (CAB).** A causal, counterfactual evaluation suite for testing LLM behavior in finance, healthcare, and employment domains. Each test case pairs a prompt and context with a non-compliant behavior and a counterfactual compliant one. CAB provides the foundation that enables everything else.
2. **Empirical evaluation using causal factor analysis.** Interventional, do-operation-style probes that move beyond correlation to identify the actual causal drivers of an LLM's decision, evaluated against CAB.
3. **Compliance Audit Framework and Minimal-cause Explainer.** A causal framework for detecting non-compliance, anchored by a Minimal-cause Explainer that identifies the smallest set of input features that would need to change for a non-compliant output to become compliant. The goal is to give auditors actionable, legally meaningful guidance.
4. **Causal Intervention Component.** A causally-supervised guardrail that integrates with the Explainer to mitigate detected compliance issues in real time during deployment.

## Repositories

📊 **[compliance-audit-benchmark](https://github.com/xai-privacy/compliance-audit-benchmark)**: Data, scripts, and artifacts of CAB. MIT licensed.

Additional repositories covering the framework, explainer, and intervention component will be released as those parts of the project mature.

## Team and affiliation

XAI Privacy is a collaboration between researchers in computer science, security, and law, spanning academia and industry.

Faculty leads:

* Prof. Sebastian Zimmeck, Wesleyan University, [Privacy Tech Lab](https://privacytechlab.org)
* Prof. Baishakhi Ray, Columbia University
* Prof. Pooyan Jamshidi, University of South Carolina

We also work with industry collaborators on real-world validation of the framework.

## Contact

For questions, collaboration, or partnership inquiries: [sebastian@privacytechlab.org](mailto:sebastian@privacytechlab.org)

---

*Our intent is to release data, benchmarks, software, and findings openly under permissive open source licenses.*
