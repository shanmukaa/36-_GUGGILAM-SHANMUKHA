This project matches a sample patient profile to relevant COVID-19 clinical trials using data from ClinicalTrials.gov. Trial metadata is loaded from a CSV file, while detailed inclusion and exclusion criteria are extracted directly from ClinicalTrials.gov XML files.

The system uses sentence-transformer embeddings and a FAISS vector store to retrieve the top-K most relevant trials based on semantic similarity to the patient profile. Eligibility decisions are then determined using deterministic logic that evaluates the patient profile against the extracted inclusion and exclusion criteria, ensuring transparent and reproducible results.

The final output consists of trial IDs along with an eligibility decision (ELIGIBLE or NOT ELIGIBLE) and clear justification derived from the trial criteria. No model training or external LLM APIs are used; the approach follows a retrieval-based and rule-driven eligibility matching pipeline.
