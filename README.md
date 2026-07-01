# HATEDEMICS Models and Data
This repository contains resources developed within the [HATEDEMICS project](https://hatedemics.eu/), including models and annotated datasets for hate speech and check-worthiness detection in English, Spanish, Polish, and Italian.

## Contents

- Final versions of hate speech detection models
- Final versions of check-worthiness detection models
- Human-annotated datasets
- LLM-annotated datasets
- Documentation on labels, data format, and model usage

## Languages

The repository currently includes resources for:

- English
- Spanish
- Polish
- Italian

## Tasks

### Hate Speech Detection

Models and annotations for identifying hate speech in online content.

### Check-Worthiness Detection

Models and annotations for identifying claims or messages that may be relevant for fact-checking.


## Models

The released models were developed using [MaChAmp](https://github.com/machamp-nlp/machamp). 
We provide final models for hate speech and check-worthiness detection in English, Spanish, Polish, and Italian.

The released models are fine-tuned versions of existing pre-trained models. Each model was fine-tuned on the corresponding annotated data released in the `data/` directory. The MaChAmp configuration files used for training are provided in the `configs/` directory.
### Released Models

| Task | Language | Base model | Training data |
|---|---|---|---|
| Hate speech detection | Italian | `MilaNLProc/hate-ita` | Human-annotated Italian Telegram data |
| Hate speech detection | Polish | `ptaszynski/bert-base-polish-cyberbullying` | Human-annotated Polish Telegram data |
| Hate speech detection | English | `facebook/roberta-hate-speech-dynabench-r4-target` | LLM-annotated English Telegram data |
| Hate speech detection | Spanish | `dccuchile/bert-base-spanish-wwm-uncased` | LLM-annotated Spanish Telegram data |
| Check-worthiness detection | Italian | `Musixmatch/umberto-commoncrawl-cased-v1` | Human-annotated Italian Telegram data |
| Check-worthiness detection | Polish | `[base model to be specified]` | Human-annotated Polish Telegram data |
| Check-worthiness detection | English | `xlm-roberta-large` | Italian/Polish in-domain Telegram data and English/Spanish out-of-domain data |
| Check-worthiness detection | Spanish | `xlm-roberta-large` | Italian/Polish in-domain Telegram data and English/Spanish out-of-domain data |



## Repository Organization

The repository is organized around the three main types of released resources: annotated data, fine-tuned models, and MaChAmp configuration files.

```text
.
├── data/
│   ├── human_annotated/
│   └── llm_annotated/
├── models/
│   ├── hate_speech/
│   └── check_worthiness/
├── configs/
│   ├── datasets/
│   └── parameters/
├── docs/
└── README.md
```