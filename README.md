```
wget https://github.com/qdbp/py9discipline/archive/master.zip \
    && unzip -oj master.zip \
            '*/.pre-commit-config.yaml' \
            '*/mypy.ini' \
            '*/requirements-dev.txt' \
    && rm master.zip \
    && pre-commit install --install-hooks \
    && touch requirements.txt \
    && sed -i '/requirements-dev.txt/d' requirements.txt \
    && echo '-r requirements-dev.txt' >> requirements.txt \
;
```

## Manual setup:

- make sure your venv is symlinked to `.venv`
- pip-install the dev requirements.
- mypy: change `src` to your desired targets.
