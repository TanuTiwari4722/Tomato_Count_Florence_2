# Tomato_Count_Florence_2
Counting tomatoes using the **Phrase Grounding** Task from Florence2

This notebook evaluates the performance of the **Florence-2** base fine-tuned model on a custom dataset of tomato images. The goal is to assess the model’s phrase grounding (PG) capability by comparing predicted bounding boxes against ground truth labels.

**Model Setup**

model_predict() takes an image, task prompt, and phrase to generate bounding boxes and labels.

Filters out large boxes to avoid noise from overly general detections.

**Dataset**

Images and labels from the corresponding dataset.

**Evaluation**

For each image:

* Predict objects using the model.
* Count number of ground-truth vs predicted bounding boxes.

Compare predicted object count against ground-truth using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* R² Score
