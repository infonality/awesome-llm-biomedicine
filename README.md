# Awesome LLM for Biomedicine

A curated list of large language models, datasets, tools, and benchmarks for biomedical and clinical applications — covering clinical text understanding, drug discovery, genomics, protein science, and healthcare AI.

Maintained by [@infonality](https://github.com/infonality) · PRs welcome · [Suggest a resource](https://github.com/infonality/awesome-llm-biomedicine/issues/new)

---

## Clinical LLMs

Pre-trained models fine-tuned on clinical notes, EHR data, and medical literature.

| Model | Params | Pre-training data | Link | Notes |
|---|---|---|---|---|
| ClinicalBERT | 110M | MIMIC-III discharge summaries | [HF](https://huggingface.co/emilyalsentzer/Bio_ClinicalBERT) | BERT fine-tuned on clinical notes |
| PubMedBERT | 110M | PubMed abstracts (from scratch) | [HF](https://huggingface.co/microsoft/PubMedBERT) | Pre-trained from scratch on PubMed — strong baseline for biomedical NLP |
| BioBERT | 110M | PubMed + PMC | [HF](https://huggingface.co/dmis-lab/biobert-base-cased-v1.2) | Early biomedical BERT; widely cited |
| ClinicalLongformer | 4K ctx | Clinical notes | [HF](https://huggingface.co/yikao810/ClinicalLongformer) | Long-context clinical model for full notes |
| BioGPT | 1.5B | PubMed + papers | [GitHub](https://github.com/microsoft/BioGPT) | Microsoft's generative model for biomedical text generation and mining |
| GatorTron | 3.9B/8.9B | 90B tokens (clinical + PubMed) | [Paper](https://arxiv.org/abs/2203.03560) | Large clinical model from UF Health |
| Med-PaLM 2 | — | Google's medical LLM | [Paper](https://arxiv.org/abs/2305.09617) | Achieves USMLE-level performance; not open-weight |
| PMC-LLaMA | 7B/13B | PubMed Central | [HF](https://huggingface.co/axiong/PMC_LLaMA_13B) | LLaMA fine-tuned on biomedical literature |
| BioMistral | 7B | PubMed Central | [HF](https://huggingface.co/BioMistral/BioMistral-7B) | Mistral-based open biomedical LLM |
| MEDITRON-7B/70B | 7B/70B | Medical papers + guidelines | [HF](https://huggingface.co/epfl-llm/meditron-7b) | EPFL; open-weight, clinical reasoning |
| Clinical-Camel | 7B/13B/70B | Clinical text | [GitHub](https://github.com/epfLLM/meditron) | Clinical domain adaptation of LLaMA-2 |
| BioMedLM (PubMedGPT) | 2.7B | PubMed | [HF](https://huggingface.co/stanford-crfm/BioMedLM) | Stanford CRFM; domain-specific from scratch |

## Genomics LLMs

Foundation models for single-cell RNA-seq, DNA sequences, and genomics.

| Model | Params | Domain | Link | Notes |
|---|---|---|---|---|
| Geneformer | 95M | scRNA-seq | [GitHub](https://github.com/jxmorisette/geneformer) | Foundation model for transcriptomics; pre-trained on 30M cells |
| scGPT | ~50M | scRNA-seq | [GitHub](https://github.com/bowang-lab/scGPT) | Single-cell foundation model; cell type annotation, perturbation prediction |
| Nucleotide Transformer | 500M–2.5B | DNA sequences | [HF](https://huggingface.co/InstaDeepAI/nucleotide-transformer-2.5b-multi-species) | Multi-species DNA foundation model |
| DNABERT-2 | 117M | DNA sequences | [GitHub](https://github.com/MAGICS-LAB/DNABERT_2) | Improved genome understanding model |
| HyenaDNA | 1k–1M ctx | DNA sequences | [GitHub](https://github.com/HazyResearch/hyena-dna) | Ultra-long-context genomic model |
| Caduceus | — | DNA | [GitHub](https://github.com/klab-lab/caduceus) | Reversible and bi-directional DNA sequence modeling |

## Drug Discovery & Molecular LLMs

Models for molecular property prediction, drug-drug interaction, and chemical generation.

| Model | Domain | Link | Notes |
|---|---|---|---|
| ChemBERTa | SMILES molecules | [HF](https://huggingface.co/seyonec/ChemBERTa-zinc-base-v1) | RoBERTa for molecular property prediction |
| MolT5 | Molecule ↔ text | [GitHub](https://github.com/blender-lab/MolT5) | T5 for molecule captioning and generation |
| Chemformer | SMILES → reactions | [GitHub](https://github.com/MolecularAI/Chemformer) | Transformer for retrosynthesis |
| Uni-Mol | 3D molecular | [GitHub](https://github.com/dptech-corp/Uni-Mol) | 3D molecular representation model |
| Galactica | Scientific text + molecules | [HF](https://huggingface.co/facebook/galactica-120b) | Meta's science LLM (deprecated but influential) |
| SmolLM-Chem | Small molecular | [HF](https://huggingface.co/ltg/ordeen-wissenschaftler-1b) | Lightweight chemical language model |

## Protein & Structural Biology LLMs

| Model | Params | Domain | Link | Notes |
|---|---|---|---|---|
| ESM-2 | 650M–15B | Protein sequences | [GitHub](https://github.com/facebookresearch/esm) | Meta's protein language model; structure prediction |
| ProtTrans | 420M–3B | Protein sequences | [HF](https://huggingface.co/Rostlab/prot_bert_bfd) | Transformer for protein sequences |
| ProGen2 | 6.4B–151B | Protein sequences | [GitHub](https://github.com/salesforce/progen2) | Generative protein design model |
| SaProt | 650M | Protein (folded) | [HF](https://huggingface.co/westlake-repl/SaProt-650M) | Structure-aware protein model |
| RoseTTAFold | — | Protein structure | [GitHub](https://github.com/RosettaCommons/RoseTTAFold) | 3D protein structure prediction (non-LLM but essential) |

## Benchmarks & Datasets

### Clinical Text

| Dataset | Task | Size | Link | Notes |
|---|---|---|---|---|
| i2b2/n2c2 | NER, RE, coreference | ~1,000 notes each year | [DBMI](https://portal.dbmi.hms.harvard.edu/projects/n2c2-2024/) | Historical shared tasks; clinical notes |
| MIMIC-III / MIMIC-IV | Clinical notes, tables | 2M+ notes | [PhysioNet](https://physionet.org/content/mimiciv/) | Most-used clinical text corpus; requires training + CITI |
| BioASQ | QA, retrieval | ~5K questions | [bioasq.org](http://bioasq.org/) | Biomedical question answering benchmark |
| PubMedQA | QA | 1K expert + 211K unlabeled | [GitHub](https://github.com/pubmedqa/pubmedqa) | QA over PubMed abstracts |
| MedQA (USMLE) | QA | 12.7K questions | [GitHub](https://github.com/jind11/MedQA) | US medical licensing exam questions |
| MMLU (medical subsets) | MCQ | 1K+ per subject | [GitHub](https://github.com/hendrycks/test) | Clinical knowledge evaluation; widely used in LLM benchmarks |
| BlueBERT | Multiple | — | [GitHub](https://github.com/ncbi-nlp/BlueBERT) | NCBI's benchmark suite for biomedical language understanding |

### Relation Extraction & Drug Interactions

| Dataset | Task | Size | Link |
|---|---|---|---|
| ChemProt | Chemical–protein RE | 1,820 abstracts | [GitHub](https://github.com/arwhirang/recursive_chemprot) |
| DDI (DrugBank) | Drug–drug interaction | 792 documents | [GitHub](https://github.com/ncbi-nlp/DDIExtraction2013) |
| EU-ADR | Drug–adverse effect | 3,000 sentences | [GitHub](https://github.com/madmanc/EU-ADR-corpus) |
| GAD | Gene–disease association | 5,330 sentences | [GitHub](https://github.com/dmis-lab/biobert) |
| ADE Corpus | Adverse drug events | 3,000+ sentences | [GitHub](https://github.com/dmis-lab/ade-corpus) |

### Genomics

| Dataset | Task | Size | Link |
|---|---|---|---|
| CellxGene | scRNA-seq census | 50M+ cells | [cellxgene.cziscience.com](https://cellxgene.cziscience.com/) | Chan Zuckerberg Initiative; largest single-cell atlas |
| GEO | Gene expression | 20M+ samples | [ncbi.nlm.nih.gov/geo](https://www.ncbi.nlm.nih.gov/geo/) | Gene Expression Omnibus |
| Tabula Sapiens | scRNA-seq | 500K+ cells | [tabula-sapiens.ds.czbiohub.org](https://tabula-sapiens.ds.czbiohub.org/) | Multi-organ human cell atlas |

## Shared Tasks & Challenges

| Event | Focus | Year(s) | Link |
|---|---|---|---|
| BioNLP Shared Task | Event extraction from biomedical text | 2009–2023 | [GitHub](https://github.com/openbiomedicalnlp/bionlp-st) |
| n2c2 / i2b2 | Clinical NLP challenges | 2007–present | [DBMI Harvard](https://portal.dbmi.hms.harvard.edu/projects/n2c2-2024/) |
| TAC ADR Extraction | ADR extraction from drug labels | 2017 | [NIST](https://tac.nist.gov/2017/ADRF/) |
| BioASQ Challenge | Biomedical QA & retrieval | 2013–present | [bioasq.org](http://bioasq.org/) |
| MEDIQA | Medical text generation & summarization | 2019–2024 | [GitHub](https://github.com/abachaa/MEDIQA) |
| MedNLI | Natural language inference in clinical text | 2018 | [GitHub](https://github.com/jgc128/mednli) |

## Tools & Libraries

| Tool | Purpose | Link | Notes |
|---|---|---|---|
| scispaCy | Biomedical NLP pipeline | [GitHub](https://github.com/allenai/scispacy) | spaCy models for biomedical NER, linking |
| MedSpaCy | Clinical NLP pipeline | [GitHub](https://github.com/medspacy/medspacy) | Clinical text processing, section detection |
| BERN2 | Biomedical NER | [GitHub](https://github.com/dl4ds/bernal) | Multi-type entity recognition (disease, drug, gene, etc.) |
| BioC | Biomedical text format | [GitHub](https://github.com/biocreative/bioc) | XML/JSON interchange format for biomedical text |
| cTAKES | Clinical NLP | [Apache](https://ctakes.apache.org/) | Clinical Text Analysis Knowledge Extraction System |
| BioGPT inference | Text generation | [GitHub](https://github.com/microsoft/BioGPT) | Microsoft's biomedical generative model |
| BigBIO | Dataset loading | [GitHub](https://github.com/bigscience-workshop/biomedical) | Unified access to 160+ biomedical datasets |

## Key Papers

### Clinical LLMs
- **BioBERT**: Lee et al. (2020). *BioBERT: a pre-trained biomedical language representation model for biomedical text mining.* [arXiv:1901.08746](https://arxiv.org/abs/1901.08746)
- **PubMedBERT**: Gu et al. (2021). *Domain-Specific Language Model Pretraining for Biomedical Natural Language Processing.* [arXiv:2007.15779](https://arxiv.org/abs/2007.15779)
- **BioGPT**: Luo et al. (2022). *BioGPT: generative pre-trained transformer for biomedical text generation and mining.* [arXiv:2210.17100](https://arxiv.org/abs/2210.17100)
- **Med-PaLM**: Singhal et al. (2023). *Large language models encode clinical knowledge.* [arXiv:2212.13138](https://arxiv.org/abs/2212.13138)
- **MEDITRON**: Chen et al. (2023). *MEDITRON-70B: Scaling Medical Pretraining of Language Models.* [arXiv:2311.18279](https://arxiv.org/abs/2311.18279)

### Genomics LLMs
- **Geneformer**: Theodoris et al. (2023). *Transfer learning enables predictions in network biology.* [Nature](https://www.nature.com/articles/s41586-023-06139-9)
- **scGPT**: Cui et al. (2024). *scGPT: Toward Building a Foundation Model for Single-Cell Multi-omics Using Single-Cell Transcriptomics.* [Nature Methods](https://www.nature.com/articles/s41592-024-02205-7)
- **Nucleotide Transformer**: Dalla-Torre et al. (2024). *The Nucleotide Transformer: Building and Evaluating Robust Foundation Models for Human Genomics.* [Nature Methods](https://www.nature.com/articles/s41592-024-02330-3)

### Drug Discovery
- **ChemBERTa**: Chithrananda et al. (2020). *ChemBERTa: Large-Scale Self-Supervised Pretraining for Molecular Property Prediction.* [arXiv:2010.09885](https://arxiv.org/abs/2010.09885)
- **MolT5**: Edwards et al. (2022). *Translation between Molecules and Natural Language.* [arXiv:2204.11817](https://arxiv.org/abs/2204.11817)

### Clinical NLP Foundations
- **ClinicalBERT**: Alsentzer et al. (2019). *Publicly Available Clinical BERT Embeddings.* [arXiv:1904.03323](https://arxiv.org/abs/1904.03323)
- **i2b2 overview**: Uzuner et al. (2011). *Extracting medication information from discharge summaries.* JAMIA.

### Evaluation & Safety
- **Med-HALT**: Pal et al. (2024). *Med-HALT: Medical Domain Hallucination Test for Large Language Models.* [arXiv:2307.15389](https://arxiv.org/abs/2307.15389)
- **Clinical safety evaluation**: Omiye et al. (2023). *Large language models propagate race-based medicine.* [Nature](https://www.nature.com/articles/d41586-023-02261-3)

## Ontologies & Knowledge Bases

Essential for any biomedical NLP/LLM practitioner entering the field.

| Resource | Coverage | Link | When to use |
|---|---|---|---|
| **UMLS** | Unified Medical Language System | [NLM](https://www.nlm.nih.gov/research/umls/) | General biomedical concept mapping; requires license (free for research) |
| **MedDRA** | Adverse drug reactions | [meddra.org](https://www.meddra.org/) | Pharmacovigilance, ADR coding; updates twice yearly |
| **SNOMED CT** | Clinical terminology | [snomed.org](https://www.snomed.org/) | Clinical notes, EHR coding |
| **RxNorm** | Drug nomenclature | [NLM](https://www.nlm.nih.gov/research/umls/rxnorm/) | Drug normalization, prescription matching |
| **ICD-10/11** | Disease classification | [WHO](https://icd.who.int/) | Diagnosis coding; billing, clinical NER |
| **LOINC** | Lab observations | [loinc.org](https://loinc.org/) | Lab test naming, clinical data standardization |
| **ChEMBL** | Bioactive molecules | [ebi.ac.uk](https://www.ebi.ac.uk/chembl/) | Drug discovery, molecular properties |
| **DrugBank** | Drug data | [drugbank.com](https://www.drugbank.com/) | Drug interactions, pharmacology |
| **PubMed** | Biomedical literature | [pubmed.ncbi.nlm.nih.gov](https://pubmed.ncbi.nlm.nih.gov/) | 36M+ citations; primary literature source |
| **ClinicalTrials.gov** | Clinical trials | [clinicaltrials.gov](https://clinicaltrials.gov/) | Trial data, drug development pipeline |

## Courses & Tutorials

| Resource | Focus | Link |
|---|---|---|
| AMIA Informatics Summit tutorials | Clinical NLP, AI in healthcare | [amia.org](https://amia.org/) |
| BioNLP workshop tutorials (ACL) | Biomedical NLP methods | [aclanthology.org](https://aclanthology.org/venues/bionlp/) |
| Stanford CS25 Transformers | LLM foundations | [stanford.edu](https://web.stanford.edu/class/cs25/) |
| Stanford BMI 215 | Biomedical informatics | [stanford.edu](https://bmi.stanford.edu/) |
| DeepLearning.AI Drug Discovery | AI for drug discovery | [deeplearning.ai](https://www.deeplearning.ai/) |

## Glossary

For ML practitioners entering biomedicine.

| Term | Meaning |
|---|---|
| EHR | Electronic Health Record — patient's digital medical record |
| MIMIC | Medical Information Mart for Intensive Care — critical care database |
| ADR | Adverse Drug Reaction |
| NER | Named Entity Recognition — identifying medical entities in text |
| RE | Relation Extraction — finding relationships between entities (e.g., drug–disease) |
| Pharmacovigilance | Detection and prevention of adverse drug effects |
| SMILES | Simplified Molecular-Input Line-Entry System — text representation of molecules |
| scRNA-seq | Single-cell RNA sequencing — gene expression at individual cell level |
| FDA label | Official prescribing information approved by the US FDA |
| USMLE | US Medical Licensing Examination — benchmark for medical LLMs |
| CITI training | Required ethics training for accessing clinical data (HIPAA, human subjects) |
| HIPAA | Health Insurance Portability and Accountability Act — US health privacy law |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Suggest additions via [issues](https://github.com/infonality/awesome-llm-biomedicine/issues/new) or submit a pull request.

## License

[CC0 1.0 (Public Domain)](https://creativecommons.org/publicdomain/zero/1.0/)

---

*Last updated: July 2026 · Maintained by [@infonality](https://github.com/infonality)*