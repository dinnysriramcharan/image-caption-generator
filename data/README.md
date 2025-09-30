# Data Directory

This directory is designed to store datasets for training and evaluation of image captioning models.

## Recommended Dataset Structure

```
data/
├── raw/                    # Original, unprocessed datasets
│   ├── coco/              # MS COCO dataset
│   ├── flickr30k/         # Flickr30k dataset
│   └── custom/            # Custom datasets
├── processed/             # Preprocessed datasets
│   ├── train/
│   ├── val/
│   └── test/
└── samples/               # Sample images for testing
```

## Popular Image Captioning Datasets

### 1. MS COCO Captions
- **Size**: 123K images, 615K captions
- **Source**: [MS COCO Dataset](https://cocodataset.org/)
- **Format**: JSON annotations with image paths
- **Use**: Standard benchmark for image captioning

### 2. Flickr30k
- **Size**: 31K images, 158K captions  
- **Source**: [Flickr30k Dataset](http://shannon.cs.illinois.edu/DenotationGraph/)
- **Format**: Text files with captions
- **Use**: Alternative benchmark dataset

### 3. Conceptual Captions
- **Size**: 3.3M image-caption pairs
- **Source**: [Google AI](https://ai.google.com/research/ConceptualCaptions/)
- **Format**: TSV files with URLs and captions
- **Use**: Large-scale pre-training

## Download Instructions

### MS COCO (Recommended for beginners)

```bash
# Download images
wget http://images.cocodataset.org/zips/train2017.zip
wget http://images.cocodataset.org/zips/val2017.zip

# Download annotations
wget http://images.cocodataset.org/annotations/annotations_trainval2017.zip

# Extract
unzip train2017.zip -d data/raw/coco/
unzip val2017.zip -d data/raw/coco/
unzip annotations_trainval2017.zip -d data/raw/coco/
```

### Flickr30k

```bash
# Request access from: http://shannon.cs.illinois.edu/DenotationGraph/
# Follow dataset provider's instructions for download
```

## Data Preprocessing

The `notebooks/` directory contains examples for:
- Loading and preprocessing datasets
- Converting annotations to standard formats
- Creating train/validation splits
- Data augmentation techniques

## Usage with This Project

The current implementation uses pre-trained models and doesn't require downloading datasets. However, if you want to:

1. **Fine-tune models**: Download MS COCO or Flickr30k
2. **Evaluate performance**: Use validation sets with ground truth captions
3. **Train from scratch**: Use large-scale datasets like Conceptual Captions

## File Formats

- **Images**: JPG, PNG (recommended: 224x224 or larger)
- **Annotations**: JSON (COCO format) or TSV (simple format)
- **Captions**: UTF-8 encoded text files

## Notes

- Large datasets are excluded from git via `.gitignore`
- Consider using cloud storage for large datasets
- Always respect dataset licenses and usage terms