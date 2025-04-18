# Ai-Based_Attendance_system
AI-BASED ATTENDANCE SYSTEM
Project Title: AI-Based Attendance System using Face Recognition
Project Overview:
This project is a real-time face recognition-based attendance system that automatically identifies individuals using a webcam and marks their attendance. It utilizes computer vision and machine learning techniques to detect and recognize faces from a dataset, record attendance, and store the data with timestamps and images. The system also provides a user-friendly graphical interface using Tkinter for starting and stopping attendance collection.
Technologies and Libraries Used:
Python – Programming language used for building the entire application.


OpenCV – Used for video capture and image processing.


face_recognition – A powerful library built on top of dlib for face detection and recognition.


dlib – For deep learning-based face encoding.


NumPy – For numerical operations.


pandas – For creating and exporting attendance records in CSV format.


Tkinter – Python's standard GUI library for creating the graphical user interface.


Pillow (PIL) – For handling image conversions compatible with Tkinter.


Step-by-step Explanation:
Face Encoding Preparation:
 The system starts by encoding known faces from the 'dataset' directory. Each sub-folder in this directory is named after a person and contains images of their face. The face_recognition library is used to extract and store face encodings (numerical representations of facial features).


GUI Setup:
 A GUI window is created using Tkinter, which includes a video display area and buttons to start and stop attendance tracking.


Video Capture and Face Detection:
 When the user clicks "Start Attendance", the system accesses the webcam using OpenCV and continuously captures frames. Each frame is converted to RGB and passed to the face_recognition library to locate and encode any detected faces.


Face Matching and Attendance Marking:
 For each detected face, the system compares it to known encodings using face_recognition.compare_faces(). If a match is found, the corresponding person's name is marked present, along with the current timestamp. A photo of the detected face is also saved for record-keeping.


Attendance Logging:
 Attendance data is saved in a dictionary and later exported to a CSV file when the user stops the process. Each entry includes the name, date, time, and a clickable hyperlink to the saved face image.


Visualization and Notifications:
 The GUI displays the video stream with rectangles around recognized faces and their names. A popup message is shown when someone’s attendance is successfully marked or saved.


Output Files:
 Attendance is saved in CSV format with filenames based on date and time, and face images are stored in a separate folder with corresponding timestamps.


Outcome:
The final application is capable of accurately recognizing individuals in real time and automating the attendance process with time and photo records. It demonstrates the integration of machine learning, computer vision, GUI programming, and file handling, making it a practical solution for educational or organizational use.

