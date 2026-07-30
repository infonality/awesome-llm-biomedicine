# Awesome LLM for Biomedicine

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of large language models, datasets, tools, and benchmarks for biomedical and clinical applications — covering clinical text understanding, drug discovery, genomics, protein science, and healthcare AI.

PRs welcome — [suggest a resource](https://github.com/infonality/awesome-llm-biomedicine/issues/new).

---

## Contents

- [Clinical LLMs](#clinical-llms)
- [Genomics LLMs](#genomics-llms)
- [Drug Discovery & Molecular LLMs](#drug-discovery--molecular-llms)
- [Protein & Structural Biology LLMs](#protein--structural-biology-llms)
- [Benchmarks & Datasets](#benchmarks--datasets)
- [Shared Tasks & Challenges](#shared-tasks--challenges)
- [Tools & Libraries](#tools--libraries)
- [Key Papers](#key-papers)
- [Ontologies & Knowledge Bases](#ontologies--knowledge-bases)
- [Courses & Tutorials](#courses--tutorials)
- [Glossary](#glossary)

---

## Clinical LLMs

Pre-trained models fine-tuned on clinical notes, EHR data, and medical literature.

- [BioBERT](https://github.com/dmis-lab/biobert) - 110M params. PubMed + PMC. Early biomedical BERT; widely cited.
- [BioMedLM (PubMedGPT)](https://huggingface.co/stanford-crfm/BioMedLM) - 2.7B params. Stanford CRFM; domain-specific from scratch.
- [BioGPT](https://github.com/microsoft/BioGPT) - 1.5B params. PubMed + papers. Microsoft's generative model for biomedical text generation and mining.
- [BioMistral](https://huggingface.co/BioMistral/BioMistral-7B) - 7B params. PubMed Central. Mistral-based open biomedical LLM.
- [ClinicalBERT](https://huggingface.co/emilyalsentzer/Bio_ClinicalBERT) - 110M params. MIMIC-III discharge summaries. BERT fine-tuned on clinical notes.
- [Clinical-Camel](https://github.com/epfLLM/meditron) - 7B/13B/70B params. Clinical domain adaptation of LLaMA-2.
- [ClinicalLongformer](https://huggingface.co/yikao810/ClinicalLongformer) - 4K context. Clinical notes. Long-context clinical model for full notes.
- [GatorTron](https://arxiv.org/abs/2203.03560) - 3.9B/8.9B params. 90B tokens (clinical + PubMed). Large clinical model from UF Health.
- [Med-PaLM 2](https://arxiv.org/abs/2305.09617) - Google's medical LLM. Achieves USMLE-level performance; not open-weight.
- [MEDITRON](https://huggingface.co/epfl-llm/meditron-7b) - 7B/70B params. Medical papers + guidelines. EPFL; open-weight, clinical reasoning.
- [PMC-LLaMA](https://huggingface.co/axiong/PMC_LLaMA_13B) - 7B/13B params. PubMed Central. LLaMA fine-tuned on biomedical literature.
- [PubMedBERT](https://huggingface.co/microsoft/PubMedBERT) - 110M params. PubMed abstracts (from scratch). Strong baseline for biomedical NLP.

## Genomics LLMs

Foundation models for single-cell RNA-seq, DNA sequences, and genomics.

- [Caduceus](https://github.com/klab-lab/caduceus) - DNA sequences. Reversible and bi-directional DNA sequence modeling.
- [DNABERT-2](https://github.com/MAGICS-LAB/DNABERT_2) - 117M params. DNA sequences. Improved genome understanding model.
- [Geneformer](https://github.com/jxmorisette/geneformer) - 95M params. scRNA-seq. Foundation model for transcriptomics; pre-trained on 30M cells.
- [HyenaDNA](https://github.com/HazyResearch/hyena-dna) - 1K-1M context. DNA sequences. Ultra-long-context genomic model.
- [Nucleotide Transformer](https://huggingface.co/InstaDeepAI/nucleotide-transformer-2.5b-multi-species) - 500M-2.5B params. DNA sequences. Multi-species DNA foundation model.
- [scGPT](https://github.com/bowang-lab/scGPT) - ~50M params. scRNA-seq. Single-cell foundation model; cell type annotation, perturbation prediction.

## Drug Discovery & Molecular LLMs

Models for molecular property prediction, drug-drug interaction, and chemical generation.

- [ChemBERTa](https://huggingface.co/seyonec/ChemBERTa-zinc-base-v1) - SMILES molecules. RoBERTa for molecular property prediction.
- [Chemformer](https://github.com/MolecularAI/Chemformer) - SMILES to reactions. Transformer for retrosynthesis.
- [Galactica](https://huggingface.co/facebook/galactica-120b) - Scientific text + molecules. Meta's science LLM (deprecated but influential).
- [MolT5](https://github.com/blender-lab/MolT5) - Molecule to text. T5 for molecule captioning and generation.
- [Uni-Mol](https://github.com/dptech-corp/Uni-Mol) - 3D molecular. 3D molecular representation model.

## Protein & Structural Biology LLMs

- [ESM-2](https://github.com/facebookresearch/esm) - 650M-15B params. Protein sequences. Meta's protein language model; structure prediction.
- [ProGen2](https://github.com/salesforce/progen2) - 6.4B-151B params. Protein sequences. Generative protein design model.
- [ProtTrans](https://huggingface.co/Rostlab/prot_bert_bfd) - 420M-3B params. Protein sequences. Transformer for protein sequences.
- [RoseTTAFold](https://github.com/RosettaCommons/RoseTTAFold) - Protein structure. 3D protein structure prediction (non-LLM but essential).
- [SaProt](https://huggingface.co/westlake-repl/SaProt-650M) - 650M params. Protein (folded). Structure-aware protein model.

## Benchmarks & Datasets

### Clinical Text

- [BioASQ](http://bioasq.org/) - QA, retrieval. ~5K questions. Biomedical question answering benchmark.
- [BlueBERT benchmark suite](https://github.com/ncbi-nlp/BlueBERT) - Multiple tasks. NCBI's benchmark suite for biomedical language understanding.
- [MedQA (USMLE)](https://github.com/jind11/MedQA) - QA. 12.7K questions. US medical licensing exam questions.
- [MIMIC-III / MIMIC-IV](https://physionet.org/content/mimiciv/) - Clinical notes, tables. 2M+ notes. Most-used clinical text corpus; requires training + CITI.
- [MMLU (medical subsets)](https://github.com/hendrycks/test) - MCQ. 1K+ per subject. Clinical knowledge evaluation; widely used in LLM benchmarks.
- [n2c2 / i2b2](https://portal.dbmi.hms.harvard.edu/projects/n2c2-2024/) - NER, RE, coreference. ~1,000 notes each year. Historical shared tasks; clinical notes.
- [PubMedQA](https://github.com/pubmedqa/pubmedqa) - QA. 1K expert + 211K unlabeled. QA over PubMed abstracts.

### Relation Extraction & Drug Interactions

- [ADE Corpus](https://github.com/dmis-lab/ade-corpus) - Adverse drug events. 3,000+ sentences.
- [ChemProt](https://github.com/arwhirang/recursive_chemprot) - Chemical-protein RE. 1,820 abstracts.
- [DDI (DrugBank)](https://github.com/ncbi-nlp/DDIExtraction2013) - Drug-drug interaction. 792 documents.
- [EU-ADR](https://github.com/madmanc/EU-ADR-corpus) - Drug-adverse effect. 3,000 sentences.
- [GAD](https://github.com/dmis-lab/biobert) - Gene-disease association. 5,330 sentences.

### Genomics

- [CellxGene](https://cellxgene.cziscience.com/) - scRNA-seq census. 50M+ cells. Chan Zuckerberg Initiative; largest single-cell atlas.
- [GEO](https://www.ncbi.nlm.nih.gov/geo/) - Gene expression. 20M+ samples. Gene Expression Omnibus.
- [Tabula Sapiens](https://tabula-sapiens.ds.czbiohub.org/) - scRNA-seq. 500K+ cells. Multi-organ human cell atlas.

## Shared Tasks & Challenges

- [BioASQ Challenge](http://bioasq.org/) - Biomedical QA and retrieval. 2013-present.
- [BioNLP Shared Task](https://github.com/openbiomedicalnlp/bionlp-st) - Event extraction from biomedical text. 2009-2023.
- [MEDIQA](https://github.com/abachaa/MEDIQA) - Medical text generation and summarization. 2019-2024.
- [MedNLI](https://github.com/jgc128/mednli) - Natural language inference in clinical text. 2018.
- [n2c2 / i2b2](https://portal.dbmi.hms.harvard.edu/projects/n2c2-2024/) - Clinical NLP challenges. 2007-present.
- [TAC ADR Extraction](https://tac.nist.gov/2017/ADRF/) - ADR extraction from drug labels. 2017.

## Tools & Libraries

- [BERN2](https://github.com/dl4ds/bernal) - Biomedical NER. Multi-type entity recognition (disease, drug, gene, etc.).
- [BigBIO](https://github.com/bigscience-workshop/biomedical) - Dataset loading. Unified access to 160+ biomedical datasets.
- [BioC](https://github.com/biocreative/bioc) - Biomedical text format. XML/JSON interchange format for biomedical text.
- [BioGPT inference](https://github.com/microsoft/BioGPT) - Text generation. Microsoft's biomedical generative model.
- [cTAKES](https://ctakes.apache.org/) - Clinical NLP. Clinical Text Analysis Knowledge Extraction System.
- [MedSpaCy](https://github.com/medspacy/medspacy) - Clinical NLP pipeline. Clinical text processing, section detection.
- [scispaCy](https://github.com/allenai/scispacy) - Biomedical NLP pipeline. spaCy models for biomedical NER, linking.

## Key Papers

### Clinical LLMs

- BioBERT: Lee et al. (2020). BioBERT: a pre-trained biomedical language representation model for biomedical text mining. [arXiv:1901.08746](https://arxiv.org/abs/1901.08746)
- BioGPT: Luo et al. (2022). BioGPT: generative pre-trained transformer for biomedical text generation and mining. [arXiv:2210.17100](https://arxiv.org/abs/2210.17100)
- ClinicalBERT: Alsentzer et al. (2019). Publicly Available Clinical BERT Embeddings. [arXiv:1904.03323](https://arxiv.org/abs/1904.03323)
- Med-PaLM: Singhal et al. (2023). Large language models encode clinical knowledge. [arXiv:2212.13138](https://arxiv.org/abs/2212.13138)
- MEDITRON: Chen et al. (2023). MEDITRON-70B: Scaling Medical Pretraining of Language Models. [arXiv:2311.18279](https://arxiv.org/abs/2311.18279)
- PubMedBERT: Gu et al. (2021). Domain-Specific Language Model Pretraining for Biomedical Natural Language Processing. [arXiv:2007.15779](https://arxiv.org/abs/2007.15779)

### Genomics LLMs

- Geneformer: Theodoris et al. (2023). Transfer learning enables predictions in network biology. [Nature](https://www.nature.com/articles/s41586-023-06139-9)
- Nucleotide Transformer: Dalla-Torre et al. (2024). The Nucleotide Transformer: Building and Evaluating Robust Foundation Models for Human Genomics. [Nature Methods](https://www.nature.com/articles/s41592-024-02330-3)
- scGPT: Cui et al. (2024). scGPT: Toward Building a Foundation Model for Single-Cell Multi-omics Using Single-Cell Transcriptomics. [Nature Methods](https://www.nature.com/articles/s41592-024-02205-7)

### Drug Discovery

- ChemBERTa: Chithrananda et al. (2020). ChemBERTa: Large-Scale Self-Supervised Pretraining for Molecular Property Prediction. [arXiv:2010.09885](https://arxiv.org/abs/2010.09885)
- MolT5: Edwards et al. (2022). Translation between Molecules and Natural Language. [arXiv:2204.11817](https://arxiv.org/abs/2204.11817)

### Evaluation & Safety

- Clinical safety evaluation: Omiye et al. (2023). Large language models propagate race-based medicine. [Nature](https://www.nature.com/articles/d41586-023-02261-3)
- Med-HALT: Pal et al. (2024). Med-HALT: Medical Domain Hallucination Test for Large Language Models. [arXiv:2307.15389](https://arxiv.org/abs/2307.15389)

## Ontologies & Knowledge Bases

Essential for any biomedical NLP/LLM practitioner entering the field.

- [ChEMBL](https://www.ebi.ac.uk/chembl/) - Bioactive molecules. Drug discovery, molecular properties.
- [ClinicalTrials.gov](https://clinicaltrials.gov/) - Clinical trials. Trial data, drug development pipeline.
- [DrugBank](https://www.drugbank.com/) - Drug data. Drug interactions, pharmacology.
- [ICD-10/11](https://icd.who.int/) - Disease classification. Diagnosis coding; billing, clinical NER.
- [LOINC](https://loinc.org/) - Lab observations. Lab test naming, clinical data standardization.
- [MedDRA](https://www.meddra.org/) - Adverse drug reactions. Pharmacovigilance, ADR coding; updates twice yearly.
- [PubMed](https://pubmed.ncbi.nlm.nih.gov/) - Biomedical literature. 36M+ citations; primary literature source.
- [RxNorm](https://www.nlm.nih.gov/research/umls/rxnorm/) - Drug nomenclature. Drug normalization, prescription matching.
- [SNOMED CT](https://www.snomed.org/) - Clinical terminology. Clinical notes, EHR coding.
- [UMLS](https://www.nlm.nih.gov/research/umls/) - Unified Medical Language System. General biomedical concept mapping; requires license (free for research).

## Courses & Tutorials

- [AMIA Informatics Summit tutorials](https://amia.org/) - Clinical NLP, AI in healthcare.
- [BioNLP workshop tutorials (ACL)](https://aclanthology.org/venues/bionlp/) - Biomedical NLP methods.
- [DeepLearning.AI Drug Discovery](https://www.deeplearning.ai/) - AI for drug discovery.
- [Stanford BMI 215](https://bmi.stanford.edu/) - Biomedical informatics.
- [Stanford CS25 Transformers](https://web.stanford.edu/class/cs25/) - LLM foundations.

## Glossary

For ML practitioners entering biomedicine.

- ADR - Adverse Drug Reaction.
- CITI training - Required ethics training for accessing clinical data (HIPAA, human subjects).
- EHR - Electronic Health Record — patient's digital medical record.
- FDA label - Official prescribing information approved by the US FDA.
- HIPAA - Health Insurance Portability and Accountability Act — US health privacy law.
- MIMIC - Medical Information Mart for Intensive Care — critical care database.
- NER - Named Entity Recognition — identifying medical entities in text.
- Pharmacovigilance - Detection and prevention of adverse drug effects.
- RE - Relation Extraction — finding relationships between entities (e.g., drug-disease).
- scRNA-seq - Single-cell RNA sequencing — gene expression at individual cell level.
- SMILES - Simplified Molecular-Input Line-Entry System — text representation of molecules.
- USMLE - US Medical Licensing Examination — benchmark for medical LLMs.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Suggest additions via [issues](https://github.com/infonality/awesome-llm-biomedicine/issues/new) or submit a pull request.
