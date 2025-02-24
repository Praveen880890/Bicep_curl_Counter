# Bicep Curl Counter (SVM-Based)

This project is a real-time bicep curl counter using computer vision and a scikit-learn Support Vector Machine (SVM) model. It trains on user-captured images of extended and contracted arm positions to detect and count bicep curl repetitions from a webcam feed. The frontend is built with Tkinter, providing a user-friendly interface.

## Features

* **Real-time Curl Counting:** Counts bicep curls in real-time using a trained SVM model.
* **Custom Training:** Allows users to capture and train the model with their own extended and contracted arm images.
* **SVM-Based Classification:** Uses scikit-learn's LinearSVC for image classification.
* **Tkinter GUI:** Provides a graphical user interface with live feed, control buttons, and counter display.
* **Webcam Input:** Works with standard webcams.
* **Counter Reset:** Allows resetting the curl count.
* **Toggle Counting:** Enables or disables the counting process.

## Prerequisites

* Python 3.x
* OpenCV (`opencv-python`)
* scikit-learn (`sklearn`)
* NumPy (`numpy`)
* Tkinter (usually included with Python)
* Pillow (PIL)

## Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/Praveen880890/Bicep_curl_Counter.git
    cd Bicep_curl_Counter
    ```

2.  Install the required dependencies:

    ```bash
    pip install opencv-python scikit-learn numpy pillow
    ```

## Usage

1.  Run the Tkinter application:

    ```bash
    python main.py
    ```

2.  **Training:**
    * Position yourself in front of the webcam.
    * Click "Extended" to capture extended arm images.
    * Click "Contracted" to capture contracted arm images.
    * Click "Train Model" to train the SVM model using the captured images.

3.  **Counting:**
    * Click "Toggle Counting" to start the live curl counting.
    * Perform bicep curls.
    * The curl count will be displayed in the counter display.

4.  **Reset:**
    * Click "Reset" to reset the curl counter.

5.  **Exit:**
    * Close the Tkinter Window.

## Code Explanation

* **`camera.py`:**
    * Handles webcam access and frame retrieval using OpenCV.
    * Converts frames to RGB.
    * Manages camera release.
* **`app.py`:**
    * Contains the Tkinter GUI and the SVM-based curl counting logic.
    * Captures video from the webcam using OpenCV.
    * Includes functions for capturing extended and contracted images, training the SVM model, and performing real-time classification.
    * Displays the live feed, control buttons, and counter display using Tkinter.
    * Uses pillow to handle image operations.
* **`model.py`:**
    * Uses scikit-learn's LinearSVC for image classification.
    * Trains the model on captured images.
    * Provides a `predict` function to classify frames as extended or contracted.
    * Image processing to get a suitable image for the model.
* **`main.py`:**
    * Initiates the App class, and starts the GUI.

## Important Notes

* The accuracy of the curl counting depends on the quality and quantity of the training images.
* Lighting conditions and webcam quality can affect the accuracy of the image classification.
* Make sure to capture a good variety of images for better model accuracy.
* The trained model is not saved to disk, so it needs to be retrained every time the application is started. (This is a possible improvement)

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.

## Author

* Praveen880890

## License

This project is open source.
