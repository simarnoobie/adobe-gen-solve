
**important** we could not completely train the model due to computation limitation however we have developed a complete model.

# CURVETOPIA: Curve Regularization and Beautification Pipeline

## Overview

CURVETOPIA is a comprehensive toolset designed for identifying, regularizing, and beautifying various types of curves in 2D Euclidean space. This project provides an end-to-end pipeline that:

1. **Trains a Convolutional Neural Network (CNN)** for classifying doodle images.
2. **Uses a U-Net model** to complete and beautify incomplete curves.
3. **Detects and applies symmetry** to enhance curves.
4. **Processes and simplifies curves** using methods like spline fitting.
5. **Outputs processed curves** as cubic Bezier curve coordinates in a CSV file.

## Features

- **Curve Regularization**: Improves the shape and smoothness of curves.
- **Curve Completion**: Completes incomplete or broken curves using a trained U-Net model.
- **Symmetry Detection and Application**: Detects both mirror and rotational symmetry and applies it to improve curve aesthetics.
- **Curve Simplification**: Reduces the complexity of curves using various methods.
- **End-to-End Workflow**: From raw doodles to beautified curves saved as cubic Bezier coordinates.

## Prerequisites

- Python 3.7
- Training and testing dataset.

## Usage

1. **Prepare Data**:
   - Organize your training images in `train_folder/` with subfolders named after each label.
   - Place the test CSV file with cubic Bezier curve coordinates in `test_folder/test.csv`.

   The script will:
   - Load and preprocess the training and test data.
   - Train a CNN model on the training images.
   - Train a U-Net model to complete and beautify curves.
   - Detect symmetry in curves and apply it where necessary.
   - Simplify and regularize the curves.
   - Save the processed curves as cubic Bezier coordinates in `output.csv`.

## Core Functions

- **`preprocess_doodles`**: Loads and preprocesses training and test images.
- **`build_model`**: Constructs and compiles a CNN model for image classification.
- **`build_unet`**: Builds a U-Net model for inpainting and curve completion.
- **`train_model`**: Trains the CNN model using data augmentation techniques.
- **`train_inpainting_model`**: Trains the U-Net model for curve inpainting.
- **`complete_incomplete_curves`**: Uses the trained U-Net model to complete and beautify curves.
- **`detect_symmetry`** and **`detect_rotational_symmetry`**: Detect and apply symmetry to curves.
- **`process_curve_points`**: Regularizes and smooths the curves using methods like spline fitting.
- **`simplify_curve`**: Simplifies the curves to reduce their complexity while preserving the essential shape.
- **`save_bezier_coordinates_to_csv`**: Saves the final cubic Bezier curve coordinates to a CSV file.



This will process the images and Bezier curves according to the steps outlined above and output the final coordinates to `output.csv`.

## Contact

For questions or contributions, feel free to contact the developers:

- **Gursimardeep singh**: simardeep2004z@gmail.com
- **Ekamjot singh**: ekmajotjaggi2511@gmail.com

