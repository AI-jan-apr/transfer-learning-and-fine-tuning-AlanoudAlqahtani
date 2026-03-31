# EfficientNet Transfer Learning – Food Classification

## Overview
This project applies transfer learning using EfficientNetB0 on the Food-11 dataset. Two approaches were implemented: feature extraction and fine-tuning.

## Experiments

### 1. Feature Extraction
- Base model frozen
- Only classification head trained
- Fast and stable training

### 2. Fine-tuning
- Last layers unfrozen
- Lower learning rate used
- Improved performance over feature extraction

## Results

| Experiment | Test Accuracy | Test Loss |
|-----------|-------------|----------|
| Feature Extraction | 0.8883 | 0.3227 |
| Fine-tuning | 0.9057 | 0.2863 |

## Observations

- Fine-tuning improved accuracy and reduced loss
- Pretrained EfficientNet features generalize well
- No strong overfitting observed
- Some classes remain harder to distinguish

## Conclusion

Fine-tuning provides better performance than feature extraction, though both approaches are effective. EfficientNetB0 is well-suited for transfer learning tasks.

## Files

- Notebook: training and evaluation
- Model: `efficientnet_food_model.keras`
- Weights: `efficientnet.weights.h5`
- Results: `results_summary.json`
