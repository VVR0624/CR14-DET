# CR14-DET: A Comprehensive Dataset for Industrial Steel Surface Defect Detection

## 📖 Introduction
**CR14-DET** is a high-quality industrial surface defect dataset collected from a real-world steel manufacturing facility in China. It is designed to support research in object detection, semi-supervised learning, and open-set recognition within complex industrial environments. The dataset specifically captures defects on cold-rolled steel strips, which are often characterized by low contrast and intricate background textures.

## 📊 Dataset Statistics
The dataset contains a total of **5,074 images** and **10,594 annotated instances**, covering 14 distinct defect categories. All images are provided in `.jpg` format.

| Class ID | Defect Category | Images | Instances | Description |
| :---: | :--- | :---: | :---: | :--- |
| `0` | **Linear（Ln）** | 250 | 405 | Thin vertical low-contrast streaks. |
| `1` | **Macular（Ma）** | 382 | 596 | Blurred hazy dark surface patches. |
| `2` | **Pit（Pt）** | 583 | 1,435 | Deep localized tiny surface pits. |
| `3` | **Scrapes（Sr）** | 635 | 838 | Horizontal friction induced scratches. |
| `4` | **Scabs（Sb）** | 654 | 1,586 | Thick crust-like protruding scales. |
| `5` | **Contusion（Cn）** | 277 | 813 | Shallow surface indentation marks. |
| `6` | **Edge Cracks（Ec）** | 129 | 166 | Irregular tears at strip boundaries. |
| `7` | **Heat Scratches（Hs）** | 140 | 783 | Parallel thermal friction lines. |
| `8` | **Impurities Pressed-in（Ip）** | 208 | 553 | Embedded small dark foreign particles. |
| `9` | **Protective Slag（Ps）** | 470 | 694 | Irregular dark slag residue spots. |
| `10` | **Rolled-in Scale（Rs）** | 616 | 957 | Rough oxide scale pressed surface. |
| `11` | **Dark Spots（Ds）** | 405 | 853 | Localized dark oxidative stains. |
| `12` | **Black Line（Bl）** | 177 | 654 | Longitudinal dark line markings. |
| `13` | **Bright Bands（Bb）** | 148 | 261 | High-reflectivity vertical bands. |

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
