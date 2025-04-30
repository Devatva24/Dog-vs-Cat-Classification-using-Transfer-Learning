<h1>Dog vs Cat Image Classification using MobileNet</h1>

<h2>📌 Objective</h2>
<p>To build a deep learning model that accurately classifies images of dogs and cats using transfer learning with the MobileNet architecture.</p>

<hr>

<h2>🛑 Problem Statement</h2>
<p>Manually distinguishing between dog and cat images at scale can be inefficient. This project aims to automate the classification using a lightweight and accurate deep learning model, optimized through transfer learning.</p>

<hr>

<h2>📊 Dataset</h2>
<ul>
  <li><b>Source:</b> <a href="https://www.kaggle.com/c/dogs-vs-cats/data" target="_blank">Kaggle - Dogs vs Cats</a></li>
  <li><b>Classes:</b> Dog, Cat</li>
  <li><b>Data Format:</b> JPEG images (~25,000 total)</li>
</ul>

<hr>

<h2>⚙️ Methodology</h2>

<h3>1. Data Preparation</h3>
<ul>
  <li>Resize images to 224x224 (MobileNet input size)</li>
  <li>Data augmentation (rotation, zoom, flip) for better generalization</li>
  <li>Split into training and validation sets</li>
</ul>

<h3>2. Model Architecture</h3>
<ul>
  <li>Base Model: <b>MobileNet</b> (pretrained on ImageNet)</li>
  <li>Custom top layers:
    <ul>
      <li>GlobalAveragePooling2D</li>
      <li>Dense (ReLU)</li>
      <li>Dropout</li>
      <li>Final Dense (Sigmoid for binary classification)</li>
    </ul>
  </li>
  <li>Frozen base layers during initial training</li>
</ul>

<h3>3. Training</h3>
<ul>
  <li>Optimizer: Adam</li>
  <li>Loss: Binary Crossentropy</li>
  <li>Metrics: Accuracy</li>
  <li>Trained for 5–10 epochs with fine-tuning of top layers</li>
</ul>

<h3>4. Evaluation</h3>
<ul>
  <li>Validation Accuracy: ~95%+</li>
  <li>Confusion matrix and classification report for detailed metrics</li>
</ul>

<hr>

<h2>🛠️ Technologies Used</h2>
<ul>
  <li>Python</li>
  <li>TensorFlow / Keras</li>
  <li>OpenCV / Pillow</li>
  <li>NumPy, Pandas</li>
  <li>Matplotlib for visualization</li>
</ul>

<hr>

<h2>✅ Results</h2>
<ul>
  <li>Achieved high accuracy using MobileNet with minimal training time</li>
  <li>Efficient model size suitable for deployment on low-resource devices</li>
</ul>

<hr>

<h2>📝 Conclusion</h2>
<p>This project showcases how transfer learning with MobileNet can be effectively used to classify images of dogs and cats, offering a lightweight and accurate solution ideal for real-world deployment.</p>

<hr>

<h2>🔮 Future Enhancements</h2>
<ul>
  <li>Implement a web interface using Streamlit or Flask</li>
  <li>Deploy model to mobile or edge devices using TensorFlow Lite</li>
  <li>Extend to multi-class animal classification</li>
</ul>
