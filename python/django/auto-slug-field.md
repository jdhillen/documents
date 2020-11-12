# [Auto Slug Field](https://github.com/justinmayer/django-autoslug)

First - Install django-autoslug

```python
pipenv install django-autoslug
```

Second - Add the autoslug field to your Imports inside your Model

```python
# ==|== Imports ====================================================================================
from autoslug import AutoSlugField
```

Third - Add the autoslug field to a class inside your Model

```python
# ==|== Example ====================================================================================
class Example(models.Model):
    def __str__(self):
        return self.name

    class Meta:
        verbose_name = "Example"
        verbose_name_plural = "Examples"

    name = models.CharField(max_length=255)
    slug = AutoSlugField(populate_from='name', always_update=True)
```
