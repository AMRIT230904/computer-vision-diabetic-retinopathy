Based on the research paper “Deep Learning-Based Hemorrhage Detection for Diabetic Retinopathy Screening” (Scientific Reports, 2023).

Focuses on automatic detection of hemorrhages (HEs), an early pathological sign of Diabetic Retinopathy (DR)
Aims to develop a computer-aided diagnosis (CAD) system to assist ophthalmologists and reduce manual screening time.

Preprocessing Stage:

Contrast enhancement using CLAHE.
Adaptive gamma correction based on gradient information to handle non-uniform illumination.
Image sharpening to improve edge clarity.

Candidate Localization:
Gaussian matched filtering to enhance dark red lesions.
Entropy-based thresholding to remove weak responses.
Morphological operations to isolate potential hemorrhage seed points.

Segmentation:

Smart Window-Based Adaptive Thresholding (SWAT).
Handles varying lesion sizes and intensity variations
Removes irrelevant background regions.

Proposed Deep Model – HemNet
Shallow convolutional neural network (19 layers).
Uses RGB (Green), HSV (Value), and CIE Lab (Luminance) channels.
Designed to efficiently classify hemorrhage vs non-hemorrhage regions.

Datasets Used:
DIARETDB1
DIARETDB0

Evaluation Metrics:
Sensitivity (SE)
Specificity (SP)
Precision (P)
Accuracy (AC)
PR Curve and ROC Curve (AUC)

Key Findings:
HemNet achieved competitive performance compared to LeNet-5, AlexNet, ResNet50, and VGG-16.
Reduced training time significantly compared to deeper networks.
Increasing network depth does not guarantee better performance.
Proper architecture design and parameter selection are critical for optimal results.
Demonstrates that a lightweight and well-designed CNN can effectively detect hemorrhages even with limited training data.
