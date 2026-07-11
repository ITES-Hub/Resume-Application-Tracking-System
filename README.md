This repository showcases a highly scalable, end-to-end AI-Powered Applicant Tracking System (ATS) Engine designed to streamline corporate recruitment through advanced semantic analysis and automated talent pipelines. Moving far beyond legacy, rigid keyword-counting software that often penalizes qualified candidates for minor phrasing differences, this platform leverages state-of-the-art Natural Language Processing (NLP) to execute deep, multi-layered alignment evaluations between unstructured candidate resumes and institutional job descriptions.

The architecture is built upon an optimized, four-stage programmatic pipeline:

Document Parsing & Text Extraction: Ingests native PDF resume submissions, dynamically stripping away format layout constraints, structural text boxes, and styling anomalies to convert the data into standardized, clean strings.

High-Dimensional Semantic Analysis: Utilizes a transformer-based vector model (all-MiniLM-L6-v2) to encode both the resume and the target job description into dense vector embeddings. By running a Cosine Similarity computation, the engine assigns an overall contextual score that rewards candidates whose experiential concepts and background profiles align with the role, regardless of vocabulary variance.

Fuzzy Entity Extraction & Skills Mapping: Employs spaCy to isolate critical grammatical components (Nouns and Proper Nouns) within the job specification. These are fed through a rapidfuzz string-matching algorithm matched against a master industrial competency framework to bypass minor typos or pluralizations. A robust, custom lowercase-to-title case mapping function prevents traditional case-sensitivity mismatch bugs during validation.

Skills Gap Analysis & Composite Logic: The engine executes a precise set-subtraction matrix to cross-reference candidate skills against requirements, explicitly printing out an actionable Missing Skills list. It then compiles an Integrated ATS Rating—a weighted blend of 40% overarching semantic context and 60% hard-skills verification.

The system concludes by running this integrated rating through an automated enterprise decision matrix. It instantly categorizes applicants into clean operational funnels (Highly Recommended, Considered for Interview, or Not Recommended) and attaches prescriptive next-step instructions for HR managers. Built in Python and optimized for high-performance execution within Google Colab, this prototype demonstrates a sophisticated, data-driven approach to eliminating manual recruitment friction and standardizing modern talent evaluation.
