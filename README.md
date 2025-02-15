# README: Magnetotelluric Inversion with GAT-Attention Model  

This repository contains the code for our paper: **"Advancing Magnetotelluric Inversion: Graph Attention Networks with Multihead Attention for Improved Resistivity Model Estimation"**. The proposed method addresses the challenges of nonlinearities and noise in magnetotelluric (MT) data inversion, offering improved accuracy and interpretability over traditional and existing machine learning techniques.  

## Abstract  

Magnetotellurics investigates subsurface resistivity from natural electromagnetic variations. Traditional MT inversion methods often struggle with nonlinearities and noisy data, resulting in less accurate resistivity profiles. While CNNs and LSTM-based models have been proposed, they still fail to effectively handle complex dependencies and noisy patterns. Our proposed deep learning architecture, based on Graph Attention Networks (GATs) and Multihead Attention mechanisms, dynamically focuses on the most relevant frequencies, enhancing depth dependency capture and improving resistivity predictions. Extensive tests on synthetic and real-world datasets demonstrate that our approach outperforms existing machine learning models, offering greater robustness to noise and non-linearity, and generating more accurate and interpretable resistivity profiles.  

---

## Repository Structure  

The repository is organized as follows:  

- `Data Generation and Training/`  
  Contains scripts for generating synthetic MT data, including resistivity profiles and their corresponding apparent resistivity and phase responses.  

- `README.md`  
  Instructions for using the codebase.  

---

## Requirements  

The code requires the following dependencies:  

- Python >= 3.8  
- TensorFlow >= 2.6.0  
- NumPy  
- Pandas  
- Matplotlib  
- SciPy  
- Scikit-learn  

Install the required packages using:  

```bash
pip install -r requirements.txt
```  

---

## Data Generation  

### Synthetic Data  
The synthetic data is generated by simulating resistivity profiles and their corresponding MT responses:  

1. **Resistivity Profiles:** Generated with a wide range of resistive and conductive structures.  
2. **MT Responses:** Apparent resistivity and phase computed across 90 frequencies.  
3. **Noise Addition:** Gaussian noise with varying levels (1%-5%) is added to simulate real-world measurement conditions.  

Run the script to generate synthetic data:  

```bash
python 'Data Generation and Training'/Data_generation.ipynp 
```  

---

## Model Implementation  

### GAT-Attention Model  
The proposed model integrates Graph Attention Networks (GATs) and Multihead Attention mechanisms to dynamically focus on relevant frequencies and improve depth dependency capture.  

**Key Features:**  
- Two GAT layers with multihead attention.  
- Feedforward neural network for final resistivity predictions.  
- Regularization and early stopping for robust training.  

---
Run the script to train the model:  

```bash
python 'Data Generation and Training'/'Model and Training.ipynb'
```

## Results  

The GAT-Attention model performs very well on synthetic and real-world data compared to VNNs and CNNs, achieving higher accuracy and robustness to noise.  

---

## License  

This repository is released under the [MIT License](LICENSE).  


## Contact  

For questions or feedback, please reach out to [700044583@uaeu.ac.ae].
