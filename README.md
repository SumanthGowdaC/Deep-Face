# DeepFace Analysis

Perform facial analysis using DeepFace library to detect emotions and race of individuals in images.

## Installation

1. Clone the repository:

    ```bash
    git clone <repository_url>
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Place the image files you want to analyze in a directory accessible to the script.
2. Update the file path in the script to point to the image file (`img1 = cv2.imread('path_to_your_image.jpg')`).
3. Run the script.
4. View the analysis results.

## Example

```python
from deepface import DeepFace
import cv2 
import matplotlib.pyplot as plt

# Load the image
img1 = cv2.imread('path_to_your_image.jpg')

# Display the image
plt.imshow(img1[:,:,::-1])
plt.show()

# Analyze emotions
emotion_result = DeepFace.analyze(img1, actions=["emotion"])
print("Emotion analysis result:", emotion_result)

# Analyze race
race_result = DeepFace.analyze(img1, actions=["race"])
print("Race analysis result:", race_result)
