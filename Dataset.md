# Dataset Information

## Dataset

English-Hindi Parallel Corpus

The dataset consists of parallel English and Hindi sentence pairs used for training a Neural Machine Translation model.

---

## Number of Samples

130,476 sentence pairs

---

## Columns

| Column | Description |
|----------|-------------|
| English | Source language sentence |
| Hindi | Target language sentence |

---

## Sample

| English | Hindi |
|----------|--------|
| Help! | बचाओ! |
| Jump. | उछलो. |
| Jump. | कूदो. |
| Hello! | नमस्ते। |

---

## Data Preparation

The preprocessing pipeline performs:

- Removal of missing values (if any)
- Tokenization
- Vocabulary construction
- Integer sequence conversion
- Padding of sequences
- Addition of `<START>` token to decoder input
- Addition of `<END>` token to decoder target

---

## Sequence Preparation

Encoder Input

```
I love India
```

↓

```
[12, 45, 98, 7]
```

Decoder Input

```
<START> मैं भारत से प्यार करता हूँ
```

↓

```
[1, 54, 88, 16, 39, 20]
```

Decoder Target

```
मैं भारत से प्यार करता हूँ <END>
```

↓

```
[54, 88, 16, 39, 20, 2]
```

---

## Padding

All sequences are right padded using

```python
padding='post'
```

to maintain compatibility with TensorFlow's masked LSTM implementation.

---

## Purpose

This dataset is used for supervised Neural Machine Translation (NMT) from English to Hindi using a Seq2Seq Encoder–Decoder architecture.
