# Image-Caption-Generator

This project implements an Image Caption Generator model that creates descriptive captions for images. It combines **Computer Vision** (to extract image features) and **Natural Language Processing** (to generate text).

## 📂 Dataset
I used the **Flickr8k Dataset**. The dataset is not included in this repository due to size constraints.
* **Source:** [Kaggle - Flickr8k Dataset](https://www.kaggle.com/adityajn/flickr8k)
* **Structure:** 8,000 images paired with 5 different captions each.

## 🏗️ Architecture
The model uses an encoder-decoder architecture:
1.  **Image Feature Extraction (Encoder):** [VGG16] pretrained on ImageNet is used to extract feature vectors from images.
2.  **Sequence Processing (Decoder):** An LSTM (Long Short-Term Memory) network processes the text sequences.
3.  **Fusion:** The image features and text embeddings are merged and passed through dense layers to predict the next word in the caption.

## 🛠️ Files in this Repo
* `Image_Caption_Generator.ipynb`: The main Google Colab notebook containing training and testing code.
* `requirements.txt`: List of Python dependencies.
* `Predictions`: Screenshots of the predicted results from the test sets/

## 🔗 Large Files (Download Required)
Due to GitHub's file size limits, the trained model and extracted features are hosted externally:

* **Best Model (.h5):** [https://drive.google.com/file/d/17NSGtKy3J7jBry0ihfmte73iJFkrncuQ/view?usp=sharing]
* **Features File (.pkl):** [https://drive.google.com/file/d/1hIdU4w9hbViHd9sQxhThZixvpiL3wD3n/view?usp=drive_link]

## 🚀 How to Run
1.  Clone the repository.
2.  Download the **Flickr8k dataset** and place it in the project folder.
3.  Download the **Model** and **Features File** from the links above.
4.  Open `Image_Caption_Generator.ipynb` in Jupyter or Google Colab.
5.  Update the file paths in the notebook to point to your downloaded files.
6.  Run the "Generate Caption" cell to test on new images.

## 📊 Results
The screenshots of some predictions made by the model is added in the Repo in Predictions folder along with the BLEU Score of the model.
