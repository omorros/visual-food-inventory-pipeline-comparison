# VLM vs. YOLO vs. CNN: A Pipeline Comparison for Visual Food Inventory

BSc (Hons) Software Engineering — Anglia Ruskin University  
Final Year Dissertation | Supervisor: Dr Vitaliy Milke

Comparing three computer vision pipelines for automated food item 
recognition from fridge/shelf images, evaluated across degraded 
imaging conditions on a 14-class dataset.

## Experiments

| # | Repository | Description |
|---|-----------|-------------|
| 1 | [food-cv-exp1-cnn-comparison](https://github.com/omorros/food-cv-exp1-cnn-comparison) | CNN classifier selection — EfficientNetB0 vs ResNet-50 vs Custom CNN |
| 2 | [food-cv-exp2-pipeline-evaluation](https://github.com/omorros/food-cv-exp2-pipeline-evaluation) | 12-condition evaluation matrix comparing VLM, YOLO-14, and YOLO+CNN hybrid |
| 3 | [food-cv-exp3-mobile-deployment](https://github.com/omorros/food-cv-exp3-mobile-deployment) | SnapShelf — React Native + Expo app deploying the VLM pipeline |

## Key Findings

- VLM pipeline achieved F1 = 0.900 vs YOLO-14's F1 = 0.603
- VLM demonstrated significantly greater robustness to image degradation
- EfficientNetB0 selected as best CNN classifier (statistically equivalent to ResNet-50 at ~5× smaller size)