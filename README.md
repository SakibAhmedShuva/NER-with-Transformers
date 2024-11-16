# NER with Transformers

This repository demonstrates Named Entity Recognition (NER) using Hugging Face Transformers library. The implementation utilizes a pre-trained BERT model fine-tuned on the CoNLL-03 dataset for English Named Entity Recognition.

## Overview

Named Entity Recognition (NER) is a natural language processing task that identifies and classifies key information (entities) in text into predefined categories such as:
- Person names
- Organizations
- Locations
- Time expressions
- Quantities
- Monetary values
- etc.

## Requirements

- Python 3.8+
- transformers
- torch

Install the required packages using:

```bash
pip install transformers torch
```

## Model Details

The project uses the `dbmdz/bert-large-cased-finetuned-conll03-english` model, which is a BERT-large model fine-tuned specifically for NER tasks. This model has been trained on the CoNLL-03 dataset and can recognize standard entity types including:
- PER (Person)
- ORG (Organization)
- LOC (Location)
- MISC (Miscellaneous)

## Usage

The main implementation can be found in `ner_tf.ipynb` notebook. Here's a quick example of how to use the model:

```python
from transformers import pipeline

# Initialize NER pipeline
pipe = pipeline('ner', model='dbmdz/bert-large-cased-finetuned-conll03-english')

# Example text
text = "Apple Inc. is planning to open a new store in San Francisco next year."

# Get predictions
results = pipe(text)
```

## Project Structure

```
NER-with-Transformers/
├── README.md
├── ner_tf.ipynb
└── requirements.txt
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or feedback, please open an issue in this repository.

## Acknowledgments

- Thanks to the Hugging Face team for providing the Transformers library
- Thanks to the DBMDZ team for training and sharing the pre-trained model
