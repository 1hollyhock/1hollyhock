Project 구조

```text
project/
├─ tokenizers/
│  ├─ __init__.py
│  ├─ base.py             # Tokenizer abstract class
│  ├─ word.py             # WordTokenizer
│  ├─ char.py             # CharTokenizer
│  └─ bpe.py              # BPETokenizer
├─ tests/
│  ├─ test_bpe.py
│  ├─ test_char.py
│  ├─ test_evaluator.py
│  ├─ test_integration.py
│  └─ test_word.py
├─ evaluator.py
├─ run_experiment.py
├─ data.txt               # Corpus
├─ README.md
└─ requirements.txt       # (pytest)
```

지원하는 tokenizer
- **WordTokenizer** (단어 단위)
- **CharTokenizer** (글자 단위)
- **BPETokenizer** (Byte Pair Encoding, 서브워드 단위)

pytest 설치
- pip install -r requirements.txt

Evaluation 실행
- python run_experiment.py --bpe_merges 50 --corpus data.txt --out results.json
