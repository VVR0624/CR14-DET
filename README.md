# CR14-DET: A Comprehensive Dataset for Industrial Steel Surface Defect Detection

## 📖 Introduction
**CR14-DET** is a high-quality industrial surface defect dataset collected from a real-world steel manufacturing facility in China. It is designed to support research in object detection, semi-supervised learning, and open-set recognition within complex industrial environments. The dataset specifically captures defects on cold-rolled steel strips, which are often characterized by low contrast and intricate background textures.

## 📊 Dataset Statistics
The dataset contains a total of **5,074 images** and **10,594 annotated instances**, covering 14 distinct defect categories. All images are provided in `.jpg` format.

| Class ID | Defect Category | Images | Instances | Description |
| :---: | :--- | :---: | :---: | :--- |
| `0` | **Linear** | 250 | 405 | Scratches caused by rollers or structural objects; straight and continuous. |
| `1` | **Macular** | 382 | 596 | Yellow or white spreading patches; blooming on the board surface. |
| `2` | **Pit** | 583 | 1,435 | Depressions or gravures of a certain depth on the surface. |
| `3` | **Scrapes** | 635 | 838 | Wide-area friction marks or abrasions. |
| `4` | **Scabs** | 654 | 1,586 | Metallic protrusions or crust-like scale patches. |
| `5` | **Contusion** | 277 | 813 | Bruise-like impact marks from mechanical collisions. |
| `6` | **Edge Cracks** | 129 | 166 | Fractures or splits occurring at the strip edges. |
| `7` | **Heat Scratches** | 140 | 783 | Scratches with thermal discoloration or heat traces. |
| `8` | **Impurities Pressed-in** | 208 | 553 | Non-metallic foreign matter pressed into the metal during rolling. |
| `9` | **Protective Slag** | 470 | 694 | Residue from casting powder or slag on the surface. |
| `10` | **Rolled-in Scale** | 616 | 957 | Oxide scale rolled tightly into the steel surface. |
| `11` | **Dark Spots** | 405 | 853 | Periodic dark or black spots. |
| `12` | **Black Line** | 177 | 654 | Dark, continuous, or semi-continuous linear marks. |
| `13` | **Bright Bands** | 148 | 261 | Abnormally bright streaks of varying widths. |

## 📁 Data Format & Directory Structure

Annotations are provided in standard **YOLO text format**. Each image has a corresponding `.txt` file containing the bounding box coordinates.

### Annotation Format
Each line in a `.txt` label file corresponds to one defect instance:
`<class_id> <x_center> <y_center> <width> <height>`

*(Note: `x_center`, `y_center`, `width`, and `height` are normalized between 0 and 1 relative to the image dimensions.)*

### Directory Structure
The dataset is provided as a raw collection of images and labels without pre-defined train/test splits. You can partition the data according to your specific experimental needs:
```text
CR14-DET/
├── images/       # Contains all 5,074 .jpg images
└── labels/       # Contains all 5,074 YOLO format .txt annotations
