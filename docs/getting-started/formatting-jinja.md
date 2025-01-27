---
sidebar_position: 4
---

# Formatting Jinja

sqlfmt loves properly-formatted jinja, too.

sqlfmt will safely attempt to import the Python code formatter, *black*. If it is successful (either because sqlfmt was installed with the `jinjafmt` extra or because *black* was installed separately in the same environment), it will use *black* to format the contents of jinja tags. 

If you do not want sqlfmt to use *black* to format your jinja, then specify the `--no-jinjafmt` flag when running sqlfmt.

Installing sqlfmt with the jinjafmt extra will also install *black*. You can do this with `pipx install sqlfmt[jinjafmt]`. If you want to pin a specific *black* version, you should specify that separately, as a direct dependency of your project (in your `Pipfile`, `pyproject.toml`, etc.).

If sqlfmt was installed without the jinjafmt extra, and *black* is not otherwise installed, then sqlfmt will not attempt to format the contents of jinja tags, except for enforcing a single space inside each curly.
