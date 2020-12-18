# [Time Input Formats](https://stackoverflow.com/questions/48514222/django-admin-datetimefield-showing-24hr-format-time/48521723)

The following snippet converts 24 hour military time to 12 hour local time and goes in the settings.py

```python
# ==|== Time Input Formats =========================================================================
TIME_INPUT_FORMATS = [
    '%I:%M:%S %p',  # 6:22:44 PM
    '%I:%M %p',     # 6:22 PM
    '%I %p',        # 6 PM
    '%H:%M:%S',     # '14:30:59'
    '%H:%M:%S.%f',  # '14:30:59.000200'
    '%H:%M',        # '14:30'
]
```
