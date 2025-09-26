🚄 Train Wagon Analysis and Reporting System
Project Summary
This project is a complete, end-to-end computer vision pipeline for analyzing train videos. Built to process a side-view recording of a train, the system automatically detects and counts individual wagons and engines. It then segments the raw video into smaller clips, extracts a minimal set of frames for a full-length view of each coach, and performs object detection to identify and report on the status of doors.

The final output is a structured directory of all processed files and a professional, multi-page PDF report that summarizes the analysis and provides detailed information for each wagon. This project demonstrates skills in video processing, object detection, and automated report generation.

✨ Features
Automated Video Processing: The system uses frame differencing to reliably detect the gaps between train coaches, enabling accurate counting and video segmentation.

Intelligent Frame Extraction: It employs a feature-based similarity algorithm (using ORB/SIFT) to select a minimal set of images that provide full visual coverage of each wagon, eliminating redundant frames.

Conceptual Object Detection: The pipeline is architecturally designed to integrate a YOLOv8 model for detecting key components like doors. It also provides a framework for classifying the door's state (open or closed).

Comprehensive Reporting: It automatically generates a professional, paginated PDF report that includes a project summary, overall wagon and engine counts, and a dedicated page for each wagon with its video path and annotated images.

Organized Output: All generated video clips, annotated images, and the final report are saved in a clean, logical folder structure for easy navigation and review.

🚀 Getting Started
This project is designed to be executed within a Google Colab environment, which provides all necessary dependencies and GPU support.

Open a New Google Colab Notebook: Go to colab.research.google.com and create a new notebook.

Copy and Paste the Code: Copy the code provided in the four main blocks and paste them into separate cells in your notebook.

Run Sequentially: Execute each cell from top to bottom. The first cell will handle all library installations and video downloads.

Download Your Output: Upon successful completion, a file named Processed_Video.zip will appear in the Colab file explorer on the left sidebar. Download this file to access all the processed videos, images, and the final report.

📦 Output Structure
After running the script, your output folder will have the following structure:

.
└── Processed_Video/
    ├── individual_coaches/
    │   ├── 12309_engine_1/
    │   │   ├── 12309_engine_1.mp4
    │   │   └── extracted_frames/
    │   │       ├── 12309_engine_1_1.jpg
    │   │       └── ..._annotated.jpg
    │   ├── 12309_wagon_1/
    │   │   ├── 12309_wagon_1.mp4
    │   │   └── extracted_frames/
    │   │       ├── 12309_wagon_1_1.jpg
    │   │       └── ..._annotated.jpg
    │   └── ...
    └── Final Report---Assignment Submission/
        └── 12309_Train_Analysis_Report.pdf
