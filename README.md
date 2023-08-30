# Driver Drowsiness Detection

This repository contains a Python-based implementation for detecting driver drowsiness using Haar Cascade files and trained models.

## Contents

- `drowsiness_detection.py`: The main Python script that utilizes Haar Cascade files to detect faces and eyes, and then predicts drowsiness based on eye aspect ratio (EAR) calculations.

- `model.py`: This script defines the architecture of the deep learning model used for drowsiness prediction. The model is trained on a suitable dataset and used to predict drowsiness based on extracted features.

- `models/`: This directory should contain the pre-trained model files.

- `haar_cascade_files/`: This directory should contain Haar Cascade XML files for face and eye detection.

- `.DS_Store`: A system-generated file on macOS that stores custom attributes of a folder. It can be ignored in version control.

- `README.md`: The file you are currently reading, providing an overview of the repository.

## How It Works

1. The `drowsiness_detection.py` script uses Haar Cascade classifiers to detect faces and eyes in a video stream or image.

2. Once the eyes are detected, the script calculates the Eye Aspect Ratio (EAR), a measure commonly used to determine eye openness. If the EAR falls below a certain threshold, it is an indication that the driver's eyes might be closed or partially closed.

3. The `model.py` script defines a deep learning model, which can be trained on a dataset containing images of open and closed eyes. This model takes eye images as input and predicts whether the eyes are open or closed.

## Getting Started

1. Clone this repository to your local machine.

2. Set up a Python virtual environment using your preferred method.

3. Install the required dependencies using the `requirements.txt` file:
   ```
   pip install -r requirements.txt
   ```

4. Download the necessary Haar Cascade XML files and place them in the `haar_cascade_files/` directory.

5. If you have a pre-trained model, place the model files in the `models/` directory.

6. Run the `drowsiness_detection.py` script:
   ```
   python drowsiness_detection.py
   ```

## Contributions

Contributions to this repository are welcome! If you find any issues or have ideas for improvements, feel free to open an issue or create a pull request.

## Disclaimer

This implementation is for educational and experimental purposes. It is not guaranteed to accurately detect driver drowsiness in all situations. Always prioritize safety while driving and use reliable and approved drowsiness detection systems where necessary.

