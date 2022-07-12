# Text Summarizer

Extractive text summarizer that extracts key sentences based on word frequency with weights on given keywords.

## Getting Started
The required libraries can be installed with:  

```
pip install -r Requirements.txt
```

## Usage

The default summarization method is to extract sentences that include high frequency words. 

```python
>>> from text_summarizer import Summarizer
>>> Summarizer(doc).summarize()
```

When n is specified, the summarizer extracts n important sentences.

```python
>>> from text_summarizer import Summarizer
>>> Summarizer(doc).summarize(n=10)
```

The weight affects the threshold to extract sentences.

```python
>>> from text_summarizer import Summarizer
>>> Summarizer(doc).summarize(weight=1.5)
```

A lisf of keywords can also be specified for extra weighting.

```python
>>> from text_summarizer import Summarizer
>>> keywords = ['some', 'important', 'words']
>>> Summarizer(doc, keywords, keyweight=2).summarize(weight=1.5)
```
