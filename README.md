
# HDRoad: Using Hybrid Attention and Directional Prior for Road Segmentation in Remote Sensing

This repository contains the code, training weights, and datasets for the paper "HDRoad: Using Hybrid Attention and Directional Prior for Road Segmentation in Remote Sensing."

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Datasets](#datasets)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

HDRoad is a novel encoder-decoder architecture tailored for road segmentation in remote sensing imagery. It features a Hybrid Attention Network (HA-Net) as the encoder, incorporating both dense and sparse spatial attentions to effectively distill semantic information. The decoder, Directional Augmented Road Morphology Extraction Network (DARMEN), utilizes morphological priors to refine and reconstruct road features.

## Installation

### Prerequisites

- Python 3.x
- PyTorch
- Other dependencies listed in `requirements.txt`

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/Hellmett/HDRoad.git
   cd HDRoad
   ```

2. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Training

To train the model on the SouthernChina13k dataset, use the following command:

```bash
python train.py --dataset SouthernChina13k --epochs 50 --batch_size 16 --learning_rate 0.0001
```

### Evaluation

To evaluate the trained model, use the following command:

```bash
python evaluate.py --model_path checkpoints/best_model.pth --dataset SouthernChina13k
```

### Inference

To run inference on new images, use the following command:

```bash
python inference.py --model_path checkpoints/best_model.pth --input_path path_to_input_images --output_path path_to_save_results
```

## Datasets

The SouthernChina13k dataset used in this project can be downloaded from [link to dataset]. Ensure the dataset is placed in the `data` directory.

## Results

The experimental results demonstrate that HDRoad surpasses both mainstream and specialized road-segmentation methods by a margin of 4%, setting new benchmarks for state-of-the-art performance in the field.

## Contributing

We welcome contributions to enhance the project. Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or issues, please contact He Fan at fan_he@tongji.edu.cn.

---
