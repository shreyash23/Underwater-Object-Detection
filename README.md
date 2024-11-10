# Underwater-object-detection

This is a pipeline for low-light underwater image enhancement and underwater object detection to be utilized for Remote Operated underwater Vehicles (ROVs). A comparitive study between RCNNs, ResNet and YOLO object detection algorithms was performed to choose the most suitable one for our pipeline. While the RCNN and ResNet algorithms were more accurate, YOLO produced object detection results 100-150% faster as compared to the two with only a small hit in accuracy. This makes YOLO perfect for pipelines involving real time object detection such as steering in ROVs. YOLOv5 and YOLOv8 were utilized in the pipeline. YOLOv5 and YOLOv8 are advanced models in the "You Only Look Once" (YOLO) series, known for their speed and accuracy in object detection tasks. YOLOv5, developed by Ultralytics, offers a lightweight, efficient architecture suited for real-time applications, achieving a mean Average Precision (mAP) of around 45.7% on the COCO dataset with YOLOv5x (its largest variant). It is optimized for ease of use, with pretrained models for various environments and rapid deployment capabilities. YOLOv8, the latest in the series, improves upon YOLOv5 by incorporating advanced features like a more flexible model structure and a new anchor-free detection head, leading to higher accuracy and faster inference times. YOLOv8 reaches an impressive mAP of around 50.2% on COCO with its largest model (YOLOv8x), offering improved precision while maintaining efficiency, making it highly suitable for real-time applications in computer vision.

![image](https://github.com/user-attachments/assets/7d110c2d-96f8-4531-8324-0aebdb28b3dd)

## Underwater image datasets for object detection model training

1. **Roboflow Aquarium Dataset**
   - **Total Images**: 638
   - **Categories**: Fish, Jellyfish, Penguin, Shark, Puffin, Stingray, Starfish
   - **Use**: Primarily for detecting various marine species in controlled underwater settings.

2. **Brackish Underwater Image Dataset**
   - **Total Images**: 14,674
   - **Categories**: Crab, Small Fish, Fish, Jellyfish, Starfish, Shrimp
   - **Use**: Focused on species in brackish (mixed salt and freshwater) environments, providing extensive examples of small and varied marine life.

3. **TrashCan1.0 Dataset**
   - **Total Images**: 7,212
   - **Main Categories**: Bio, Trash, Unknown
      - **Bio**: Includes Turtle, Squid, Lobster, Jellyfish, Stingray, Shrimp, Crawfish, Octopus, Shark, Shell, Crab, Starfish, Eel
      - **Trash**: Clothing, Pipe, Bottle, Bag, Snack Wrapper, Glove, Tire, Can, Cup, Container, Branch, Wreckage, Tarp, Box, Hose, Rope, Hay, Net, Paper, Bucket, Wire
   - **Use**: Designed for detecting and classifying waste and biological objects in underwater environments.

4. **Trash-ICRA19 Dataset**
   - **Total Images**: 5,700
   - **Categories**: Labeled with bounding boxes for trash, biological objects (plants, animals), and ROVs (Remotely Operated Vehicles)
   - **Use**: Useful for distinguishing trash from marine life and underwater equipment, promoting better object detection in complex underwater scenes.

5. **HICRD (Heron Island Coral Reef Dataset)**
   - **Total Images**: 8,003 (2,000 restored reference images and 6,003 original underwater images)
   - **Use**: Specialized in underwater image restoration, providing high-quality reference images for model training to improve clarity and color accuracy in murky underwater photos.

**Note**: The **Roboflow Aquarium** and **Brackish Underwater Image Dataset** were used in this work, providing essential data for recognizing marine species and understanding image characteristics in mixed aquatic environments.

## Underwater Image Datasets for image enhancement models

1. **LSUI (Large Scale Underwater Image Dataset)**
   - **Total Images**: 5,004 image pairs
   - **Characteristics**: Contains varied underwater scenes with different lighting, water types, and subjects, plus high-quality reference images.
   - **Use**: Provides a diverse range of underwater conditions for detailed visual analysis and enhancement tasks.

2. **EUVP (Enhancing Underwater Visual Perception)**
   - **Total Images**: 24,840 image pairs (good and bad quality)
   - **Use**: Supports models focused on enhancing underwater images, with paired data to improve visibility and perception in poor conditions.

3. **UIEB (Underwater Image Enhancement Benchmark)**
   - **Total Images**: 890 pairs of raw and reference images
   - **Use**: Used in this work for underwater image enhancement, serving as a benchmark for quality improvement and clarity in underwater imagery.

**Note**: The **UIEB dataset** was utilized in this work, offering raw and reference image pairs to benchmark image enhancement techniques, enabling the improvement of visual clarity in underwater scenes.

