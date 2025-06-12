# Contributing

Contributions are welcome and are greatly appreciated! Every little bit helps, and credit will always be given.

You can contribute to the project in the following ways:

- Report bugs and errors
- Suggest improvements and new features
- Write documentation
- Write code
- Write tests

## Writing code

To write code, you can use the following steps:

1. Fork the repository into your own GitHub account/organization.
2. Clone the repository to your local machine and checkout a new branch for the contribution you're working on.
3. Make your changes and commit them.
4. Push your changes to the relevant branch in your fork.
5. Create a pull request on GitHub to the development branch of the main repository. Pull requests to the production branch will not be accepted.


It is recommended to use a virtual environment to write code. The project uses uv for this purpose, but you can use any other virtual environment manager. 
You are however required to use uv to install the dependencies and to run the tests. You can install uv using pipx, or checkout the [official installation guide](https://docs.astral.sh/uv/installation/).

```sh
pipx install uv
```

```sh
uv sync
```

## Writing Documentation

Documentation is always welcome! You can contribute to the documentation by writing documentation for the code you write or by improving the existing documentation.

Documentation is written in the `docs/source` folder and is written in [`MyST Markdown`](https://myst-parser.readthedocs.io/en/latest/), which is a dialect of Markdown that is compatible with Sphinx. 

If you're writing docs, make sure to install the docs dependencies.

```sh
uv sync # install all dependencies, docs is included in the default list of groups to install

# OR

uv sync --group docs
```

You can then build the documentation locally using sphinx.

```sh
uv run sphinx-build -b html docs/source docs/build
```

You can then view the documentation locally by opening the `docs/build/index.html` file in your browser.
