Todo this, we just need to use the `Blueprint` class that can be imported through the main package:
```python
from flask import Blueprint
```

After that, we can use the blueprint object to map the routes that we are going to use. We also need to initialize the `Blueprint` class with a series of parameters that further improve the chunking of code:
```python
bp = Blueprint('name_of_the_blueprint', __name__, kwargs...)
```

Then, we can use the `bp` object just like we use the `app` instance in the main application. Example:

```python
@bp.route('/')
def index():
    return 'Hello World'
```

Finally, we just need to register the blueprint in the main application. To do this, we use the method `register_blueprint` in the `app` instance:

```python
def create_app():
    app = Flask(__name__)
    # The rest of the logic...

    from . import <file_name>

    app.register_blueprint(<file_name>.bp)
```