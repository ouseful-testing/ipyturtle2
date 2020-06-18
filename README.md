
# ipyturtle2

Turtle implemention for Jupyter Notebook

## Installation

You can install using `pip`:

```bash
pip install ipyturtle2
```

Or if you use jupyterlab:

```bash
pip install ipyturtle2
jupyter labextension install @jupyter-widgets/jupyterlab-manager
```

If you are using Jupyter Notebook 5.2 or earlier, you may also need to enable
the nbextension:
```bash
jupyter nbextension enable --py [--sys-prefix|--user|--system] ipyturtle2
```

## Development

```bash
docker run --rm -it -p 8888:8888 -v $(pwd):/home/jovyan jupyter/minimal-notebook bash
```

```bash
pip install -e ".[test, examples]"
jupyter nbextension install --sys-prefix --symlink --overwrite --py ipyturtle2
jupyter nbextension enable --sys-prefix --py ipyturtle2
jupyter notebook
```

[http://localhost:8888](http://localhost:8888)

## Publish

```bash
python setup.py sdist bdist_wheel
pip install twine
twine upload dist/ipyturtle2-*
```
