Smart Toy Scanner
->Project Description
This project develops a Smart Toy Scanner using an EfficientNet-B0 model trained to classify toy materials (wood, fabric, plastic, rubber). The project includes data collection, model training, evaluation, and deployment as a Flask web application.

->Setup Instructions
To set up and run this project locally or in a Colab environment, follow these steps:
Install Dependencies: Ensure you have all necessary libraries installed. This notebook automatically installs duckduckgo-search, timm, ddgs, pyngrok, and Flask.
!pip install duckduckgo-search timm ddgs pyngrok Flask
Dataset Preparation: The notebook downloads images for various toy materials (wood, fabric, plastic, rubber) using ddgs.DDGS().images. It then cleans corrupted images and splits the dataset into training and testing sets.
Model Training: An EfficientNet-B0 model is loaded with pre-trained weights and fine-tuned for toy material classification. The model is trained for 5 epochs.
Model Evaluation: The trained model's accuracy is evaluated on the test set.
Web Application Deployment: A Flask web application is created to allow users to upload an image and get a prediction of the toy's material. The app is exposed publicly using ngrok.

->Usage
Once the Flask application is running and the ngrok tunnel is established, you will receive a public URL. Visit this URL in your web browser.

->Upload Image: On the web interface, you can upload an image of a toy.
Get Prediction: The application will then predict the material of the toy (e.g., wood, fabric, plastic, rubber) and display the confidence level.
