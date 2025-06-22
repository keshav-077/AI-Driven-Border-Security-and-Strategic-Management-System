  
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">

</head>
<body>

  <h1>🔐 AI-Driven Border Security & Strategic Surveillance System</h1>
  <p>
    In this project we introduced an AI-Driven Border Security System designed to enhance real-time surveillance and threat detection. The system integrates cutting-edge deep learning models and classical computer vision techniques to ensure robust performance in complex border environments.  

YOLOv8 serves as the core object detection model, specializing in identifying and classifying critical entities such as individuals and weapons from live video streams with high efficiency. Haar Cascade is employed for face detection, while Local Binary Pattern Histogram (LBPH) is utilized for facial recognition, ensuring accurate identification of individuals. Additionally, OSNet-based re-identification is incorporated to track and identify individuals across multiple cameras, enabling seamless monitoring even in multi-camera setups.  

The models are trained and fine-tuned using a custom-curated dataset, annotated through Roboflow, to achieve optimal performance in real-world scenarios. The system integrates with IP Webcam, enabling real-time multi-camera feeds to provide comprehensive border coverage.  

Performance evaluation employs metrics like precision, recall, and F1-score, along with detailed precision-recall curves and confusion matrices. Results indicate outstanding accuracy and reliability, showcasing the system’s capability to detect, classify, and re-identify individuals effectively.  

Future enhancements will focus on extending the system's capabilities to include behavior analysis and anomaly detection, further solidifying its role as an indispensable tool for border security and national safety.
  </p>

  <div class="section">
    <h2>📁 Dataset Preparation</h2>
    <ul>
      <li><strong>Weapon Detection Dataset:</strong> 4,200 images (Pistols, Rifles, Knives) from Roboflow</li>
      <li><strong>Face Classification Dataset:</strong> 1,000 images (Soldier vs Terrorist), custom created</li>
      <li><strong>Person Detection Dataset:</strong> 6,000 person images from Roboflow</li>
    </ul>
    <p>All datasets are labeled using YOLO format and augmented with rotation, flipping, and brightness changes.</p>
  </div>

  <div class="section">
    <h2>⚙️ Preprocessing & Model Training</h2>
    <ul>
      <li>Images resized, normalized, and augmented using YOLO’s preprocessing pipeline</li>
      <li><strong>Weapon Detection:</strong> YOLOv8 trained for 40 epochs using SGD with cosine annealing</li>
      <li><strong>Face Classification:</strong> CNN with 3 conv layers + FC layers, 85–90% accuracy</li>
      <li><strong>Person Detection:</strong> YOLOv8 trained for multi-camera person tracking</li>
    </ul>
  </div>

  <div class="section">
    <h2>📸 System Architecture</h2>
    <p>Below is the high-level architecture integrating multi-camera inputs, object detection, and classification logic.</p>
    <img src="assets/architecture.png" alt="System Architecture Diagram">
  </div>

  <div class="section">
    <h2>🎯 Key Features</h2>
    <ul>
      <li>📷 <strong>Multi-Camera Support:</strong> IP/Webcam feed integration</li>
      <li>🔫 <strong>Weapon Detection:</strong> Pistols, rifles, knives</li>
      <li>🧍 <strong>Person Tracking:</strong> Detects and tracks individuals</li>
      <li>🆔 <strong>Facial Classification:</strong> Labels individuals as Soldier or Terrorist</li>
      <li>🚨 <strong>Real-time Alert System:</strong> Ready for SMS/Email integration</li>
    </ul>
  </div>

  <div class="section">
    <h2>📊 Results & Evaluation</h2>
    <h3>1. Weapon Detection</h3>
    <ul>
      <li>Precision: 92%</li>
      <li>Recall: 90%</li>
      <li>F1-Score: 91%</li>
    </ul>
    <img src="assets/weapon_precision.png" alt="Weapon Detection - Precision">
    <img src="assets/weapon_recall.png" alt="Weapon Detection - Recall">
    <img src="assets/weapon_f1score.png" alt="Weapon Detection - F1 Score">
    <img src="assets/weapon_confusion_matrix.png" alt="Weapon Detection - Confusion Matrix">
    <img src="assets/weapon_loss_curve.png" alt="Weapon Detection - Training Loss Curve">
    <img src="assets/weapon_pr_curve.png" alt="Weapon Detection - PR Curve">
    <h3>2. Person Detection</h3>
    <ul>
      <li>Precision: 91%</li>
      <li>Recall: 89%</li>
      <li>F1-Score: 90%</li>
    </ul>
    <img src="assets/person_precision.png" alt="Person Detection - Precision">
    <img src="assets/person_recall.png" alt="Person Detection - Recall">
    <img src="assets/person_f1score.png" alt="Person Detection - F1 Score">
    <img src="assets/person_confusion_matrix.png" alt="Person Detection - Confusion Matrix">
    <img src="assets/person_loss_curve.png" alt="Person Detection - Training Loss Curve">
    <img src="assets/person_pr_curve.png" alt="Person Detection - PR Curve">
  </div>

  <div class="section">
    <h2>📈 Comparative Analysis</h2>
    <ul>
      <li><strong>YOLOv8 outperformed Faster R-CNN</strong> in speed and accuracy</li>
      <li>Maintained 30 FPS on IP webcam inputs</li>
      <li>Generalized well across varying environments (high mAP and low loss)</li>
    </ul>
  </div>

  <div class="section">
    <h2>🚀 Deployment Highlights</h2>
    <ul>
      <li>Real-time prototype tested and demonstrated</li>
      <li>Scalable to wider zones via multicam support</li>
      <li>Low-latency processing with CUDA on NVIDIA RTX 3060</li>
    </ul>
  </div>

  <div class="section">
    <h2>🛠 Tech Stack</h2>
    <ul>
      <li>Python, OpenCV, YOLOv8, CNN, ReLU, Roboflow</li>
      <li>Training accelerated on RTX 3060 GPU</li>
      <li>Real-time camera integration with Flask/OpenCV</li>
    </ul>
  </div>

  <div class="section">
    <h2>🔮 Future Scope</h2>
    <ul>
      <li>Add license plate & vehicle detection</li>
      <li>Integrate face recognition with national databases</li>
      <li>Cloud-based notification system with real-time dashboard</li>
    </ul>
  </div>

  <div class="section">
    <h2>📬 Contact</h2>
    <p>For questions or collaboration, reach out via <a href="https://github.com/keshav-077">GitHub</a> or email.</p>
  </div>

</body>
</html>
