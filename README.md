# 🖼️ AI-Powered Image Caption Generator

An end-to-end machine learning project that generates descriptive captions for images using state-of-the-art computer vision and natural language processing.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-red)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28%2B-green)
![Transformers](https://img.shields.io/badge/🤗%20Transformers-4.30%2B-yellow)

## 🎯 Project Overview

This project combines **Computer Vision** and **Natural Language Processing** to automatically generate human-readable descriptions of images. It demonstrates a complete ML workflow from model implementation to web deployment.

### ✨ Key Features

- **State-of-the-art AI Model**: Uses BLIP (Bootstrapping Language-Image Pre-training) from Salesforce Research
- **Web Interface**: Interactive Streamlit app for easy image upload and caption generation
- **Real-time Processing**: Instant caption generation with pre-trained models
- **User-friendly**: Simple drag-and-drop interface with sample images
- **Educational**: Detailed explanations of the underlying technology

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│                 │    │                 │    │                 │
│  Input Image    │───▶│  Vision Model   │───▶│  Text Decoder   │
│  (JPG/PNG)     │    │  (ViT Encoder)  │    │  (Language LM)  │
│                 │    │                 │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                                                        │
                                                        ▼
                                              ┌─────────────────┐
                                              │                 │
                                              │ Generated       │
                                              │ Caption         │
                                              │                 │
                                              └─────────────────┘
```

### 🔧 Technical Components

1. **Vision Encoder**: Vision Transformer (ViT) extracts visual features
2. **Language Decoder**: Transformer-based language model generates captions
3. **Preprocessing**: Image normalization and tokenization
4. **Inference**: Beam search for optimal caption generation

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dinnysriramcharan/image-caption-generator.git
   cd image-caption-generator
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application:**
   ```bash
   streamlit run src/app.py
   ```

4. **Open your browser** and navigate to `http://localhost:8501`

## 📁 Project Structure

```
image-caption-generator/
├── src/
│   └── app.py              # Main Streamlit application
├── data/                   # Dataset storage (for future training)
├── notebooks/              # Jupyter notebooks for experimentation
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
└── .gitignore            # Git ignore patterns
```

## 🎮 Usage

### Web Interface

1. **Upload an Image**: Click "Browse files" and select a JPG, JPEG, or PNG image
2. **Try Sample**: Click "Try Sample Image" to test with a demo image
3. **Generate Caption**: Click the "Generate Caption" button
4. **View Results**: The AI-generated caption will appear below the image

### Example Results

| Image | Generated Caption |
|-------|------------------|
| 🐱 Cat | "a close up of a cat looking at the camera" |
| 🏔️ Mountain | "a view of a mountain range with snow capped peaks" |
| 🏖️ Beach | "a beautiful sunset over the ocean with waves crashing on the shore" |

## 🔬 Model Details

### BLIP (Bootstrapping Language-Image Pre-training)

- **Paper**: [BLIP: Bootstrapping Language-Image Pre-training](https://arxiv.org/abs/2201.12086)
- **Developer**: Salesforce Research
- **Architecture**: Vision-Language Transformer
- **Training Data**: 14M+ image-text pairs from the web
- **Performance**: State-of-the-art on multiple vision-language benchmarks

### Key Advantages

- **Multimodal Understanding**: Jointly processes visual and textual information
- **Robust Performance**: Handles diverse image types and styles
- **Efficient Inference**: Optimized for real-time applications
- **Pre-trained**: No additional training required

## 🛠️ Development

### Adding New Features

The project is designed to be extensible:

1. **Custom Models**: Replace BLIP with other vision-language models
2. **Fine-tuning**: Add domain-specific training on custom datasets
3. **Additional Features**: Implement visual question answering, image search, etc.
4. **Performance**: Add GPU acceleration, model quantization, caching

### Directory Details

- **`src/`**: Source code for the main application
- **`data/`**: Placeholder for datasets (MS COCO, Flickr30k, etc.)
- **`notebooks/`**: Jupyter notebooks for research and experimentation

## 📊 Performance & Evaluation

The model can be evaluated using standard metrics:

- **BLEU Score**: Measures n-gram overlap with reference captions
- **CIDEr**: Consensus-based evaluation metric
- **METEOR**: Considers synonyms and paraphrases
- **ROUGE-L**: Longest common subsequence metric

## 🔄 Future Enhancements

- [ ] **Custom Training**: Implement training pipeline for domain-specific data
- [ ] **Multi-language Support**: Support for captions in multiple languages
- [ ] **Batch Processing**: Handle multiple images simultaneously
- [ ] **API Deployment**: RESTful API for programmatic access
- [ ] **Mobile App**: React Native or Flutter mobile application
- [ ] **Advanced Models**: Integration with GPT-4V, LLaVA, or other VLMs

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Salesforce Research** for the BLIP model
- **Hugging Face** for the Transformers library
- **Streamlit** for the web framework
- **PyTorch** for the deep learning framework

## 📞 Contact

- **Developer**: Dinny Sriram Charan
- **GitHub**: [@dinnysriramcharan](https://github.com/dinnysriramcharan)
- **Project Link**: [https://github.com/dinnysriramcharan/image-caption-generator](https://github.com/dinnysriramcharan/image-caption-generator)

---

**⭐ If you found this project helpful, please consider giving it a star!**
