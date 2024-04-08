## Logging
### Tests

If you've got passing tests but still want to see the output of logging etc. then you can use the following: `pytest -rP`
## Arrays

To check whether an array contains a specified value, you can use the `in` keyword like so:

```python
if my_value in my_array:
```

## Lambdas

They can be a bit annoying to work with, given they don't really support multi-line functions in the same way that JS/TS would. Therefore, it's usually better to define a named function elsewhere (even if it's just a little bit further up in the code) and then call that in the lambda.

 Otherwise, you'll spend a load of time banging your head against a wall trying to work out the correct syntax - whether it's `()` or `[]` to wrap the code-block in etc.