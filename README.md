# MudraVisualisation

1. collect_imgs.py
This script captures images from a live video feed using OpenCV. It allows the user to collect a dataset of hand images for various classes. The number of classes (n), images per class (dataset_size), and other parameters can be adjusted.

2. image_cropper.py
This script uses the MediaPipe library to crop hand images captured by the collect_imgs.py script. It detects hand landmarks and crops the images around the detected hand region. Cropped images are then saved to a specified output directory.

3. image_flipper.py
This script takes the cropped hand images from the image_cropper.py script and creates horizontally flipped versions. The flipped images are saved with a 'flipped_' prefix in the same directory.

4. YOLO_model.ipynb
This Jupyter notebook demonstrates the usage of the Ultralytics YOLO (You Only Look Once) framework for training a model on hand images. It uses a pre-trained YOLO model and fine-tunes it on a specified dataset, showing how to train the model for a certain number of epochs and image size.

5. Metrics_YOLO.ipynb
This Jupyter notebook evaluates the trained YOLO model from YOLO_model.ipynb. It calculates and displays accuracy, precision, recall, F1-score, and confusion matrix using scikit-learn metrics. It also maps the predicted class labels to the original class labels based on a provided mapping.

6. VideoYOLO.ipynb
This Jupyter notebook integrates hand detection using the MediaPipe library with a pre-trained YOLO model for mudra (hand gesture) recognition. It captures live video, detects hands, crops the region of interest, and predicts the mudra using the YOLO model. Predictions are displayed in real-time along with bounding boxes on the detected hands.
