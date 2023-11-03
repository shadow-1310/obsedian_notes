### errors
---
#### corpora/wordnet not found
- [github discussion](https://github.com/nltk/nltk/issues/3028)
```text
LookupError: 
**********************************************************************
  Resource 'corpora/wordnet' not found.  Please use the NLTK
  Downloader to obtain the resource:  >>> nltk.download()
  Searched in:
    - '/root/nltk_data'
    - '/usr/share/nltk_data'
    - '/usr/local/share/nltk_data'
    - '/usr/lib/nltk_data'
    - '/usr/local/lib/nltk_data'
**********************************************************************
```

- first do download wordnet
```python
import nltk
nltk.download('wordnet')
```

- unzip wordnet from /usr/share/nltk_data
```bash
unzip /usr/share/nltk_data/corpora/wordnet.zip -d /usr/share/nltk_data/corpora/
```
