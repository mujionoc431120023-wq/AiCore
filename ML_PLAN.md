# Plan: ML Integration & Dataset Generation for OS-Mini AI

## Information Gathered

### Current System Overview:
- **Architecture**: Rule-based AI with fuzzy logic, context-aware switching
- **Languages**: C (core), Python (optional helpers)
- **AI Domains**: Healthcare, Education, Finance, Manufacturing, IoT, Smart City, Governance, Future AI, CodeAgent
- **Intelligence Features**: 
  - Fuzzy Logic (anti-typo)
  - Context-Aware Switching
  - Multi-language Detection
  - Sentiment Analysis
  - Long-term Memory (Persistence)
  - Self-Repair System

### Existing Modules:
- `/src/main.c` - Main CLI application
- `/src/ai_hub.c` - Central AI dispatcher
- `/src/codeagent.c` - Coding assistant
- `/ai_core/src/intelligence/` - Intelligence modules (fuzzy, context, sentiment, etc.)
- `/include/ai_hub.h` - Header definitions

## Plan

### Step 1: Create ML Integration Layer (Python)
- Create `ml_integration.py` with scikit-learn models
- Implement classification models for each domain
- Add sentiment analysis with ML (complement existing rule-based)
- Add prediction models for manufacturing, finance
- Add clustering for IoT device patterns

### Step 2: Create Dataset Generator
- Create `dataset_generator.py`
- Generate comprehensive dataset from all AI domains
- Include features: input_text, domain, sentiment, context, output
- Export to CSV/JSON format for ML training

### Step 3: Create ML-Powered Enhancements
- Add prediction endpoints for each domain
- Add anomaly detection for IoT/Manufacturing
- Add sentiment classification with ML model

### Step 4: Update Requirements
- Add scikit-learn, pandas, numpy to requirements.txt
- Add Python ML dependencies

### Step 5: Create ML Training Script
- Create `train_models.py`
- Train models on generated dataset
- Save models for inference

## Dependent Files to be Created

1. **New Files:**
   - `ml_integration/` - ML module directory
   - `ml_integration/__init__.py`
   - `ml_integration/dataset_generator.py` - Dataset generation
   - `ml_integration/train_models.py` - Model training
   - `ml_integration/predictors.py` - ML predictors
   - `ml_integration/sentiment_ml.py` - ML sentiment analysis
   - `datasets/os_mini_ai_dataset.csv` - Generated dataset

2. **Modified Files:**
   - `requirements.txt` - Add ML dependencies

## Followup Steps

1. Install dependencies: `pip install -r requirements.txt`
2. Generate dataset: `python ml_integration/dataset_generator.py`
3. Train models: `python ml_integration/train_models.py`
4. Test ML integration: `python ml_integration/predictors.py`

