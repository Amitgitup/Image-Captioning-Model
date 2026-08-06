# Image Captioning Model

## Overview
This project implements an end-to-end deep learning pipeline for automatic image captioning. The model generates natural language descriptions for images by combining computer vision and natural language processing techniques. The approach uses a CNN (DenseNet201) for image feature extraction and an RNN (LSTM) for sequence generation.

## Features
- End-to-end image captioning using deep learning
- Preprocessing and tokenization of captions
- Feature extraction from images using DenseNet201
- Custom data generator for efficient training
- Model training with early stopping and learning rate scheduling
- Streamlit web app for interactive caption generation
- Utilities for inference and visualization

## Project Structure
```
├── main.py                  # Streamlit app for caption generation
├── image-captioning-model.ipynb  # Model training and experimentation notebook
├── model.keras              # Trained captioning model
├── feature_extractor.keras  # Trained image feature extractor
├── feature_extractor.pkl    # Pickled feature extractor
├── tokenizer.pkl            # Pickled tokenizer
```

## Setup Instructions
1. **Clone the repository**
2. **Install dependencies** (create a requirements.txt if not present):
   ```bash
   pip install streamlit tensorflow keras numpy pandas matplotlib seaborn tqdm
   ```
3. **Download the Flickr8k dataset** and place images and captions in the appropriate directories as referenced in the notebook.
4. **Train the model** (optional):
   - Run `image-captioning-model.ipynb` to preprocess data, extract features, and train the model.
   - Saved models and tokenizers will be generated.
5. **Run the Streamlit app**:
   ```bash
   streamlit run main.py
   ```

## Usage
- Upload an image using the web interface.
- The app will display the image and generate a caption using the trained model.

## Example Output
![Sample Output](sample_output.png)

## References
- [Flickr8k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr8k)
- [DenseNet201 Paper](https://arxiv.org/abs/1608.06993)
- [Image Captioning with Deep Learning](https://papers.nips.cc/paper/2015/hash/a8d2c5bfa2b9e3d5b1a9e7b8e6b1c1c1-Abstract.html)

## License
MIT License

---

**For more details, see the Jupyter notebook (`image-captioning-model.ipynb`).**
