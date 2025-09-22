# Python-Screening-Task-3
Python Screening Task 3: Evaluating Open Source Models for Student Competence Analysis


# Research Plan
## Google  
**LLM:** Gemma 2 (9B & 27B parameters; instruction-tuned; Apache 2.0)[1][2]
**NLP Framework:** TensorFlow (with high-level Keras APIs; supports tokenization, parsing, embeddings)[3]
**Educational Analytics:** Open Online Education “Course Builder” (open-source MOOC platform with deep learning–driven performance analytics)[4]

Approach: Identify models via GitHub and Hugging Face catalogs; evaluate architecture, license, community support, hardware requirements. Test by crafting Python code snippets for student solutions, prompt generation tasks, and measuring model outputs against expert-authored competence questions.  
Criteria: model performance on code understanding benchmarks, prompt relevance scores, inference speed, cost of deployment, interpretability via attention or saliency maps.  

Initial Thoughts:  
- Gemma 2’s instruction-tuned variants enable coherent prompt generation but may require fine-tuning on Python code corpora.  
- TensorFlow’s Keras pipelines offer seamless integration for tokenizing and embedding student submissions but need custom modules for code AST analysis.  
- Course Builder provides rich telemetry for student engagement but lacks prebuilt ML pipelines for competence inference; would need adapter layers.

## Meta  
**LLM:** Llama 3 (8B & 70B parameters; instruction-tuned; community license)[5][6]
**NLP Framework:** PyText (PyTorch-based; supports sequence tagging, semantic parsing, multitask training; production-grade)[7]
**Educational Analytics:** SphereAI in Blended OS (Llama 3.1-powered AI-school OS offering real-time feedback, automated grading, performance dashboards)[8]

Approach: Survey Meta AI releases and open-source repos; select latest Llama for code reasoning tasks; integrate with PyText pipelines to preprocess and analyze student text/code. Validate by comparing generated prompts to human-designed assessments.  
Criteria: adaptability to code-analysis tasks, context-window adequacy, community tooling for deployment, alignment with K-12 standards, licensing for educational use.  

Initial Thoughts:  
- Llama 3’s large context window supports multi-turn code review prompts but may struggle with code syntax without additional fine-tuning.  
- PyText excels at rapid prototyping of NLP pipelines but needs extension for AST extraction and logic error detection.  
- SphereAI demonstrates feasibility of end-to-end analytics in an educational setting but is tied to a proprietary platform; reusing its graph-powered modules could accelerate prototype development.

## Microsoft  
**LLM:** Phi-3.x / Phi-4 (3.8B–42B parameters; MoE architectures; long context up to 128K tokens; research license)[9][10]
**NLP Framework:** NLWeb (Model Context Protocol server; enables natural-language interfaces for websites; modular)[11]
**Educational Analytics:** Open Education Analytics (OEA) framework (Azure-based lakehouse & Power BI templates for at-risk prediction, personalized dashboards)[12][13]

Approach: Extract model specs from Azure AI Model Catalog; benchmark Phi-4 on code reasoning datasets (HumanEval, CodeXGLUE). Leverage NLWeb to build prompt-based interfaces over student code repositories. Use OEA’s data pipelines to gather student performance metrics.  
Criteria: benchmark scores on coding and reasoning tasks, inference cost on Azure GPUs/CPUs, ease of integrating NLWeb with custom datasets, OEA’s support for streaming analytics and privacy controls.  

Initial Thoughts:  
- Phi-4’s MoE setup boosts efficiency for complex reasoning but may introduce deployment complexity.  
- NLWeb simplifies building prompt UIs but requires customization for code-centric prompts.  
- OEA provides robust analytics infrastructure out of the box; coupling OEA data lakes with model outputs can yield comprehensive competence profiles.

---  
[1](https://huggingface.co/blog/gemma)
[2](https://www.instaclustr.com/education/open-source-ai/top-10-open-source-llms-for-2025/)
[3](https://opensource.google/projects/tensorflow)
[4](https://edu.google.com/intl/es-419/resources/more-educational-resources/)
[5](https://ai.meta.com/blog/meta-llama-3/)
[6](https://en.wikipedia.org/wiki/Llama_(language_model))
[7](https://engineering.fb.com/2018/12/14/ai-research/pytext-open-source-nlp-framework/)
[8](https://ai.meta.com/blog/blended-labs-ai-driven-schools-with-llama/)
[9](https://news.microsoft.com/source/features/ai/the-phi-3-small-language-models-with-big-potential/)
[10](https://blog.n8n.io/open-source-llm/)
[11](https://news.microsoft.com/source/features/company-news/introducing-nlweb-bringing-conversational-interfaces-directly-to-the-web/)
[12](https://github.com/OpenEducationAnalytics/OpenEducationAnalytics)
[13](https://azuremarketplace.microsoft.com/en-us/marketplace/consulting-services/antares_solutions.oea_national)
[14](https://docs.google.com/document/d/10huDVf8Ok-3v21vWzSAp9hCDTkAGQH9BpJA4_i1jZek/edit?tab=t.0)
[15](https://blog.google/technology/developers/gemma-open-models/)
[16](https://github.com/eugeneyan/open-llms)
[17](https://www.llama.com)
[18](https://www.youtube.com/watch?v=7ySqrQVLIF8)
[19](https://ai.meta.com/resources/models-and-libraries/)
[20](https://azure.microsoft.com/en-us/products/phi)
[21](https://cloud.google.com/ai/llms)
[22](https://about.fb.com/news/2024/07/open-source-ai-is-the-path-forward/)
[23](https://learn.microsoft.com/en-us/azure/machine-learning/prompt-flow/tools-reference/open-model-llm-tool?view=azureml-api-2)
[24](https://deepmind.google/models/)
[25](https://www.llama.com/llama-downloads/)
[26](https://microsoft.github.io/autogen/0.2/)
[27](https://github.com/google-deepmind/gemma)
[28](https://www.reddit.com/r/LocalLLaMA/comments/1cobwif/why_do_companies_like_meta_release_their_local/)
[29](https://www.nltk.org)
[30](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/natural-language-processing)
[31](https://rasa.community/open-source-nlu-nlp/)
[32](https://ai.meta.com/research/nlp/)
[33](https://github.com/microsoft/nlp-recipes)
[34](https://www.edenai.co/post/top-free-nlp-tools-apis-and-open-source-models)
[35](https://opensource.fb.com/projects/pytorch/)
[36](https://www.carmatec.com/blog/top-10-natural-language-processing-tools-and-platforms/)
[37](https://kairntech.com/blog/articles/top-10-nlp-tools-in-2025-a-complete-guide-for-developers-and-innovators/)
[38](https://meta-guide.com/natural-language/nlp/toolkits)
[39](https://learn.microsoft.com/en-us/azure/databricks/machine-learning/reference-solutions/natural-language-processing)
[40](https://opensource.com/article/19/3/natural-language-processing-tools)
[41](https://www.xenonstack.com/blog/nlp-tools)
[42](https://learn.microsoft.com/en-us/azure/ai-services/language-service/overview)
[43](https://cloud.google.com/natural-language)
[44](https://lumenalta.com/insights/9-of-the-best-natural-language-processing-tools-in-2025)
[45](https://www.edanalytics.org/open-source-and-non-commercial-solutions)
[46](https://www.frontiersin.org/journals/bioinformatics/articles/10.3389/fbinf.2024.1305969/full)
[47](https://www.edgraph.com/blog/2023/07/07/edgraph-named-oea-advanced-partner-by-microsoft)
[48](https://developers.google.com/analytics)
[49](https://ai.meta.com/resources/)
[50](https://pulse.microsoft.com/wp-content/uploads/2018/07/MicrosoftEducationAnalytics.pdf)
[51](https://opensource.fb.com)
[52](https://pulse.microsoft.com/en/sustainable-futures-en/education-en/fa1-develop-modern-data-intelligence-capabilities-with-open-education-analytics/)
[53](https://opensource.fb.com/projects/)
[54](https://opensource.microsoft.com)
[55](https://cloud.google.com/docs/data)
[56](https://metaflow.org)
[57](https://www.microsoft.com/en-us/research/blog/taskweaver-a-code-first-agent-framework-for-efficient-data-analytics-and-domain-adaptation/)
[58](https://cloud.google.com/blog/products/ai-machine-learning/open-source-framework-for-connecting-llms-to-your-data)
[59](https://www.metabase.com)
## Approach to identifying and evaluating relevant models

## How you would test or validate their applicability to the problem?

## Reasoning and decision-making process
.

<details>
  <summary> Q. What makes a model suitable for high-level competence analysis? </summary>
  .
</details>

<details>
  <summary> Q. How would you test whether a model generates meaningful prompts? </summary>
  .
</details>

<details>
  <summary> Q. What trade-offs might exist between accuracy, interpretability, and cost? </summary>
  .
</details>

<details>
  <summary> Q. Why did you choose the model you evaluated, and what are its strengths or limitations? </summary>
  .
</details>
