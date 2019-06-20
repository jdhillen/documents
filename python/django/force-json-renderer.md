[Force JSON Renderer](https://stackoverflow.com/a/45498990)
===

Add to `settings.py`

```python
# ==|== Force JSON render of API Calls =============================================================
REST_FRAMEWORK = {
    'DEFAULT_RENDERER_CLASSES': (
        'rest_framework.renderers.JSONRenderer',
    ),
    'DEFAULT_PARSER_CLASSES': (
        'rest_framework.parsers.JSONParser',
    )
}
```
