# captcha-solver-cnn-bilstm
An end-to-end deep learning framework using a hybrid CNN-BiLSTM-CTC architecture to decode distorted alphanumeric CAPTCHAs without manual segmentation, featuring a real-time Flask web interface.

**CAPTCHA Solver: Automated Recognition via Deep Learning**

**Overview**

This project presents an advanced deep learning framework for automated CAPTCHA recognition designed to decode distorted alphanumeric text images. Traditional Optical Character Recognition (OCR) often fails due to complex visual conditions like overlapping characters, irregular spacing, and background noise. This system overcomes these limitations by integrating Convolutional Neural Networks (CNNs) for spatial feature extraction and Bidirectional Long Short-Term Memory (BiLSTM) for sequential modeling.

**Problem Statement**

Modern CAPTCHA systems utilize intentional text distortion and noise patterns to distinguish humans from bots, creating a significant challenge for standard automation. Conventional methods relying on handcrafted preprocessing struggle to maintain accuracy under these adversarial designs. This project addresses the need for a robust, intelligent system that can recognize characters directly from raw, noisy images.

**Key Features**

• Segmentation-Free Recognition: The model predicts the complete CAPTCHA sequence directly, avoiding errors typically caused by manual character segmentation.

• Sequential Modeling: Utilizes BiLSTM layers to capture context and relationships between characters, which is essential for decoding connected or overlapping text.

• CTC-Based Decoding: Implements Connectionist Temporal Classification (CTC) to handle variable-length outputs and align input sequences with text labels efficiently.

• Real-Time Deployment: Integrated into a Flask web application, allowing users to upload images and receive instant predictions with confidence scores.

• Robustness: Engineered to handle various fonts, background interference, and heavy deformations.

**System Architecture**

The system follows a modular pipeline: Preprocessing → Feature Extraction → Sequence Modeling → Decoding.

1. CNN Backbone: Learns hierarchical spatial features such as edges, curves, and textures.
 
2. BiLSTM Layers: Processes feature sequences in both forward and backward directions to understand temporal dependencies.
 
3. CTC Loss: Align predicted sequences with ground truth without requiring explicit character-level labels.
   
4. Flask Interface: Provides an interactive UI for image uploads and result visualization.
   
**Technical Stack**

• Deep Learning: TensorFlow, Keras

• Computer Vision: OpenCV, Pillow (PIL)

• Web Framework: Flask

• Data Handling: NumPy

• Development Environment: VS Code

**Performance**

The model was trained on a custom dataset featuring diverse fonts and noise levels.
• Training Accuracy: The system achieved a high recognition reliability through careful tuning of hyperparameters.

• Evaluation Accuracy: In testing scenarios, the model demonstrated a high success rate, with specific evaluations reaching 95.28% accuracy
