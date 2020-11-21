```
wget https://github.com/qdbp/py9discipline/archive/master.zip \
    && unzip -oj master.zip \
            '*/.pre-commit-config.yaml' \
            '*/mypy.ini' \
    && rm master.zip \
    && pre-commit install --install-hooks \
;
```
