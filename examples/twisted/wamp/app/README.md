## Hello WAMP

Run a WAMP router listening on `ws://localhost:8080/ws`, e.g. Crossbar.io:

```shell
crossbar init
crossbar start
```

Start the app component:

```shell
python hello.py
```

Open `hello.html` in your browser.


### Dev. Notes

For hacking on Autobahn library code while running this example, there are 2 options.

Either insert the following at the beginning of the `hello.py`:

```python
import sys
sys.path.insert(0, "../../../../autobahn")
```

or run the example by doing:

```shell
PYTHONPATH=../../../../autobahn python hello.py
```

Note that in the latter case, you must remove any installed Autobahn from your Python (since PYTHONPATH will be *appended* to the Python module search path).

