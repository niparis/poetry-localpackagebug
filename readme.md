# Demonstrates local package installation with poetry 1.1.4

Steps

## ** with poetry 1.1.4** [fails]

install poetry 1.1.4

```
poetry self update 1.1.4
```

```
cd service
poetry update
poetry install
```

then try to import "library1", get an import error

```
poetry shell
python 

>>> import library1
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ModuleNotFoundError: No module named 'library1'
>>> 
```

## ** with poetry 1.0.9** [works]

install poetry 1.0.9

```
poetry self update 1.0.9
```

Delete the lockfile and the virtualenvironment


```
cd service
rm poetry.lock
poetry env remove python3.8

poetry update
poetry install
```

Then try to import library1, works

```
poetry shell
python 

>>> import library1
>>> 
```


