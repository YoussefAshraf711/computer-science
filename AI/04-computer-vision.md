[العربي](./04-computer-vision_ar.md)

# <a name="-4-computer-vision"></a>🤖 Chapter 4: Computer Vision (CV)

## 1. What is it?
Computer Vision enables machines to extract meaningful information from images and video — including classification, detection, segmentation, and tracking.

## 2. What does the specialist do?
A CV specialist acquires and annotates visual data, trains and fine-tunes models (CNNs, vision transformers), optimizes inference for latency and memory, and integrates models into production systems.

## 3. Sub-domains
- Image classification  
- Object detection  
- Semantic and instance segmentation  
- Pose estimation and tracking  
- 3D vision and depth estimation  
- Video understanding and action recognition

## 4. Expanded Key Concepts
- Convolutions, receptive fields, feature pyramids  
- Data augmentation and domain adaptation  
- Detection metrics: IoU, mAP; segmentation metrics: pixel accuracy, IoU  
- Anchor mechanisms, NMS, and multi-scale features

## 5. Expanded Tools & Technologies
- PyTorch, torchvision, Detectron2, MMDetection, YOLO implementations  
- Annotation tools: CVAT, LabelImg; datasets: COCO, ImageNet, Pascal VOC  
- Inference acceleration: TensorRT, OpenVINO, ONNX Runtime

## 6. In-Depth Workflow (example: industrial defect detection)
1. Collect balanced dataset including faulty cases.  
2. Annotate images and export in COCO format.  
3. Train with strong augmentations and a robust backbone.  
4. Optimize with pruning/quantization; measure latency on target hardware.  
5. Deploy to edge or cloud with monitoring for false positives.

## 7. Common Job Roles
- Computer Vision Engineer  
- Perception Engineer  
- Image Processing Engineer

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Augmentation`** | The process of creating new training data by modifying existing data. |
| **`Bounding Box`** | A rectangle drawn around an object in an image. |
| **`COCO`** | Common Objects in Context, a large-scale object detection, segmentation, and captioning dataset. |
| **`Detection`** | The task of identifying the presence and location of objects in an image. |
| **`IoU`** | Intersection over Union, a metric for evaluating the accuracy of an object detector. |
| **`mAP`** | mean Average Precision, a common metric for evaluating the performance of object detection models. |
| **`NMS`** | Non-Maximum Suppression, a technique used to select the best bounding box from a set of overlapping bounding boxes. |
| **`OCR`** | Optical Character Recognition, the task of converting images of text into machine-readable text. |
| **`Pretrained`** | A model that has been trained on a large dataset and can be used as a starting point for a new task. |
| **`Segmentation`** | The task of partitioning an image into multiple segments. |
| **`YOLO`** | You Only Look Once, a real-time object detection system. |

</details>

[⬆️ Back to Table of Contents](./README.md)
