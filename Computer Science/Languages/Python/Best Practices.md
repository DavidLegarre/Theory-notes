```toc
```

## Where to store API Keys/Tokens

The best practice would be to create a blank file, e.g.:  `Constants.py`  and store in it:
```python
API_KEY = "ABCABCABC"
```

Then in the file you want to use the keys:

```python
import Constants

service_key = constants.API_KEY
```
