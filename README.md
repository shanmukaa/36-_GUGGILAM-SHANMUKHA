Clinical Trial Eligibility Matching System

This project matches a patient profile to relevant COVID-19 clinical trials using data from ClinicalTrials.gov. Trial metadata is read from a CSV file, while detailed inclusion and exclusion criteria are extracted from ClinicalTrials.gov XML files.

Semantic search is performed using sentence-transformer embeddings and a FAISS vector store to retrieve the most relevant trials based on inclusion criteria. An open-source HuggingFace language model (FLAN-T5) integrated through LangChain is used to reason over inclusion and exclusion criteria and determine patient eligibility.

The system produces Top-K trial IDs along with a clear eligibility decision (ELIGIBLE or NOT ELIGIBLE) and a short justification. No model training or fine-tuning is performed; the approach follows a retrieval-augmented reasoning pipeline using pre-trained models.
