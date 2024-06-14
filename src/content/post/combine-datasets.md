---
title: "Combine datasets"
description: "--------------------------------------------------"
publishDate: "1 Jun 2024"
tags: ["deep learning", "object detection", "YOLO"]
---

I merged two datasets: a custom dataset with 2,418 images and the COCO128 dataset with 128 images.

After training the model, I evaluated its performance using the trained weight.pt for object detection.

<br>

> I observed two issues: incorrect detections and failure to recognize objects altogether.

<br>

The problem stemmed from the **imbalance between the datasets**; such a significant disparity can weaken the classification standards.

In classification models, a biased dataset can lead to overfitting, which negatively impacts the model's performance on larger datasets.

If you're facing difficulties in dataset collection, <U>consider setting the training data ratio to 9:1 or 8:2</U> to mitigate this issue. 😊

<br>
<br>
<br>

![1](@/assets/1.jpeg)