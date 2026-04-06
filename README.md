<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>YOLO Vehicle Detection, Tracking and Counting</title>

<style>
body{
    font-family: Arial, Helvetica, sans-serif;
    margin:40px;
    background:#f4f6f8;
    line-height:1.7;
}

.container{
    background:white;
    padding:30px;
    border-radius:10px;
    box-shadow:0px 0px 15px rgba(0,0,0,0.1);
}

h1,h2{
    color:#0a4d8c;
}

code{
    background:#eee;
    padding:3px 6px;
    border-radius:5px;
}

.section{
    margin-bottom:25px;
}

.footer{
    margin-top:40px;
    text-align:center;
    font-size:14px;
    color:gray;
}
</style>
</head>

<body>

<div class="container">

<h1>🚦 Vehicle Detection, Tracking and Counting using YOLO</h1>

<div class="section">
<h2>📌 Project Information</h2>

<p><b>Student Name:</b> Siri Vennela Amaragani</p>
<p><b>Roll Number:</b> 160723748301</p>
<p><b>College:</b> Methodist College of Engineering and Technology</p>
<p><b>Department:</b> Computer Science Engineering (AI & ML)</p>
<p><b>Project Type:</b> Computer Vision / Artificial Intelligence</p>
</div>

<hr>

<div class="section">
<h2>📖 Project Overview</h2>

<p>
This project implements an intelligent traffic monitoring system using
<strong>YOLO Object Detection</strong> and <strong>Object Tracking</strong>.
The system detects vehicles from video input, tracks each vehicle using
unique IDs, and counts vehicles automatically when they cross a virtual line.
</p>

<p>
The solution simulates a real-world smart city traffic analytics system used in:
</p>

<ul>
<li>Smart Traffic Management</li>
<li>Automated Toll Systems</li>
<li>Urban Traffic Analysis</li>
<li>Surveillance and Monitoring</li>
</ul>
</div>

<hr>

<div class="section">
<h2>📥 Inputs</h2>

<ul>
<li>Traffic video file (.mp4)</li>
<li>Pretrained YOLO model weights (<code>yolo11l.pt</code>)</li>
<li>Vehicle class filters (car, bus, truck, motorcycle, etc.)</li>
</ul>

<p><b>Input Source:</b> Recorded traffic surveillance video.</p>
</div>

<hr>

<div class="section">
<h2>📤 Outputs</h2>

<ul>
<li>Real-time vehicle detection bounding boxes</li>
<li>Unique tracking IDs assigned to each vehicle</li>
<li>Vehicle counting when crossing detection line</li>
<li>Class-wise vehicle statistics displayed on screen</li>
<li>Annotated output video frames</li>
</ul>
</div>

<hr>

<div class="section">
<h2>📊 Dataset Used</h2>

<p>
The detection model is pretrained on the <strong>COCO Dataset (Common Objects in Context)</strong>.
</p>

<ul>
<li>80 object categories</li>
<li>Includes vehicles such as:
    <ul>
        <li>Car</li>
        <li>Bus</li>
        <li>Truck</li>
        <li>Motorcycle</li>
        <li>Bicycle</li>
    </ul>
</li>
</ul>

<p>
The testing dataset consists of real-world traffic videos used for inference and evaluation.
</p>
</div>

<hr>

<div class="section">
<h2>🤖 Algorithm Used</h2>

<h3>1. YOLO (You Only Look Once)</h3>
<p>
YOLO is a deep learning-based object detection algorithm that detects multiple objects
in a single forward pass of a neural network.
</p>

<ul>
<li>Single-stage detector</li>
<li>Real-time detection capability</li>
<li>High accuracy and speed</li>
</ul>

<h3>2. Object Tracking Algorithm</h3>

<p>
YOLO tracking mode uses tracking algorithms such as:
</p>

<ul>
<li>ByteTrack / BoT-SORT tracking</li>
<li>Assigns persistent IDs to detected objects</li>
<li>Maintains identity across frames</li>
</ul>

<h3>3. Line Crossing Counting Logic</h3>

<ul>
<li>Center point of bounding box is calculated</li>
<li>Virtual line drawn across frame</li>
<li>Vehicle counted when crossing line once</li>
<li>Duplicate counting prevented using ID tracking</li>
</ul>

</div>

<hr>

<div class="section">
<h2>🧠 YOLO Version Used</h2>

<ul>
<li><b>Model:</b> YOLOv11 Large (<code>yolo11l.pt</code>)</li>
<li><b>Framework:</b> Ultralytics YOLO</li>
<li><b>Language:</b> Python</li>
<li><b>Libraries:</b>
    <ul>
        <li>OpenCV</li>
        <li>Ultralytics</li>
        <li>PIL</li>
        <li>NumPy</li>
    </ul>
</li>
</ul>
</div>

<hr>

<div class="section">
<h2>⚙️ System Workflow</h2>

<ol>
<li>Load YOLO pretrained model</li>
<li>Read video frame-by-frame using OpenCV</li>
<li>Detect vehicles using YOLO</li>
<li>Track vehicles with unique IDs</li>
<li>Draw bounding boxes and labels</li>
<li>Check if vehicle crosses counting line</li>
<li>Update vehicle counts</li>
<li>Display processed output</li>
</ol>

</div>

<hr>

<div class="section">
<h2>✅ Results</h2>

<ul>
<li>Accurate multi-vehicle detection achieved</li>
<li>Real-time object tracking implemented</li>
<li>Class-wise vehicle counting successful</li>
<li>Minimal duplicate counting due to ID persistence</li>
</ul>

</div>

<hr>

<div class="section">
<h2>📌 Conclusion</h2>

<p>
The project successfully demonstrates a real-time intelligent vehicle
monitoring system using modern computer vision techniques.
By integrating YOLO detection with object tracking, the system efficiently
detects, tracks, and counts vehicles automatically.
</p>

<p>
This approach can be extended for smart city infrastructure, traffic congestion
analysis, automated surveillance systems, and AI-powered transportation analytics.
</p>

</div>

<hr>

<div class="section">
<h2>🚀 Future Enhancements</h2>

<ul>
<li>Vehicle speed estimation</li>
<li>Direction-based counting (IN/OUT)</li>
<li>Cloud dashboard analytics</li>
<li>Live CCTV stream integration</li>
<li>Traffic density prediction using AI</li>
</ul>
</div>

<div class="footer">
<p>© 2026 | Siri Vennela Amaragani | Methodist College of Engineering and Technology</p>
</div>

</div>

</body>
</html>
