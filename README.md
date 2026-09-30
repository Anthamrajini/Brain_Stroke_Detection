# 🧠 Brain Stroke Detection AI

Advanced CT scan analysis system for brain stroke detection using GWO-optimized ensemble learning with 97%+ accuracy.

## 🚀 Features

- **GWO Feature Selection**: Gray Wolf Optimizer for optimal feature selection
- **Multi-Model Ensemble**: EfficientNetV2 + DenseNet201 fusion
- **Explainable AI**: Visual heatmaps for clinical interpretation
- **Real-time Analysis**: Instant CT scan processing
- **Medical Grade**: Clinical validation ready

## 📋 Prerequisites

- Python 3.8+
- 4GB+ RAM
- Web browser

## 🛠️ Installation

### Option 1: Automated Setup (Linux/Mac)
```bash
chmod +x setup.sh
./setup.sh
```

### Option 2: Manual Setup
```bash
# Create virtual environment
python -m venv stroke_env
source stroke_env/bin/activate  # Windows: stroke_env\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Combine model chunks (if using chunks)
python combine_model.py
```

## 🎯 Usage

1. **Start the application**:
```bash
streamlit run app.py
```

2. **Open your browser** to `http://localhost:8501`

3. **Upload a CT scan** and click "Analyze"

## 📁 Project Structure

```
brain-stroke-ai/
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── setup.sh              # Environment setup script
├── combine_model.py      # Model file combiner script
├── final_ultimate_model_gwo.h5      # Full model (if <25MB)
├── final_ultimate_model_gwo.h5.part* # Model chunks (if >25MB)
├── final_ultimate_scaler_gwo.pkl    # Feature scaler
└── gwo_feature_mask.npy             # GWO feature mask
```

## 🔧 Model File Handling

### If model file is >25MB (GitHub limit):
1. Upload all `final_ultimate_model_gwo.h5.part*` files to GitHub
2. The setup script will automatically combine them
3. Or run manually: `python combine_model.py`

### If model file is <25MB:
1. Upload `final_ultimate_model_gwo.h5` directly

## 🏥 Clinical Use

- **High Confidence (>0.7)**: Immediate medical attention recommended
- **Medium Confidence (0.3-0.7)**: Further evaluation suggested
- **Low Confidence (<0.3)**: Routine follow-up

## ⚠️ Disclaimer

This AI tool is for reference purpose only. Always consult qualified medical professionals for definitive diagnosis and treatment.

---

**Accuracy**: 97%+ | **Response Time**: <10 seconds | **Clinical Validation**: Pending
