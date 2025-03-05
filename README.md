# Face-Recognition
we created an automated attendance system using face recognition
Face recognition is one of the most advanced biometric authentication techniques, used widely in security and automation. This project, Face Recognition-Based Student Attendance System, automates the attendance process using facial recognition technology. The system identifies students in real-time and marks their attendance, ensuring efficiency, accuracy, and security.

Project Overview
The proposed system captures students' faces through a webcam, compares them with pre-stored face data, and automatically registers attendance. Each student belongs to a particular section (e.g., Section A, Section B), and their attendance is recorded separately for better organization.

Technology Stack
Programming Language: Python
Libraries Used:
face_recognition – For face detection and recognition
OpenCV – For real-time image processing
NumPy – For handling numerical operations
CSV – For storing attendance records
OS & DateTime – For managing files and timestamps

Project Workflow
Image Collection: The system stores pre-collected images of students classified into sections (e.g., aiml_a, aiml_b).
Face Encoding: Each student’s face is encoded and stored for comparison.
Live Video Capture: A webcam continuously captures video frames.
Face Detection: The system detects faces in real time using OpenCV.
Face Recognition: Encoded images are compared with live captures to identify students.
Attendance Logging: If a match is found, attendance is marked in a CSV file corresponding to the student’s section.
Display Results: Recognized students' names are displayed on the screen with a real-time bounding box.

Implementation Details
1. Image Collection and Preprocessing
Student images are stored in two folders: aiml_a and aiml_b.
Each image is converted to RGB format and encoded using face_recognition.face_encodings().
2. Face Recognition & Attendance Marking
The webcam captures live video.
Face locations and encodings are extracted from frames.
Recognized faces are matched against the stored dataset using Euclidean distance.
If a match is found, attendance is recorded in YYYY-MM-DD_aiml_a.csv or YYYY-MM-DD_aiml_b.csv.
3. CSV File Handling
The system maintains a separate attendance record for each section.
If a student is recognized for the first time in a session, their name and timestamp are logged.
Duplicate attendance is prevented by tracking already recognized students.
