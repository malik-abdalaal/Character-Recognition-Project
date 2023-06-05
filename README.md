# Character-Recognition-Project
Project Description:

The provided code consists of two parts. The first part generates letter images and saves them as JPEG files. It uses the generate_letter_image and generate_text_image functions to create images of individual letters and text, respectively. The generated images are saved in the "images" directory using different fonts. The second part of the code involves training a character classification model and evaluating its performance.

Project Details:

1. Generating Letter Images:

•The generate_letter_image function generates a letter image using a specified font. It creates a blank image with a black background and draws the letter on it using the specified font. The image is then saved as a JPEG file in the "images" directory with the font name as a subdirectory.

• The generate_text_image function generates a text image using a specified font. It creates a blank image with a black background and draws each letter of the text on the image using the specified font. The images are saved as JPEG files in the "images/text" directory with the font name and text as the file name.

• The code includes a loop that iterates over a list of fonts and generates letter and text images for the English alphabet.

2. Training and Evaluating the Character Classification Model:

• The code loads training and test data from numpy files (training_images.npy, training_labels.npy, test_images.npy, test_labels.npy).
• It performs some preprocessing on the data by expanding the dimensions of the images, normalizing the pixel values to the range [0, 1], and converting the data type to float32.
• A visual representation of a subset of training images is displayed using subplots.
• The code defines a sequential model named "chars_classifier" using Keras. It consists of convolutional layers followed by dense layers. The model is compiled with the Adam optimizer and sparse categorical cross-entropy loss.
• The model's summary is printed, showing the layers and the number of parameters.
• The accuracy of the model on the test data is evaluated and printed.
• The predict_image function is defined to make predictions on individual images using the trained model. It loads the model, preprocesses the image, and makes predictions using the model. The predicted label (character) is returned.
• The test_letters function is defined to test the trained model on a subset of letter images. It displays the letter images along with their predicted labels. The number of wrong predictions is counted and printed.
• The code includes a loop that iterates over the files in the "images" directory (excluding the "images/text" directory) and calls the test_letters function for each font.
• The predict_text function is defined to predict the text from a test image by making predictions on individual characters. It takes a test image, preprocesses it, and calls the predict_image function for each character in the image. The predicted text is returned.
• The differences function is defined to compare two strings character by character and return the indexes of the differing characters.
• The code generates text images using different fonts and specific text phrases.
• It tests the trained model on the text images and displays the predicted text along with any differences between the predicted and actual text. The number of wrong letters is counted and printed.
• The final accuracy is calculated by comparing the total number of tested characters with the number of wrong letters.

![image](https://github.com/malik-abdalaal/Character-Recognition-Project/assets/108053187/fa352a06-e7fd-4deb-8381-fecb5a90f026)

![image](https://github.com/malik-abdalaal/Character-Recognition-Project/assets/108053187/94108da4-6b74-42e4-86cb-1a4c0720fe58)
