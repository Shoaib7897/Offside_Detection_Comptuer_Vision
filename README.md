# Offside_Detection_Computer_Vision

## Introduction

![Offside Rule Illustration](assets/offside_rule_illustration.png)

In many sports, referees are tasked with making crucial decisions that can significantly impact the outcome of games. Human bias and inconsistencies, however, mean that errors are inevitable. This project aims to solve this problem in the context of soccer by using computer vision techniques to automatically identify offside positions.

## Background

By definition, an attacking player is considered to be in an offside position under certain conditions. The rules are complex but crucial for fair gameplay.

> **Figure 1**: Player A is considered to be offside  
> ![Player A Offside](assets/player_a_offside.png)

## Details of the Approach

### YOLOv5 Model

![YOLOv5 Architecture](assets/yolov5_architecture.png)

We use the YOLOv5 model for object detection to identify players and their bounding boxes. The model is both fast and accurate, making it ideal for real-time applications.

#### Bounding Box Explanation

```python
# Sample code to calculate bounding box coordinates
def calculate_coordinates(x1, y1, x2, y2):
    return ((x1 + x2) / 2, y2)
