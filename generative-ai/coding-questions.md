# Generative AI Coding Questions

## 1. Implementing a Simple Generative Model
- **Question**: Write a Python function to implement a simple generative model using Gaussian Mixture Models (GMM).
- **Answer**:
```python
import numpy as np
from sklearn.mixture import GaussianMixture

def generate_samples(n_samples=100, n_components=3):
    # Generate random data
    X = np.random.rand(n_samples, 2)
    
    # Fit a Gaussian Mixture Model
    gmm = GaussianMixture(n_components=n_components)
    gmm.fit(X)
    
    # Sample from the GMM
    samples, _ = gmm.sample(n_samples)
    return samples
```

## 2. Text Generation with LSTM
- **Question**: How would you implement a simple text generation model using LSTM in TensorFlow/Keras?
- **Answer**:
```python
import numpy as np
from keras.models import Sequential
from keras.layers import LSTM, Dense, Embedding

def create_lstm_model(vocab_size, embedding_dim, lstm_units):
    model = Sequential()
    model.add(Embedding(input_dim=vocab_size, output_dim=embedding_dim))
    model.add(LSTM(lstm_units, return_sequences=True))
    model.add(Dense(vocab_size, activation='softmax'))
    return model
```

## 3. Image Generation with GANs
- **Question**: Describe how to implement a simple Generative Adversarial Network (GAN) for image generation.
- **Answer**:
```python
from keras.models import Sequential
from keras.layers import Dense, Reshape, Flatten

def build_generator(latent_dim):
    model = Sequential()
    model.add(Dense(128, activation='relu', input_dim=latent_dim))
    model.add(Dense(784, activation='sigmoid'))
    model.add(Reshape((28, 28)))
    return model

def build_discriminator():
    model = Sequential()
    model.add(Flatten(input_shape=(28, 28)))
    model.add(Dense(128, activation='relu'))
    model.add(Dense(1, activation='sigmoid'))
    return model
```

## 4. Fine-tuning a Pre-trained Transformer
- **Question**: Explain how to fine-tune a pre-trained transformer model for a specific NLP task.
- **Answer**:
```python
from transformers import AutoModelForSequenceClassification, Trainer, TrainingArguments

def fine_tune_model(model_name, train_dataset, eval_dataset):
    model = AutoModelForSequenceClassification.from_pretrained(model_name)
    training_args = TrainingArguments(
        output_dir='./results',
        num_train_epochs=3,
        per_device_train_batch_size=16,
        per_device_eval_batch_size=64,
        evaluation_strategy='epoch'
    )
    trainer = Trainer(
        model=model,
        args=training_args,
        train_dataset=train_dataset,
        eval_dataset=eval_dataset
    )
    trainer.train()
```

## 5. Evaluating Generative Models
- **Question**: What metrics would you use to evaluate the performance of a generative model?
- **Answer**:
- Inception Score (IS)
- Fréchet Inception Distance (FID)
- Perceptual Similarity Metrics (LPIPS)

## Conclusion
These coding questions cover various aspects of generative AI, including model implementation, fine-tuning, and evaluation. Understanding these concepts is crucial for roles focused on generative models in machine learning and AI.