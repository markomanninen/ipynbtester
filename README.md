ipynbtester - IPython Notebook test suite
=========================================

Forged from runtests (Matt Davis) gist: https://gist.github.com/jiffyclub/4013594

## Usage on IPython Notebooks

### 1. Load extension and runaway module

```python
%load_ext ipynbtester
```

### 2. Define tests

```python
def test_my_test_ok():
    assert True == True

def test_my_test_fail():
    assert True == False

def test_my_test_error():
    assert True == none
```

### 3. Run tests

```python
%runaway
```

### Output

![ipynbtester](https://raw.githubusercontent.com/markomanninen/ipynbtester/master/test.png "IPython Notebook test results")

## The [MIT](http://choosealicense.com/licenses/mit/) License

Copyright (c) 2014 Marko Manninen