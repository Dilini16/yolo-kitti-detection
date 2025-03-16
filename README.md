# YOLO KITTI Object Detection

This project trains a **YOLOv8** model on the **KITTI dataset** to detect **cars, pedestrians, and cyclists**. It uses the **Ultralytics YOLOv8** implementation for training and object detection.

##  Project Structure

```
.
├── kitti_dataset/
│    ├── images/      # Image files (e.g., .png)
│    └── labels/      # YOLO-formatted label files (.txt)
├── train_yolo_kitti.py  # Main script for training and detection
├── output/              # Output folder for results
└── README.md
```

## 🛠️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/yolo-kitti-detection.git
cd yolo-kitti-detection
```

### 2. Create and Activate Virtual Environment
```bash
python3 -m venv yolo_env
source yolo_env/bin/activate
```

### 3. Install Dependencies
```bash
pip install ultralytics matplotlib opencv-python
```

## 📊 KITTI Dataset Setup

1. Download the **KITTI Object Detection** dataset: [KITTI](https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=2d).
2. Organize your dataset as follows:

```
kitti_dataset/
├── images/
│    ├── 000001.png
│    └── ...
└── labels/
     ├── 000001.txt
     └── ...
```

Ensure the label files are in **YOLO format**:
```
<Class_ID> <x_center> <y_center> <width> <height>
```

### Class Mapping:
| Class         | ID |
|---------------|----|
| Car           | 0  |
| Pedestrian    | 1  |
| Cyclist       | 2  |

##  Run the Training Script

```bash
python train_yolo_kitti.py
```

##  Run Object Detection on a Video

To detect cars, pedestrians, and cyclists in a video:

1. Add your video to the project folder.
2. Update the `video_path` in `train_yolo_kitti.py`.

Run:

```bash
python train_yolo_kitti.py
```

The output video will be saved in the `output/` folder.

##  Contributing
Feel free to submit pull requests if you'd like to enhance the project.

## Contact
For questions, reach out via [GitHub Issues](https://github.com/your-username/yolo-kitti-detection/issues).

