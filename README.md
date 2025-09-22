# Python-Screening-Task-3
Python Screening Task 3: Evaluating Open Source Models for Student Competence Analysis


# Research Plan
This research aims to systematically evaluate and select optimal AI models for high-level competence analysis across multiple domains including reasoning, language understanding, coding proficiency, and multimodal capabilities. The primary objective is to identify models that can accurately assess, generate meaningful prompts for, and provide interpretable evaluations of complex competencies while maintaining cost-effectiveness for deployment scenarios. The research will focus on five leading AI model families: OpenAI's gpt-oss series (120B and 20B variants), Google's Gemma 3 family (particularly the 27B model), Microsoft's AutoGen framework with Azure AI Language services, IBM's Granite 3.0 series (8B model), and NVIDIA's Nemotron Nano 2 and Qwen3-Next models.

The investigation will employ a multi-dimensional evaluation framework incorporating standardized benchmarks (MMLU, AIME, GSM8K, HumanEval), domain-specific competence assessments, and practical deployment considerations. Each model will be assessed across three critical dimensions: accuracy in competence evaluation tasks, interpretability of decision-making processes, and computational cost-effectiveness. The research will utilize both automated evaluation metrics and human expert validation to ensure robust assessment of model capabilities in generating meaningful prompts and evaluating high-level competencies across diverse professional and academic contexts.

## Approach to identifying and evaluating relevant models
**Phase 1: Technical Specification Analysis**
-	Parameter count and architecture assessment (Dense vs MoE models)
-	Context window capabilities (32K-128K tokens)
-	Multimodal support (text, image, code)
-	Training data scope (12+ trillion tokens, 140+ languages)
-	Inference efficiency metrics (throughput, memory requirements)

**Phase 2: Benchmark Performance Evaluation**
- Academic benchmarks: MMLU (general knowledge), AIME (mathematical reasoning), GSM8K (problem-solving)
- Code generation: HumanEval, MBPP, LiveCodeBench
-	Reasoning capabilities: Big-Bench Hard, GPQA Diamond
-	Language understanding: HellaSwag, WinoGrande, TruthfulQA
- Instruction following: IFEval scores

**Phase 3: Domain-Specific Competence Assessment**
-	Professional skill evaluation (legal, medical, technical domains)
-	Critical thinking and analytical reasoning tasks
-	Creative problem-solving scenarios
-	Ethical reasoning and bias detection
-	Long-context reasoning abilities (RULER-128K benchmark)


## How you would test or validate their applicability to the problem?
**Approach 1: Multi-Criteria Decision Analysis (MCDA)**
Each model will be evaluated using a weighted scoring system across:
  - Accuracy (40%): Performance on standardized competence benchmarks
  - Interpretability (30%): Explainability of reasoning processes and decision pathways
  - Cost-effectiveness (20%): Inference cost per evaluation, deployment requirements
  - Robustness (10%): Consistency across diverse prompts and contexts

**Approach 2: Human Expert Validation**
  - Domain expert evaluation of model outputs across 5 professional areas
  - Comparative analysis with gold-standard human assessments
  - Inter-rater reliability testing with multiple evaluators
  - Bias detection through diverse demographic and cultural perspectives

**Approach 3: Real-World Deployment Testing**
  - A/B testing in controlled educational/professional environments
  -	Performance monitoring over extended periods (3-6 months)
  -	User satisfaction and adoption metrics
  -	Cost analysis in production scenarios


## Reasoning and decision-making process
<details>
  <summary> Q. What makes a model suitable for high-level competence analysis? </summary>
  A model suitable for high-level competence analysis must demonstrate several critical capabilities:
  Reasoning Depth: The model must exhibit sophisticated logical reasoning, evidenced by strong performance on benchmarks like AIME (mathematical competition problems) and GPQA (graduate-level science questions). The selected gpt-oss-120b achieves 90.0% on MMLU and 93.0% on competition coding tasks, while Gemma 3-27B demonstrates 78.6% on MMLU and 82.6% on GSM8K.
  Contextual Understanding: High competence analysis requires processing complex, multi-faceted scenarios. Models with extended context windows (128K tokens) like Gemma 3 and gpt-oss series can maintain coherence across lengthy professional scenarios and documentation.
  Domain Expertise: The model must demonstrate knowledge across diverse professional domains. IBM Granite 3.0's training on 116 programming languages and enterprise-specific data makes it particularly suitable for technical competence evaluation, while AutoGen's multi-agent architecture allows specialized domain expertise through agent composition.
  Metacognitive Awareness: The ability to assess its own reasoning and identify knowledge limitations is crucial. This is evidenced through calibration scores and the model's capacity to express uncertainty appropriately.
</details>

<details>
  <summary> Q. How would you test whether a model generates meaningful prompts? </summary>
  Prompt Quality Assessment Framework:
  1.	Clarity and Specificity Metrics:
  -	Linguistic analysis of prompt structure and complexity
  -	Domain expert rating of prompt clarity (1-10 scale)
  -	Automated assessment of specificity using entropy measures
  2.	Response Quality Correlation:
  -	Comparison of responses generated from model-created vs expert-crafted prompts
  -	Inter-prompt reliability testing across multiple response generations
  -	Quality degradation analysis when prompts are simplified or modified
  3.	Competence Alignment Testing:
  -	Verification that prompts accurately target intended competency dimensions
  -	Cross-validation with established competency frameworks (UNESCO AI Competency, etc.)
  -	Expert panel validation of prompt-competency alignment
  4.	Prompt Effectiveness Metrics:
  -	Success rate in eliciting demonstrable competency indicators
  -	Discriminative power in distinguishing competency levels
  -	Consistency across diverse demographic and cultural contexts

</details>

<details>
  <summary> Q. What trade-offs might exist between accuracy, interpretability, and cost? </summary>
  Accuracy vs. Cost Trade-offs:
  •	High-accuracy models like gpt-oss-120b require substantial computational resources (80GB GPU minimum) but deliver superior performance on complex reasoning tasks
  •	Cost-efficient alternatives like Nemotron-Nano-9B-v2 provide 6x faster inference while maintaining competitive accuracy on many benchmarks
  •	Deployment scenarios significantly impact cost-effectiveness: cloud-based inference vs. on-premises deployment vs. edge computing
  Interpretability vs. Accuracy Trade-offs:
  •	Complex models (MoE architectures) often provide higher accuracy but reduced interpretability of decision pathways
  •	Simpler architectures like dense transformer models offer clearer reasoning traces but may sacrifice performance on nuanced tasks
  •	Hybrid approaches using AutoGen's multi-agent system provide interpretability through agent specialization while maintaining high overall performance
  Practical Trade-off Matrix:
  •	Enterprise deployment: IBM Granite 3.0 balances interpretability needs with enterprise security requirements
  •	Research applications: gpt-oss models provide maximum accuracy with full reasoning chain access
  •	Real-time applications: Nemotron-Nano models optimize for speed while maintaining acceptable accuracy levels
  •	Resource-constrained environments: Gemma 3 smaller variants (1B, 4B) provide deployment flexibility
</details>

<details>
  <summary> Q. Why did you choose the model you evaluated, and what are its strengths or limitations? </summary>
  Selected Model: IBM Granite 3.0-8B-Instruct
  Selection Rationale:
  1.	Enterprise Readiness: Designed specifically for professional competence evaluation with comprehensive safety guardrails
  2.	Balanced Performance: Achieves 69.04% on Open LLM Leaderboard while maintaining 8B parameter efficiency
  3.	Interpretability: Provides clear reasoning traces essential for competence assessment validity
  4.	Cost-Effectiveness: Moderate computational requirements suitable for institutional deployment
  5.	Domain Coverage: Training on 12 trillion tokens across 116 programming languages supports diverse competency domains
  Key Strengths:
  •	Function Calling Capabilities: Native support for tool use essential in competence evaluation scenarios
  •	Apache 2.0 License: Enables customization and fine-tuning for specific competency frameworks
  •	Enterprise Focus: Optimized for professional contexts with appropriate ethical safeguards
  •	Speculative Decoding: Enhanced inference speed through architectural optimizations
  •	Multi-language Support: Comprehensive coverage for global competence assessment needs
  Primary Limitations:
  •	Scale Constraints: 8B parameters may limit performance on highly complex reasoning tasks compared to larger models
  •	Multimodal Gaps: Limited visual processing capabilities compared to Gemma 3's integrated vision encoder
  •	Context Window: Standard context limitations compared to extended 128K capabilities in other models
  •	Specialized Training: Enterprise focus may limit performance in certain academic or creative competency domains
  •	Inference Speed: While improved through speculative decoding, still slower than hybrid architectures like Nemotron-Nano

</details>
