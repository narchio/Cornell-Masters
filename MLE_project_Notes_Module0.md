## My notes for Module 0

### Set Up (venv)
activate venv
```
source venv/bin/activate
```

### Testing 
```
python3 run_tests.py {optional specific test argument}
```

filters: (first to run a task, second is to find a specific test)
```
python3 -m pytest tests/ -m task0_1 
python3 -m pytest tests/ -k test_sum 
```

### Unit Tests
assert v.s. assert_close
assert is a boolean compare so use assert_close

ex. unit test for relu()
    enumerate through all nums 0 -> n, assert that relu(current_num) is 1
    enumerate through all nums -n -> 0, assert that relu(current_num) is 0
    ** but.. how can that happen? property is right but takes too much time 

    QuickCheck (Hypothesis) 
        - basically randomizes small floats for example, and we just simply check properties


### Other

Higher Order functions
```
def combine3(fn): 
    def apply(a, b, c): 
        return fn(fn(a, b), c)
    return apply
```




