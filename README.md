# Melody Generation with LSTM

This repository contains code for training and generating melodies using an LSTM neural network. The project involves preprocessing musical data, training an LSTM model, and generating new melodies based on the trained model.

## Files in the Repository

### 1. melodygenerator.py
Contains the `MelodyGenerator` class which uses a trained LSTM model to generate melodies.

### 2. PreProcessing.py
Includes functions and constants for preprocessing the dataset used for training the model.

### 3. train.py
Contains the script for training the LSTM model on the preprocessed dataset.

## Dataset

The dataset used in this project is taken from the following source:
[European Folk Music (Essen Folksong Collection)](https://kern.humdrum.org/cgi-bin/browse?l=essen/europa/deutschl)

## Getting Started

### Prerequisites
- Python 3.x
- TensorFlow
- music21
- NumPy
- Matplotlib

### Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/melody-generation-lstm.git
    cd melody-generation-lstm
    ```
2. Install the required packages:
    ```sh
    pip install -r requirements.txt
    ```

### Usage

#### Preprocess the Dataset
1. Ensure your dataset is in the correct format and located in the specified path (`KERN_DATASET_PATH`).
2. Run the preprocessing script to generate the training sequences.

#### Train the Model
1. Customize the training parameters in `train.py` if necessary.
2. Run the training script:
    ```sh
    python train.py
    ```

#### Generate Melodies
1. Use the `MelodyGenerator` class to generate new melodies:
    ```python
    from melodygenerator import MelodyGenerator
    
    mg = MelodyGenerator(model_path="model.h5")
    seed = "your-seed-string"
    melody = mg.generate_melody(seed, num_steps=500, max_sequence_length=64, temperature=1.0)
    ```

## Acknowledgements

A huge thanks to Valerio Velardo - The Sound of AI for helping me in this project.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License.
