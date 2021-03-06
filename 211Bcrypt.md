#Bcrypt, Django Style!

In your Django `virtualenv`:

```terminal
(djangoEnv)>pip install bcrypt
```

This should be getting familiar... checkout the [documentation](https://pypi.python.org/pypi/bcrypt/2.0.0)!


After you have pip installed try the following:

```terminal
(djangoenv)>python
>>> import bcrypt
>>> password = b"super secret password"
>>> hashed = bcrypt.hashpw(password, bcrypt.gensalt())
>>> print hashed
>>> print len(hashed)
>>> exit()
```

Should you run into an **encoding** error when you're hashing passwords with `bcrypt`, the following method might be useful:

+[`your_string.encode()`](https://docs.python.org/3/library/stdtypes.html#str.encode)
