# Train_Machine_Learning_Project
Video Processing for Train Bottom View
1. Environment
   - Mount the google drive to store input/output
     from google.colab import drive
     drive.mount('/content/drive')
2. Install dependencies
   !pip install opencv-python moviepy numpy tqdm ultralytics reportlab
3. Folder Structure
   train_project/
│
├── Raw_video/
│   └── DHN-wagon/
│       └── <input_train_video>.mp4
│
├── Processed_Video/      # auto-created for outputs
4. How to run the project
   This is divided into different steps :
   
   step 1 : setup environment and folders
   
   step 2 : split video into coaches , it saves clips as <train_number>_<i>.mp4
   
   step 3 : Extract frames per coach , it saves every 10 frames as <train_number>_<i>_<frameNo>.jpg
   
   step 4 : Detect doors using YOLO (Ultralytics) , labels as door/door open/door closed.
   
   step 5 : Select Minimal images as front,mid and rear.
   
   step 6 : Generate reports
   
5 . Limitations and assumptions :
   - Model Dependency: The script relies on a pre-trained model (model) and a function (detect_coach_boundaries) that are not included in the provided code. These are             essential for the script to function correctly.
   - Video Format: The script is specifically designed to work with .mp4 video files.
   - Frame Rate: The fps variable is an integer, so if the video's FPS is not an integer, it may be rounded.
   - Sampling Rate: The script processes only every 10th frame (frame_no % 10 == 0). This is an assumption that a 10% sample is sufficient for the analysis.
   
   

