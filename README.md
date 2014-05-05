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
    assert True == None
```

### 3. Run tests

```python
%runaway
```

### Output

```text
Collected 2 tests.

Test function name | Status
---------------------------
test_my_test_fail  | failed
test_my_test_error | error
test_my_test_ok    | successful
---------------------------
Failed             |
test_my_test_fail  | AssertionError()
---------------------------
Errors             |
test_my_test_error | NameError("global name 'none' is not defined",)
---------------------------
        Successful | 1
            Failed | 1
            Errors | 1
         Execution | 0.001 seconds
```

## The [MIT](http://choosealicense.com/licenses/mit/) License

Copyright (c) 2014 Marko Manninen