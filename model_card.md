# Swahili Syllabic Tokenizer

## Model Overview

The Swahili Syllabic Tokenizer is a custom tokenizer designed to tokenize Swahili text into syllables. It is built using a syllabic vocabulary and has a byte fallback mechanism for handling out-of-vocabulary tokens. This tokenizer is compatible with the Hugging Face `transformers` library, making it easy to integrate into NLP pipelines and models.

## Features

- **Syllabic Tokenization**: Breaks down Swahili text into syllables based on a predefined vocabulary.
- **Byte Fallback**: Converts out-of-vocabulary tokens into UTF-8 byte representations.
- **Special Tokens**: Supports special tokens like `<s>`, `<s/>`, `<pad>`, and `<unk>` for compatibility with transformer models.
- **Customizable**: Easily extendable and adaptable for specific NLP tasks.

## Installation

To install the tokenizer, use the following command:

```bash
pip install swahili-tokenizer
```

## Usage
Here is an example of how to use the Swahili Syllabic Tokenizer:

```python
from swahili_tokenizer import SilabiTokenizer

# Load the custom tokenizer
tokenizer = SilabiTokenizer()

# Tokenize text
text = "Mlima wa Kenya unahusu mambo mengi sana."
tokens = tokenizer.tokenize(text)
token_ids = tokenizer.tokens_to_ids(tokens)

print("Tokens:", tokens)
print("Token IDs:", token_ids)

```

## Tokenizer Details

### Vocabulary
The tokenizer uses a predefined syllabic vocabulary, which includes common syllables used in Swahili, as well as special tokens for unknown tokens (<unk>), beginning of sequence (<s>), end of sequence (<s/>), and padding (<pad>). It also includes a fallback mechanism to handle out-of-vocabulary tokens by converting them into their UTF-8 byte representations.

### Special Tokens
- `<unk>`: Unknown token
- `<s>`: Start of sequence
- `<s/>`: End of sequence
- `<pad>`: Padding token

### Tokenization Process
The tokenizer works by iterating through the input text and matching substrings against its vocabulary. If a match is found, the substring is added to the list of tokens. If no match is found, the first character of the substring is converted to its UTF-8 byte representation and added to the list of tokens. This process continues until the entire input text is tokenized.

## License
This project is licensed under the MIT License.

## Citation
If you use this tokenizer in your research, please cite it as follows:
```
@misc{swahili_tokenizer,
  author = {Edwin Ndiritu},
  title = {Swahili Silabi Tokenizer},
  year = {2024},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/nguthiru/silabi-tokenizer}}
}
```
## Contributions
Contributions and suggestions are welcome! Please feel free to open an issue or submit a pull request on the GitHub repository.

## Contact
For any questions or inquiries, please contact:

Name: Edwin Nguthiru
Email: nguthiruedwin@gmail.com
GitHub: nguthiru
