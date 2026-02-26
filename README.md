# BKAI ColonFormer - Colonoscopy Polyp Segmentation

## Overview

This is a colonoscopy polyp segmentation solution using the ColonFormer model. The project aims to detect and segment polyps in colonoscopy images, helping physicians in the diagnosis and treatment of colorectal diseases.

## 🎯 Objectives

- Detect and segment colorectal polyps from colonoscopy images
- Support physicians in diagnosing and treating colorectal pathologies
- Leverage modern Transformer architecture to improve accuracy

## 📊 Results

The model achieves:
- **Average Dice: 0.4505 ± 0.0392**
- **Average IoU: 0.4145 ± 0.0636**
- **Best Dice: 0.4870**
- **Precision: 0.8547**
- **Recall: 0.9047**

## 🏗️ Project Structure

```
BKAI_ColonFormer/
├── BKAI_ColonFormer.ipynb      # Main notebook
├── data/                        # Train/val/test data
│   ├── train/images/
│   ├── train/masks/
│   ├── val/images/
│   ├── val/masks/
│   └── test/test/
├── models/                      # Saved models
└── submission.csv              # Submission results
```

## 📦 Environment Requirements

### Main Libraries:
```
PyTorch >= 1.9.0
torchvision >= 0.10.0
numpy
pandas
opencv-python (cv2)
matplotlib
scikit-learn
albumentations
```

### Installation

```bash
pip install torch torchvision
pip install numpy pandas opencv-python matplotlib scikit-learn
pip install albumentations
```

### GPU Requirements
- Notebook is designed for Google Colab with T4 GPU
- Can run on other GPUs (RTX, A100, etc.)

## 🚀 How to Use

### 1. Prepare Data

Data should be organized as follows:
```
data/
├── train/
│   ├── images/      (original images)
│   └── masks/       (segmentation masks)
├── val/
│   ├── images/
│   └── masks/
└── test/
    └── test/        (test images)
```

### 2. Run Training

Open the `BKAI_ColonFormer.ipynb` notebook on Google Colab or Jupyter:

```python
# The notebook will automatically:
# 1. Load data
# 2. Initialize model
# 3. Train the model
# 4. Evaluate on validation set
# 5. Generate submission
```

### 3. Inference on Test Set

```python
model.eval()
pred = model(test_image)
pred_mask = pred.argmax(dim=1)
```

### 4. Generate Submission

The notebook automatically creates a `submission.csv` file containing predictions in RLE encoding format.

## 🔧 Main Components

### Model (ColonFormer)
- Transformer architecture designed for medical image segmentation
- Encoder-Decoder with attention mechanism
- Supports multi-class segmentation (Background, Polyp Type 1, Polyp Type 2)

### Data Augmentation
Using `albumentations` library:
- Random rotation, flip
- Color jittering
- Elastic transform
- Grid distortion

### Loss Function
- Dice Loss
- Cross Entropy Loss (can be weighted)

### Metrics
- Dice Score
- IoU (Intersection over Union)
- Precision & Recall

## 📈 Training Process

1. **Data Loading**: Load images and masks from directories
2. **Augmentation**: Apply data augmentation to training set
3. **Model Training**: Train with learning rate scheduler
4. **Validation**: Evaluate on validation set
5. **Prediction**: Inference on test set
6. **Post-processing**: Resize predictions to original image size

## 🎨 Key Features

✅ Multi-class segmentation (3 classes)  
✅ RLE encoding for submission  
✅ Automatic model checkpointing  
✅ Detailed evaluation metrics  
✅ Visualization support  
✅ GPU acceleration  

## 📝 Output Format

The `submission.csv` file has the following format:
```csv
id,predicted
image_id_1,<RLE_encoded_mask>
image_id_2,<RLE_encoded_mask>
...
```

RLE (Run Length Encoding) is a compression format widely used in Kaggle competitions.

## ⚙️ Hyperparameter Tuning

Hyperparameters that can be adjusted in the notebook:
- **Learning Rate**: Controls learning speed
- **Batch Size**: Batch size (depends on GPU memory)
- **Epochs**: Number of training epochs
- **Weight Decay**: Regularization parameter
- **Warmup Steps**: Number of warmup steps

## 🐛 Troubleshooting

### Out of Memory (OOM)
- Reduce batch size
- Decrease input image size

### Low Accuracy
- Increase number of epochs
- Adjust learning rate
- Check data augmentation settings

### Slow Training
- Use a more powerful GPU
- Reduce image resolution

## 📚 References

- ColonFormer paper: [Link if available]
- PyTorch Documentation: https://pytorch.org/docs/
- Segmentation Metrics: https://en.wikipedia.org/wiki/Dice_coefficient

## 👥 Contributing

If you want to improve the project:
1. Fork the repository
2. Create a branch for your feature
3. Commit your changes
4. Push and create a Pull Request

## 📄 License

[Specify license if applicable]

## 📧 Contact

[Add contact information if needed]

---

**Note**: This project is primarily designed to run on Google Colab. To run locally, you'll need a GPU and proper dependency installation.

## 🎓 Next Steps

1. Optimize hyperparameters
2. Try different data augmentation techniques
3. Ensemble with other models
4. Apply test-time augmentation (TTA)
5. Fine-tune with pre-trained models

**Happy Segmenting! 🏥**