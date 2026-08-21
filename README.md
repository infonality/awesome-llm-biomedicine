# Awesome LLMs for Biomedicine [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) [![License: CC0 1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](LICENSE)

[![Biomedical AI research banner](assets/banner.png)](https://github.com/infonality/awesome-llm-biomedicine#readme)

Large language models, datasets, tools, benchmarks, and papers for biomedical and clinical applications.

I maintain this list from more than 15 years of work in the field, including experience organizing the n2c2/i2b2 shared tasks.

PRs welcome — [suggest a resource](https://github.com/infonality/awesome-llm-biomedicine/issues/new).

> **Educational resource.** This list supports research and engineering discovery. It is not medical advice, a clinical guideline, or a substitute for safety, privacy, regulatory, or licensing review.

---

## Contents

- [Scope & Selection](#scope--selection)
- [Clinical LLMs](#clinical-llms)
- [Vision-Language Models](#vision-language-models)
- [Genomics LLMs](#genomics-llms)
- [Drug Discovery & Molecular LLMs](#drug-discovery--molecular-llms)
- [Protein & Structural Biology Models](#protein--structural-biology-models)
- [Benchmarks & Datasets](#benchmarks--datasets)
- [Shared Tasks & Challenges](#shared-tasks--challenges)
- [LLM Agents & Toolkits](#llm-agents--toolkits)
- [Tools & Libraries](#tools--libraries)
- [Key Papers](#key-papers)
- [Ontologies & Knowledge Bases](#ontologies--knowledge-bases)
- [Courses & Tutorials](#courses--tutorials)
- [Glossary](#glossary)

---

## Scope & Selection

This list focuses on resources that apply language-modeling or foundation-model techniques to biomedicine, clinical practice, biomedical data, or life-science research.

I prioritize:

- Official project pages, papers, or model cards with enough documentation to evaluate a resource.
- Resources with a clear biomedical use case rather than general-purpose models with only a passing medical example.
- Benchmarks and datasets with documented provenance, access requirements, and intended tasks.

The list is curated, not ranked. Parameter counts, dataset sizes, availability, and maintenance status can change; treat them as approximate descriptors and verify the primary source before relying on a resource.

## Clinical LLMs

Language models trained or adapted for biomedical literature, clinical notes, medical dialogue, and clinical reasoning.

- [BioBERT](https://github.com/dmis-lab/biobert) - A 110M-parameter BERT model pretrained on PubMed abstracts and PMC full-text articles.
- [BioGPT](https://github.com/microsoft/BioGPT) - A 1.5B-parameter generative model pretrained on PubMed literature for biomedical text generation and mining.
- [BioMedLM (PubMedGPT)](https://huggingface.co/stanford-crfm/BioMedLM) - 2.7B params. Stanford CRFM; domain-specific model trained from scratch.
- [BioMistral](https://huggingface.co/BioMistral/BioMistral-7B) - A 7B-parameter Mistral model adapted to biomedical text from PubMed Central.
- [ClinicalBERT](https://huggingface.co/emilyalsentzer/Bio_ClinicalBERT) - A 110M-parameter BERT model adapted to clinical notes from MIMIC-III discharge summaries.
- [ClinicalLongformer](https://huggingface.co/yikuan8/Clinical-Longformer) - A long-context clinical language model with a 4K-token context window for full-note processing.
- [GatorTron](https://arxiv.org/abs/2203.03560) - Clinical language models from UF Health, trained on up to 90B tokens of clinical and biomedical text, with 3.9B and 8.9B parameter variants.
- [HuatuoGPT](https://github.com/FreedomIntelligence/HuatuoGPT) - Chinese medical language models fine-tuned on physician dialogues, available in 7B, 13B, and 33B variants.
- [HuatuoGPT-II](https://github.com/FreedomIntelligence/HuatuoGPT-II) - 7B/13B/34B params. One-stage medical adaptation for Chinese medical dialogue.
- [Med-PaLM 2](https://arxiv.org/abs/2305.09617) - Google's medical language model; it is not open-weight and was evaluated on USMLE-style tasks.
- [MedGemma](https://github.com/google-health/medgemma) - Collection of Gemma 3 variants for medical text and image comprehension: a 4B multimodal model and a 27B text-only model.
- [MediPhi](https://huggingface.co/collections/microsoft/mediphi) - Collection of 3.8B-parameter Phi-3.5-based models adapted to medical and clinical NLP tasks.
- [MEDITRON](https://huggingface.co/epfl-llm/meditron-7b) - 7B/70B params. Medical papers + guidelines. EPFL open-weight models for medical language tasks.
- [MMedLM 2](https://github.com/MAGIC-AI4Med/MMedLM) - Multilingual medical LLM supporting 8 languages and trained on a multilingual medical corpus.
- [OpenBioLLM](https://huggingface.co/aaditya/OpenBioLLM-Llama3-8B) - Llama 3 adaptations for biomedical text, available in 8B and 70B variants.
- [PMC-LLaMA](https://huggingface.co/axiong/PMC_LLaMA_13B) - LLaMA models fine-tuned on PubMed Central articles, available in 7B and 13B variants.
- [PubMedBERT (BiomedBERT)](https://huggingface.co/microsoft/BiomedNLP-BiomedBERT-base-uncased-abstract-fulltext) - A 110M-parameter BERT model pretrained from scratch on PubMed abstracts and PMC full-text articles.

## Vision-Language Models

Multimodal models for biomedical imaging, radiology, pathology, and medical visual question answering.

- [BiomedCLIP](https://huggingface.co/microsoft/BiomedCLIP-PubMedBERT_256-vit_base_patch16_224) - Biomedical vision-language foundation model pretrained on PMC-15M image-text pairs.
- [BiomedGPT](https://github.com/taokz/BiomedGPT) - Generalist vision-language foundation model for diverse biomedical tasks. Nature Medicine 2024.
- [BiomedParse](https://github.com/microsoft/BiomedParse) - Biomedical foundation model for joint segmentation, detection, and recognition across nine imaging modalities.
- [HuatuoGPT-Vision](https://github.com/FreedomIntelligence/HuatuoGPT-Vision) - Medical multimodal LLM that injects visual knowledge at scale; 7B/34B models.
- [LLaVA-Med](https://github.com/microsoft/LLaVA-Med) - Biomedical vision-language assistant trained on PMC-15M with curriculum learning for medical VQA.

## Genomics LLMs

Foundation models for single-cell RNA sequencing, DNA sequences, and genomics.

- [AlphaGenome](https://github.com/google-deepmind/alphagenome_research) - 1 Mb context. DNA sequence-to-function model for regulatory variant effects across gene expression, splicing, chromatin, and 3D contacts; Apache-2.0 research code and weights subject to non-commercial model terms.
- [Caduceus](https://github.com/kuleshov-group/caduceus) - DNA sequences. Reversible and bidirectional DNA sequence modeling.
- [DNABERT-2](https://github.com/MAGICS-LAB/DNABERT_2) - 117M params. DNA sequences. Improved genome-understanding model.
- [Evo 2](https://github.com/arcinstitute/evo2) - 1B–40B params. DNA sequences. Long-context language model for genome modeling and design at single-nucleotide resolution up to 1M base pairs.
- [Geneformer](https://huggingface.co/ctheodoris/geneformer) - 95M params. scRNA-seq. Foundation model pretrained on 30M cells for network-biology tasks.
- [HyenaDNA](https://github.com/HazyResearch/hyena-dna) - 1K–1M context. DNA sequences. Ultra-long-context genomic model.
- [Nucleotide Transformer](https://huggingface.co/InstaDeepAI/nucleotide-transformer-2.5b-multi-species) - 500M–2.5B params. DNA sequences. Multi-species DNA foundation model.
- [scGPT](https://github.com/bowang-lab/scGPT) - ~50M params. scRNA-seq. Single-cell foundation model for cell-type annotation and perturbation prediction.
- [scBERT](https://github.com/TencentAILabHealthcare/scBERT) - Single-cell type annotation using BERT-style pretraining.
- [UmiFormer](https://arxiv.org/abs/2305.02110) - Transformer for single-cell RNA-seq cell-type annotation.

## Drug Discovery & Molecular LLMs

Models for molecular property prediction, biomolecular interactions, drug–drug interaction, retrosynthesis, and chemical generation.

- [Boltz-2](https://github.com/jwohlwend/boltz) - Biomolecular foundation model that jointly predicts complex structures and binding affinities; MIT-licensed code and weights.
- [ChemBERTa](https://huggingface.co/seyonec/ChemBERTa-zinc-base-v1) - SMILES molecules. RoBERTa for molecular property prediction.
- [Chemformer](https://github.com/MolecularAI/Chemformer) - SMILES to reactions. Transformer for retrosynthesis.
- [MolT5](https://github.com/blender-nlp/MolT5) - Molecule to text. T5 model for molecule captioning and generation.
- [MolReGPT](https://arxiv.org/abs/2310.17341) - LLM-based molecular generation through prompt engineering with SMILES.
- [TxGemma](https://developers.google.com/health-ai-developer-foundations/txgemma/model-card) - 2B, 9B, and 27B language models fine-tuned for therapeutic tasks across small molecules, proteins, nucleic acids, diseases, and cell lines; Health AI Developer Foundations terms apply.
- [Uni-Mol](https://github.com/dptech-corp/Uni-Mol) - 3D molecular representation model for drug-discovery tasks.

## Protein & Structural Biology Models

Protein sequence, structure, and design models. This section includes important foundation models that are not strictly language models.

- [ESM-2](https://github.com/facebookresearch/esm) - 650M–15B params. Protein sequences. Meta's protein language model family.
- [ESM3](https://www.evolutionaryscale.ai/blog/esm3-release) - Protein language model from EvolutionaryScale for generative protein design.
- [LucaOne](https://github.com/LucaOne/LucaOne) - Unified nucleic-acid and protein foundation model with code and checkpoints for sequence embeddings, classification, regression, and residue-level tasks.
- [ProGen2](https://github.com/salesforce/progen/tree/main/progen2) - 151M–6.4B params. Protein sequences. Generative protein-design models.
- [ProtTrans](https://huggingface.co/Rostlab/prot_bert_bfd) - 420M–3B params. Protein sequences. Transformer models for protein representation learning.
- [RoseTTAFold](https://github.com/RosettaCommons/RoseTTAFold) - Protein structure. 3D protein-structure prediction; non-LLM but essential context.
- [SaProt](https://github.com/westlake-repl/SaProt) - 650M params. Protein structure. Structure-aware protein model.

## Benchmarks & Datasets

### Clinical Text

- [AMEGA-LLM](https://github.com/DATEXIS/AMEGA-benchmark) - Guideline adherence. Open-ended clinical benchmark across 24 diagnostic scenarios in 13 specialties with physician-designed rubrics.
- [BioASQ](https://bioasq.org/) - Biomedical question answering and retrieval benchmark; includes expert-annotated questions.
- [BlueBERT benchmark suite](https://github.com/ncbi-nlp/BlueBERT) - Multiple tasks. NCBI benchmark suite for biomedical language understanding.
- [BRIDGE](https://github.com/YLab-Open/BRIDGE) - Clinical text. Multilingual benchmark with 87 real-world tasks across nine languages and a continuously updated leaderboard.
- [HealthBench](https://openai.com/index/healthbench/) - Health conversations. 5,000 realistic multi-turn conversations graded with physician-created rubrics from 262 physicians across 60 countries.
- [LLMEval-Med](https://github.com/llmeval/LLMEval-Med) - Clinical evaluation. EMNLP 2025 benchmark of 2,996 questions from EHRs and expert-designed scenarios with physician-validated scoring.
- [MedNLI](https://github.com/jgc128/mednli) - Natural language inference in clinical text. Clinical-premise/hypothesis benchmark.
- [MedQA (USMLE)](https://github.com/jind11/MedQA) - QA. 12.7K questions. US medical licensing exam questions.
- [MedMCQA](https://github.com/MedMCQA/MedMCQA) - QA. 194K questions. Indian medical entrance exam MCQs.
- [MedXpertQA](https://github.com/TsinghuaC3I/MedXpertQA) - QA. 4,460 questions. Expert-level medical reasoning benchmark. ICML 2025. Text and multimodal subsets.
- [MIMIC-III / MIMIC-IV](https://physionet.org/content/mimiciv/) - Clinical notes and structured data. Credentialed access and training are required.
- [MMLU (medical subsets)](https://github.com/hendrycks/test) - MCQ. Medical subject subsets for broad knowledge evaluation.
- [PubMedQA](https://github.com/pubmedqa/pubmedqa) - QA. Expert-labeled and unlabeled questions over PubMed abstracts.

### Relation Extraction & Drug Interactions

- [ADE Corpus](https://jbiomedsem.biomedcentral.com/articles/10.1186/2041-1480-3-15) - Adverse drug events. 3,000+ annotated case-report sentences.
- [ChemProt](https://github.com/ncbi-nlp/BLUE_Benchmark) - Chemical–protein relation extraction benchmark from BioCreative VI, with 1,820 PubMed abstracts.
- [DDI Corpus](https://github.com/yardstick17/DDIExtraction) - Drug–drug interaction extraction. 792 documents.
- [EU-ADR](https://github.com/mi-erasmusmc/EU-ADR-Corpus) - Drug–adverse-effect relations. 3,000 sentences.
- [GAD (Genetic Association Database)](https://academic.oup.com/bioinformatics/article/25/18/2486/194116) - Gene–disease association extraction. 5,330+ sentences.

### Genomics

- [CellxGene](https://cellxgene.cziscience.com/) - Single-cell data census and exploration platform from the Chan Zuckerberg Initiative.
- [GEO](https://www.ncbi.nlm.nih.gov/geo/) - Public archive of gene-expression data and functional genomics studies.
- [Tabula Sapiens](https://github.com/czbiohub-sf/tabula-sapiens) - Multi-organ human single-cell atlas.

### Agent Benchmarks

- [ASCENT](https://proceedings.mlr.press/v333/choi26a.html) - Diagnostic reasoning. Clinician-annotated benchmark of 3,078 stepwise problems derived from MedQA-USMLE.
- [DrugDiscoveryBench](https://github.com/scaleapi/DrugDiscoveryBench) - Drug-discovery agents. Open task and image data for computational drug-discovery workflows; reference rubrics require gated Hugging Face access.
- [FHIR-AgentBench](https://github.com/glee4810/FHIR-AgentBench) - EHR agents. 2,931 clinical questions grounded in HL7 FHIR with released data and evaluation code; MIMIC-IV FHIR data and cloud setup are required.
- [MedAgentBench](https://stanfordmlgroup.github.io/projects/medagentbench) - Agent evaluation. 300 physician-written tasks across 10 categories in a FHIR-compliant EHR environment.
- [RadLE 2.0](https://crashlab.in/radle-technicalreport) - Radiology agents. Uncertainty-aware benchmark for single-image diagnosis that scores confidence, safety, accuracy, and handover readiness.

## Shared Tasks & Challenges

- [BioASQ Challenge](https://bioasq.org/participate/challenges) - Biomedical question answering and retrieval challenge.
- [BioNLP Shared Task](https://aclanthology.org/venues/bionlp/) - Event extraction from biomedical text. 2009–2026.
- [MedReason Challenge 2026](https://medreason26.github.io/) - Medical multimodal reasoning. MICCAI challenge evaluating visual question answering under low-dose X-ray, 7T MRI, and other domain shifts.
- [MEDIQA](https://github.com/abachaa/MEDIQA2019) - Medical text generation and summarization. 2019.
- [n2c2 / i2b2 challenges](https://portal.dbmi.hms.harvard.edu/projects/n2c2-nlp/) - Clinical NLP challenges and datasets dating back to 2006; access terms vary by release.
- [TAC ADR Extraction](https://tac.nist.gov/) - Adverse-drug-reaction extraction from drug labels. 2017. NIST TAC archive.

## LLM Agents & Toolkits

LLM-based agents and systems for clinical reasoning, therapeutic decision-making, and medical research.

- [Biomni](https://github.com/snap-stanford/Biomni) - Biomedical research agent combining LLM planning, retrieval-augmented execution, and code tools across life-science tasks; sandbox generated code and review integrated-tool licenses.
- [TxAgent](https://github.com/mims-harvard/TxAgent) - Agent for therapeutic reasoning with access to a large biomedical tool universe; Harvard.

## Tools & Libraries

- [BERN2](https://github.com/dmis-lab/bern) - Biomedical NER. Multi-type entity recognition for diseases, drugs, genes, and other entities.
- [BigBio](https://github.com/bigscience-workshop/biomedical) - Dataset loading. Unified access to 160+ biomedical datasets.
- [BioC](https://pypi.org/project/bioc/) - Biomedical text format. XML/JSON interchange format for biomedical text.
- [cTAKES](https://ctakes.apache.org/) - Clinical NLP. Clinical Text Analysis Knowledge Extraction System.
- [MedSpaCy](https://github.com/medspacy/medspacy) - Clinical NLP pipeline with section detection and rule-based processing.
- [scispaCy](https://github.com/allenai/scispacy) - Biomedical NLP pipeline with models for NER and entity linking.

## Key Papers

### Clinical LLMs

- BioBERT: Lee et al. (2020). BioBERT: a pre-trained biomedical language representation model for biomedical text mining. [arXiv:1901.08746](https://arxiv.org/abs/1901.08746)
- BioGPT: Luo et al. (2022). BioGPT: generative pre-trained transformer for biomedical text generation and mining. [arXiv:2210.17100](https://arxiv.org/abs/2210.17100)
- ClinicalBERT: Alsentzer et al. (2019). Publicly Available Clinical BERT Embeddings. [arXiv:1904.03323](https://arxiv.org/abs/1904.03323)
- HuatuoGPT: Zhang et al. (2023). HuatuoGPT, towards Taming Language Model to Be a Doctor. [arXiv:2305.15075](https://arxiv.org/abs/2305.15075)
- Med-PaLM: Singhal et al. (2023). Large language models encode clinical knowledge. [arXiv:2212.13138](https://arxiv.org/abs/2212.13138)
- MedGemma: Golden et al. (2025). MedGemma: Open Weight Medical LLMs. [arXiv:2507.05201](https://arxiv.org/abs/2507.05201)
- MediPhi: Corbeil et al. (2025). A Modular Approach for Clinical SLMs Driven by Synthetic Data with Pre-Instruction Tuning, Model Merging, and Clinical-Tasks Alignment. [ACL 2025](https://aclanthology.org/2025.acl-long.950/)
- MEDITRON: Chen et al. (2023). MEDITRON-70B: Scaling Medical Pretraining of Language Models. [arXiv:2311.18279](https://arxiv.org/abs/2311.18279)
- MMedLM: Qiu et al. (2024). Towards Building Multilingual Language Model for Medicine. [Nature Communications](https://www.nature.com/articles/s41467-024-52417-z)
- OpenBioLLM: Rahman et al. (2024). OpenBioLLM: Leveraging Open Access Data to Build Specialized Medical LLMs. [arXiv:2405.17364](https://arxiv.org/abs/2405.17364)
- PubMedBERT: Gu et al. (2021). Domain-Specific Language Model Pretraining for Biomedical Natural Language Processing. [arXiv:2007.15779](https://arxiv.org/abs/2007.15779)

### Vision-Language Models

- BiomedCLIP: Zhang et al. (2024). Large-Scale Domain-Specific Pretraining for Biomedical Vision-Language Processing. [arXiv:2303.00915](https://arxiv.org/abs/2303.00915)
- BiomedGPT: Zhang et al. (2024). A generalist vision-language foundation model for diverse biomedical tasks. [Nature Medicine](https://www.nature.com/articles/s41591-024-03185-2)
- BiomedParse: Zhao et al. (2025). A foundation model for joint segmentation, detection and recognition of biomedical objects across nine modalities. [Nature Methods](https://www.nature.com/articles/s41592-024-02499-w)
- LLaVA-Med: Li et al. (2023). LLaVA-Med: Training a Large Language-and-Vision Assistant for Biomedicine in One Day. [arXiv:2306.00890](https://arxiv.org/abs/2306.00890)

### Genomics LLMs

- Geneformer: Theodoris et al. (2023). Transfer learning enables predictions in network biology. [Nature](https://www.nature.com/articles/s41586-023-06139-9)
- Nucleotide Transformer: Dalla-Torre et al. (2024). The Nucleotide Transformer: Building and Evaluating Robust Foundation Models for Human Genomics. [Nature Methods](https://www.nature.com/articles/s41592-024-02523-z)
- scGPT: Cui et al. (2024). scGPT: Toward Building a Foundation Model for Single-Cell Multi-omics Using Single-Cell Transcriptomics. [Nature Methods](https://www.nature.com/articles/s41592-024-02201-0)
- AlphaGenome: Avsec et al. (2026). Advancing regulatory variant effect prediction with AlphaGenome. [Nature](https://www.nature.com/articles/s41586-025-10014-0)
- Evo 2: Brixi et al. (2026). Genome modeling and design across all domains of life with Evo 2. [Nature](https://doi.org/10.1038/s41586-026-10176-5)

### Protein & Structural Biology

- LucaOne: He et al. (2025). Generalized biological foundation model with unified nucleic acid and protein language. [Nature Machine Intelligence](https://doi.org/10.1038/s42256-025-01044-4)

### Drug Discovery

- Boltz-2: Passaro et al. (2025). Boltz-2: Towards Accurate and Efficient Binding Affinity Prediction. [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC12262699/)
- ChemBERTa: Chithrananda et al. (2020). ChemBERTa: Large-Scale Self-Supervised Pretraining for Molecular Property Prediction. [arXiv:2010.09885](https://arxiv.org/abs/2010.09885)
- MolT5: Edwards et al. (2022). Translation between Molecules and Natural Language. [arXiv:2204.11817](https://arxiv.org/abs/2204.11817)
- TxGemma: Wang et al. (2025). TxGemma: Efficient and Agentic LLMs for Therapeutics. [arXiv:2504.06196](https://arxiv.org/abs/2504.06196)

### Evaluation & Safety

- Clinical safety evaluation: Omiye et al. (2023). Large language models propagate race-based medicine. [npj Digital Medicine](https://www.nature.com/articles/s41746-023-00939-z)
- AMEGA-LLM: Fast et al. (2024). Autonomous Medical Evaluation for Guideline Adherence of Large Language Models. [npj Digital Medicine](https://www.nature.com/articles/s41746-024-01356-6)
- BRIDGE: Wu et al. (2026). BRIDGE: Benchmarking Large Language Models for Understanding Real-world Clinical Practice Text. [arXiv:2504.19467](https://arxiv.org/abs/2504.19467)
- HealthBench: Arora et al. (2025). HealthBench: Evaluating Large Language Models Towards Improved Human Health. [arXiv:2505.08775](https://arxiv.org/abs/2505.08775)
- MedFailBench: Ozkan (2026). MedFailBench: A Clinician-Built Open-Source Benchmark for Medical AI Safety Boundary Inspection. [arXiv:2607.15166](https://arxiv.org/abs/2607.15166)
- Med-HALT: Pal et al. (2024). Med-HALT: Medical Domain Hallucination Test for Large Language Models. [arXiv:2307.15389](https://arxiv.org/abs/2307.15389)
- MedXpertQA: Zuo et al. (2025). MedXpertQA: Benchmarking Expert-Level Medical Reasoning and Understanding. [arXiv:2501.18362](https://arxiv.org/abs/2501.18362)

### LLM Agents

- ASCENT: Choi et al. (2026). ASCENT: A Benchmark for Evaluating and Advancing Stepwise Diagnostic Reasoning in Large Language Models on Common Clinical Scenarios. [Open PDF](https://raw.githubusercontent.com/mlresearch/v333/main/assets/choi26a/choi26a.pdf)
- FHIR-AgentBench: Lee et al. (2025). FHIR-AgentBench: Benchmarking LLM Agents for Realistic Interoperable EHR Question Answering. [arXiv:2509.19319](https://arxiv.org/abs/2509.19319)
- TxAgent: Gao et al. (2025). TxAgent: An AI Agent for Therapeutic Reasoning Across a Universe of Tools. [arXiv:2503.10970](https://arxiv.org/abs/2503.10970)

## Ontologies & Knowledge Bases

Essential resources for biomedical NLP, retrieval, and clinical data work. Access terms vary; check each provider's license before downloading or redistributing data.

- [ChEMBL](https://www.ebi.ac.uk/chembl/) - Bioactive molecules. Drug discovery and molecular properties.
- [ClinicalTrials.gov](https://clinicaltrials.gov/) - Clinical trials. Trial data and drug-development pipeline.
- [CTD (Comparative Toxicogenomics Database)](https://ctdbase.org/) - Gene–disease–chemical interactions. Curated toxicology and pharmacology database.
- [DrugBank](https://go.drugbank.com/) - Drug data. Drug interactions and pharmacology; access terms apply.
- [ICD-10/11](https://icd.who.int/) - Disease classification. Diagnosis coding and clinical NER.
- [LOINC](https://loinc.org/) - Lab observations. Lab-test naming and clinical-data standardization.
- [MedDRA](https://www.meddra.org/) - Adverse drug reactions. Pharmacovigilance and ADR coding; updated twice yearly.
- [PubMed](https://pubmed.ncbi.nlm.nih.gov/) - Biomedical literature. Primary literature search and citation database.
- [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/) - Drug nomenclature. Drug normalization and prescription matching.
- [SNOMED CT](https://www.snomed.org/) - Clinical terminology. Clinical notes and EHR coding.
- [UMLS](https://www.nlm.nih.gov/research/umls/) - Unified Medical Language System. Biomedical concept mapping; requires a free research license.

## Courses & Tutorials

- [AMIA Informatics Summit tutorials](https://amia.org/) - Clinical NLP and AI in healthcare.
- [BioNLP workshop tutorials (ACL)](https://aclanthology.org/2023.bionlp-1/) - Biomedical NLP methods.
- [DeepLearning.AI Drug Discovery](https://www.deeplearning.ai/) - AI for drug discovery.
- [Stanford BMDS 215](https://bulletin.stanford.edu/courses/2122201) - Data science for medicine.
- [Stanford CS25 Transformers](https://web.stanford.edu/class/cs25/) - LLM foundations.

## Glossary

Some terms that appear throughout the list.

- ADR: Adverse drug reaction.
- CITI training: Required ethics training for accessing some clinical datasets and research environments.
- EHR: Electronic health record; a patient's digital medical record.
- FDA label: Official prescribing information approved by the US FDA.
- FHIR: Fast Healthcare Interoperability Resources; a standard for exchanging health information.
- HIPAA: Health Insurance Portability and Accountability Act; the US health privacy law.
- MIMIC: Medical Information Mart for Intensive Care; a critical care database.
- NER: Named entity recognition; identifying medical entities in text.
- Pharmacovigilance: Detection and prevention of adverse drug effects.
- RAG: Retrieval augmented generation; generating responses using retrieved external context.
- RE: Relation extraction; finding relationships between entities such as drug and disease links.
- scRNA-seq: Single-cell RNA sequencing; measuring gene expression at individual cell resolution.
- SMILES: Simplified Molecular Input Line Entry System; a text representation of molecules.
- USMLE: United States Medical Licensing Examination; a benchmark used in some medical model evaluations.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the contribution guide. Suggest additions through [issues](https://github.com/infonality/awesome-llm-biomedicine/issues) or submit a pull request.
