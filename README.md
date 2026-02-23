# Pixel Coordinate Prediction — DeepEdge ML Assignment

**Author:** Vaibhav Dasari

---

## Problem Statement

Given a 50×50 grayscale image with exactly one white pixel (value 255) and all others black (value 0), predict the **(x, y)** coordinates of that white pixel using a deep learning model.

---

## Approach

I approached this as a **regression problem**, where the model predicts the x and y coordinates directly.

Since the input is spatial (an image), I used a CNN to help the model learn where the active pixel is located. I normalized both the input images and the output coordinates to make training more stable, and used a sigmoid activation at the end so predictions stay within a valid range.
---

## Repository Structure

```
.
├── Vaibhav_ML_Assignment_final.ipynb   # Main notebook with full solution
└── README.md                           # This file
```

---

## Dependencies

The project uses the following libraries:
- numpy  
- matplotlib  
- tensorflow  
- scikit-learn  

If running locally, install them using:

    pip install numpy matplotlib tensorflow scikit-learn

The notebook was developed and tested on Google Colab.

---

## How to Run

**Option 1 — Google Colab (recommended):**
1. Upload `Vaibhav_ML_Assignment_final.ipynb` to Google Colab
2. Run all cells from top to bottom (`Runtime → Run all`)

**Option 2 — Local Jupyter:**
1. Install dependencies (see above)
2. Launch Jupyter: `jupyter notebook`
3. Open `Vaibhav_ML_Assignment_final.ipynb` and run all cells

---

## What the Notebook Contains

- Dataset generation using synthetic data  
- CNN-based model for coordinate prediction  
- Training with validation split  
- Training Curves - Loss and MAE plots across epochs
- Evaluation on a separate test set  
- Scatter plots on Ground truth vs predicted X and Y coordinates  
- Error distribution analysis  
- Visualization of predictions on sample images  
---

## Results Summary

The model is trained on 50,000 synthetic images and evaluated on a completely separate test set of 5,000 images. It achieves sub-pixel mean Euclidean error, with predicted coordinates visually overlapping the ground truth pixel in nearly all test cases. The model has learned the spatial mapping effectively.

---

## Final Thoughts

This was a simple but interesting problem to work on. Even though it can be solved directly using logic, using a neural network helped me understand how models learn positional information from minimal data.