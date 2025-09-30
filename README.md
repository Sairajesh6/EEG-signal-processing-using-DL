# EEG Classification for Seizure Diagnosis  

## 📌 Project Overview  
This project focuses on automated seizure diagnosis using EEG spectrogram analysis. We experimented with transformer-based architectures and proposed a **novel spatio-temporal deep learning pipeline**, achieving **92%+ classification accuracy on 106k EEG samples**.  

The system is designed to:  
- Convert EEG time-series into spectrogram representations.  
- Learn both spatial and temporal dependencies across multiple EEG channels.  
- Provide scalable inference for real-time seizure detection.  

## 🔑 Key Features  
- **Novel Spatio-Temporal Model**: Captures fine-grained temporal dependencies across EEG signals.  
- **Swin Transformer + ConvNeXt Backbone**: Leieves state-of-the-art computer vision models for EEG spectrogram feature extraction.  
- **Multi-Channel EEG Support**: Works with MNE-processed EEG datasets.  
- **High Accuracy**: Achieved >92% accuracy, reducing neurologists’ manual interpretation time by ~80%.  
- **Scalable**: Optimized pipelines for large datasets and efficient inference.  ```

## 🧠 Models Implemented  
1. **Novel Spatio-Temporal Model**  
   - Combines CNN layers for spatial encoding with temporal transformers for sequence modeling.  
   - Designed specifically for EEG spectrograms.  

2. **Swin Transformer**  
   - Hierarchical vision transformer with shifted windows.  
   - Strong performance on spectrogram classification.  

3. **ConvNeXt**  
   - Modernized CNN inspired by transformers.  
   - Efficient and scalable for large datasets.  

## ⚙️ Installation  
```bash
git clone https://github.com/your-username/eeg-classification.git
cd eeg-classification
pip install -r requirements.txt
```

## 📊 Dataset  
- **Source**: Processed EEG dataset with spectrograms (106k samples).  
- **Preprocessing**:  
  - Used **MNE** for EEG channel handling.  
  - Converted signals into spectrograms with SciPy + PIL.  
  - Normalized and split into train/val/test sets.  

## 🚀 Training  
Run training with desired model:  
```bash
python train.py --model spatio_temporal --epochs 50
python train.py --model swin --epochs 50
python train.py --model convnext --epochs 50
```

## 📈 Evaluation  
- Accuracy: **92%+** (Spatio-Temporal model).  
- Compared Swin and ConvNeXt backbones for performance and efficiency.  
- Metrics: Accuracy, F1-Score, Confusion Matrix.  

## 📑 Results  
| Model                 | Accuracy | F1-Score | Notes                         |  
|------------------------|----------|----------|-------------------------------|  
| Spatio-Temporal (ours) | **92.4%** | 91.8%   | Best overall performance      |  
| Swin Transformer       | 90.7%    | 89.9%   | Strong on spatial patterns    |  
| ConvNeXt               | 88.9%    | 87.5%   | Efficient, lower compute cost |  

## 📌 Applications  
- Automated seizure detection for hospitals.  
- Reducing neurologists’ manual diagnosis effort.  
- Foundation for real-time EEG monitoring systems.  

## 🛠️ Tech Stack  
- **Python**  
- **PyTorch**  
- **MNE, SciPy, PIL** for EEG preprocessing  
- **Transformers** (Swin, ConvNeXt)  
- **Matplotlib / Seaborn** for visualization  

## 👨‍💻 Contributors  
- **Sai Rajesh Velagana** – Research, Model Development, Evaluation  
