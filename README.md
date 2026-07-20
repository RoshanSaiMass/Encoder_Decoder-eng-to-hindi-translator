# English to Hindi Neural Machine Translation (Seq2Seq)

A Neural Machine Translation (NMT) model that translates English sentences into Hindi using a stacked Encoder–Decoder LSTM architecture implemented from scratch in TensorFlow/Keras.

This project implements the classic Sequence-to-Sequence (Seq2Seq) architecture proposed before the introduction of Transformers, providing a complete understanding of encoder-decoder based machine translation.

---

## Features

- English → Hindi Translation
- Stacked 4-Layer LSTM Encoder
- Stacked 4-Layer LSTM Decoder
- Separate Tokenizers for Source and Target Languages
- Teacher Forcing during Training
- Word Embedding Layers
- Sequence Padding & Masking
- Softmax Word Prediction
- Built using TensorFlow/Keras

---

## Model Architecture

```
English Sentence
       │
Embedding
       │
LSTM Layer 1
       │
LSTM Layer 2
       │
LSTM Layer 3
       │
LSTM Layer 4
       │
Encoder States
       │
────────────────────────────
       │
Hindi Decoder Input
(<START> Sentence)
       │
Embedding
       │
LSTM Layer 1
       │
LSTM Layer 2
       │
LSTM Layer 3
       │
LSTM Layer 4
       │
Dense + Softmax
       │
Predicted Hindi Sentence
```

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## Dataset

The project uses an English-Hindi parallel corpus containing over **130,000** sentence pairs.

Example:

| English | Hindi |
|----------|--------|
| Help! | बचाओ! |
| Jump. | उछलो. |
| Hello! | नमस्ते। |

Special tokens used:

- `<START>`
- `<END>`

---

## Data Preprocessing

- Lowercasing
- Tokenization
- Vocabulary Creation
- Sequence Encoding
- Right Padding
- Teacher Forcing
- Addition of `<START>` and `<END>` tokens

---

## Training

Loss Function:

- Sparse Categorical Crossentropy

Optimizer:

- Adam

Training Strategy:

- Teacher Forcing

---

## Project Structure

```
.
│
├── Encoder_Decoder_Translator.ipynb
├── Dataset_English_Hindi.csv
├── README.md
└── DATASET.md
```

---

## Future Improvements

- Bahdanau Attention
- Luong Attention
- Beam Search Decoding
- BLEU Score Evaluation
- Transformer Architecture
- Larger Vocabulary
- Pretrained Embeddings

---

## References

- Sequence to Sequence Learning with Neural Networks (Sutskever et al., 2014)
- TensorFlow Documentation
- Keras Documentation
