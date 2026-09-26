# Ansh Chhikara

AI engineering student in Gurugram, India. I build RAG systems, LLM evaluations and LangGraph
agents, and I measure whether they actually work before I claim they do.

**Open to AI/ML internships** · [chikaraansh0@gmail.com](mailto:chikaraansh0@gmail.com) · [LinkedIn](https://www.linkedin.com/in/ansh-chhikara-961175369/)

## Projects

### [hybridrag](https://github.com/AnshChhikara001/hybridrag)
Hybrid BM25 + dense retrieval over FastAPI's docs, fused with Reciprocal Rank Fusion, with
inline citations that are checked claim by claim against the cited source.
- Recall@5 **0.90** vs 0.83 dense-only, on a hand-verified golden set with bootstrap intervals
- Citation support **0.90** vs 0.05 for random passages (negative control)
- A cross-encoder reranker was built, measured, and left out: it didn't beat plain hybrid
- 580+ tests, CI, FastAPI service and Streamlit dashboard. Total API spend: $0.29

`Python` `Chroma` `rank_bm25` `FastAPI` `Streamlit`

### [synclint](https://github.com/AnshChhikara001/synclint) · [Marketplace](https://github.com/marketplace/actions/synclint)
A GitHub Action that finds the documentation a pull request made wrong, repairs what it
safely can, and flags the rest. It links code chunks (parsed with `ast`) to the markdown
sections that describe them, asks a model whether each affected section is still accurate,
and opens a pull request of repairs.
- 100% precision and 0 false positives on 18 decoys; 7 of 7 changes found in a real library
  ([humanize](https://github.com/python-humanize/humanize)), 61% recall on a planted-drift corpus
- A rules-based gate stopped the one wrong repair that model validation approved; the model's
  confidence (96–99% every time) could not
- Released as v1.0.0, 227 tests, mypy strict. A live run costs about $0.002

`Python` `GitHub Actions` `OpenAI` `ast` `embeddings`

### [pharma-ccms](https://github.com/AnshChhikara001/pharma-ccms)
Customer complaint management for pharmaceutical QA. A complaint narrative pasted in plain
English becomes a structured, auditable record through a LangGraph agent.
- Extracts fields with provenance, flags missing information, suggests severity, finds duplicates
- Every model call passes through a hard spend cap; AI output is advisory, never a determination
- Role-based access with segregation of duties, automatic audit trail, 299 backend tests

`LangGraph` `FastAPI` `PostgreSQL` `React` `TypeScript`

### [ai-ats-resume-analyzer](https://github.com/AnshChhikara001/ai-ats-resume-analyzer)
Scores a resume against a job description. Llama 3.3 (via Groq) parses both into structured
fields; the score combines keyword overlap with MiniLM semantic similarity, and every listed
skill is checked for evidence in the resume's projects and experience.

`FastAPI` `spaCy` `Sentence-Transformers` `Supabase`

### [SnapClass](https://github.com/AnshChhikara001/SNAP-CLASS---ANSH)
Classroom attendance from a single class photo: dlib face embeddings with an SVM classifier,
plus voice verification with Resemblyzer speaker embeddings.
**[Live demo](https://ansh-snap-classes.streamlit.app/)**

`Streamlit` `dlib` `Resemblyzer` `Supabase`

## Stack

Python · TypeScript · LangGraph · FastAPI · Sentence-Transformers · Chroma · PostgreSQL ·
Supabase · React · Docker · GitHub Actions
