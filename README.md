# A GAN-Based Approach to Solar Radiation Prediction

This repository contains the code, datasets, and documentation for the study titled "A GAN-based approach to solar radiation prediction: data augmentation and model optimization for Saudi Arabia." The framework employs Generative Adversarial Networks (GANs) to generate synthetic solar radiation data, enhancing the predictive accuracy of machine learning and deep learning models.

## Repository Structure

```plaintext
.
├── README.md                   # Documentation and instructions
├── data/                       # Dataset folder
│   ├── raw/                    # Raw datasets
│   ├── processed/              # Preprocessed datasets
├── src/                        # Source code folder
│   ├── preprocessing.py        # Data preprocessing scripts
│   ├── gan_training.py         # GAN training scripts
│   ├── model_training.py       # Predictive model training scripts
│   ├── evaluation.py           # Evaluation metrics implementation
├── notebooks/                  # Jupyter notebooks for experiments
│   ├── exploratory_analysis.ipynb
│   ├── gan_training.ipynb
│   ├── model_evaluation.ipynb
├── results/                    # Results and outputs
│   ├── synthetic_data_samples/ # GAN-generated synthetic data
│   ├── model_performance/      # Model performance metrics and plots
├── requirements.txt            # Required Python libraries
├── LICENSE                     # License information
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- NVIDIA GPU (Recommended for GAN training)
- Libraries listed in `requirements.txt`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ProfAlameen/-A-GAN-based-approach-to-solar-radiation-prediction-data-augmentation-and-model-optimization.git
   cd -A-GAN-based-approach-to-solar-radiation-prediction-data-augmentation-and-model-optimization
   ```

2. Create a virtual environment and install dependencies:
   ```bash
   python -m venv env
   source env/bin/activate  # For Windows, use `env\Scripts\activate`
   pip install -r requirements.txt
   ```

3. Verify the installation:
   ```bash
   python --version
   pip list
   ```

## Usage

### 1. Data Preprocessing

Run the preprocessing script to normalize and partition the dataset:
```bash
python src/preprocessing.py --input data/raw/ --output data/processed/
```

### 2. GAN Training

Train the GAN to generate synthetic solar radiation data:
```bash
python src/gan_training.py --config configs/gan_config.json
```

### 3. Predictive Model Training

Train predictive models using augmented datasets:
```bash
python src/model_training.py --data data/processed/ --output results/model_performance/
```

### 4. Evaluation

Evaluate the predictive models:
```bash
python src/evaluation.py --results results/model_performance/
```

## Datasets

- **Raw Data**: Place raw datasets in the `data/raw/` folder.
- **Preprocessed Data**: Processed datasets will be saved in `data/processed/`.
- **Synthetic Data**: Samples of GAN-generated data can be found in `results/synthetic_data_samples/`.

## Results

All results, including synthetic data samples and performance metrics, are stored in the `results/` directory. Key metrics include RMSE, MAE, and SSIM.

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add some feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or collaboration, please contact Abdalla Alameen at [a.alameen@psau.edu.sa](mailto:a.alameen@psau.edu.sa).

---

This README provides a detailed guide to understand, set up, and use the repository effectively. Let me know if additional details or customization are needed.
