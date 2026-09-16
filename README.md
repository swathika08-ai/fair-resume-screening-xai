# An Explainable AI Framework for Fair Resume Screening and Candidate Skill Gap Analysis

## Project Type

**Research-Oriented Major Project**

## Team

* Balabhadra Swathika
* Annapureddy Bala Yaswanth
* Chinta Venkata Madhuri
* Ala Venu Gopal

## Guide

Mrs. P. Nikhitha

# Abstract

Organizations receive thousands of resumes for a single job opening, making manual resume screening time-consuming, inconsistent, and prone to human bias. Existing AI-powered recruitment systems automate candidate ranking but often operate as black-box models that do not provide explanations for their decisions. Furthermore, concerns regarding gender, race, and demographic bias have raised questions about the fairness of automated hiring systems.

This project proposes an Explainable AI Framework for Fair Resume Screening and Candidate Skill Gap Analysis. The system leverages Sentence-BERT embeddings for semantic matching between resumes and job descriptions, fairness analysis for identifying potential bias in ranking outcomes, Explainable AI techniques such as SHAP and LIME for transparent decision-making, and a skill-gap analysis module to identify missing competencies in candidates.

The proposed framework aims to improve transparency, fairness, and trustworthiness in AI-assisted recruitment systems.

# Problem Statement

Traditional recruitment processes face several challenges:

* Large volume of job applications
* Time-consuming manual screening
* Inconsistent candidate evaluation
* Human bias during selection
* Lack of transparency in AI-based screening systems

Most existing AI systems focus only on candidate ranking and fail to answer:

* Why was a candidate selected?
* Why was a candidate rejected?
* Is the ranking fair?
* Which skills are missing?

This project aims to address these limitations.

# Research Gap

The base paper:

**Gender, Race, and Intersectional Bias in Resume Screening via Language Model Retrieval (AIES 2024)**

focuses on identifying demographic bias in resume retrieval systems.

### Limitations of Existing Research

* Focuses primarily on bias detection
* Does not provide explainable recommendations
* Does not identify missing candidate skills
* Does not provide fairness-aware recruitment support
* Not designed as a complete recruiter-facing application

# Proposed Solution

We propose a multi-component AI framework consisting of:

1. Semantic Resume Matching
2. Fairness Analysis
3. Explainable AI Module
4. Skill Gap Analysis
5. Recruiter Dashboard

The system will evaluate resumes against job descriptions while providing transparent explanations and fairness insights.

# Project Objectives

### Primary Objectives

* Automate resume screening
* Improve candidate-job matching accuracy
* Detect potential demographic bias
* Explain AI-generated rankings
* Identify candidate skill gaps

### Secondary Objectives

* Increase recruiter trust in AI decisions
* Improve transparency in hiring
* Support fair recruitment practices

# Novelty of the Project

The novelty lies in combining four major components into a single recruitment framework.

## Novelty 1: Explainable Resume Ranking

Traditional systems provide only scores.

Example:

Candidate A → 95

Candidate B → 85

Our system explains:

Candidate A ranked higher because:

* Python skills
* Machine Learning experience
* Cloud certifications

Technologies:

* SHAP
* LIME

## Novelty 2: Fairness Analysis

Existing systems may unintentionally favor specific groups.

Our framework analyzes ranking outcomes to identify:

* Potential demographic disparities
* Group-wise ranking patterns
* Fairness metrics

This increases transparency and accountability.

## Novelty 3: Skill Gap Analysis

The system compares:

Resume Skills

vs

Job Requirements

and identifies:

* Missing skills
* Recommended improvements
* Candidate readiness level

Example:

Required:

* Python
* SQL
* AWS

Candidate:

* Python
* SQL

Output:

Missing Skill:

* AWS

## Novelty 4: Semantic Understanding

Instead of simple keyword matching, the system uses Sentence-BERT.

Example:

Resume:
"Machine Learning Engineer"

Job Description:
"AI Developer"

Although keywords differ, Sentence-BERT captures semantic similarity.

# System Architecture

```text
Job Description
       │
       ▼
 Resume Collection
       │
       ▼
 Resume Parsing
       │
       ▼
 Sentence-BERT Embedding Generation
       │
       ▼
 Similarity Calculation
(Cosine Similarity)
       │
       ▼
 Candidate Ranking
       │
 ┌─────┼───────────┐
 ▼     ▼           ▼
Fairness   Explainability   Skill Gap
Analysis   (SHAP/LIME)      Analysis
 │          │                │
 └──────────┼────────────────┘
            ▼
    Final Recruiter Report
```

# Technologies Used

## AI / NLP

* Python
* Sentence-BERT
* Transformers
* Scikit-Learn

## Explainable AI

* SHAP
* LIME

## Data Processing

* Pandas
* NumPy

## Visualization

* Matplotlib
* Seaborn
* Plotly

## Backend

* Flask / FastAPI

## Frontend

* HTML
* CSS
* JavaScript
* Bootstrap

## Database

* SQLite

# Dataset

Potential datasets:

### Resume Dataset

* Kaggle Resume Dataset
* Resume Screening Dataset

### Job Description Dataset

* Kaggle Job Description Dataset

### Research Dataset

* Public benchmark datasets used in resume screening research

# Methodology

## Phase 1: Data Collection

Collect:

* Resumes
* Job descriptions

Perform:

* Cleaning
* Preprocessing
* Normalization

## Phase 2: Semantic Matching

Generate embeddings using Sentence-BERT.

Compute:

```text
Resume Embedding
       vs
Job Description Embedding
```

Using:

* Cosine Similarity

Output:

* Matching score

## Phase 3: Candidate Ranking

Sort candidates based on similarity scores.

Generate:

* Top candidate list

## Phase 4: Explainable AI

Apply:

### SHAP

Global feature importance.

### LIME

Local candidate-level explanations.

Output:

* Why candidate was selected
* Important skills influencing ranking

## Phase 5: Fairness Analysis

Evaluate:

* Group-wise score distribution
* Ranking disparities
* Fairness indicators

Identify:

* Potential bias patterns

## Phase 6: Skill Gap Analysis

Extract:

* Candidate skills
* Required skills

Compare both sets.

Generate:

* Missing skills
* Suggested learning areas

# Evaluation Metrics

## Ranking Performance

* Precision@K
* Recall@K
* NDCG
* MAP

## Similarity Quality

* Cosine Similarity Score

## Explainability

* Explanation Consistency
* Feature Importance Validation

## Fairness Metrics

* Ranking Distribution Analysis
* Demographic Parity Analysis
* Fairness Comparison Metrics

# Expected Outcomes

The system should:

* Accurately rank candidates
* Provide transparent explanations
* Detect possible bias
* Identify missing skills
* Support recruiters in decision-making

# Deliverables

## Research Deliverables

* Literature Survey
* Base Paper Analysis
* Comparative Study
* Experimental Results

## Technical Deliverables

* Source Code
* Trained Models
* Dataset
* Evaluation Report
* Research Paper
* Final Project Report

# Future Scope

* Integration with ATS systems
* Interview recommendation engine
* Real-time recruitment platform
* Multilingual resume analysis
* LLM-powered recruiter assistant
* AI-generated candidate feedback

# Conclusion

This project extends existing resume screening research by integrating semantic matching, fairness analysis, explainable AI, and skill-gap identification into a unified recruitment framework. The proposed system aims to make AI-assisted hiring more accurate, transparent, interpretable, and fair while addressing key limitations of existing resume screening approaches.
