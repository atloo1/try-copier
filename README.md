# try-copier

try updating from this remote

```
copier \
    copy \
    https://github.com/atloo1/try-copier \
    test-try-copier \
    -d project_description='test updating from try-copier' \
    -d project_name_kebab_case='test-try-copier' \
    --defaults \
    --trust
cd test-try-copier/
uv run python -m src.test_try_copier.main
uv run pytest tests/main_test.py
```

```
cd test-try-copier/
copier update --defaults --trust
uv run python -m src.test_try_copier.main
uv run pytest tests/main_test.py
```
