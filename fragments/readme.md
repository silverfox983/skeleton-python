# <div align="center">{{repo}}<br>[![skeleton](https://img.shields.io/badge/{{sref|urlencode|replace("-", "–")}}-skeleton?label=%F0%9F%92%80%20{{skeleton|urlencode}}&labelColor=black&color=grey&link={{skeleton_url|urlencode}})]({{srev}})#% if pypi %# [![Supported Python versions](https://img.shields.io/pypi/pyversions/{{pypi_project}}.svg?logo=python&label=Python)]({{pypi_url}}) [![Package version](https://img.shields.io/pypi/v/{{pypi_project}}?label=PyPI)]({{pypi_url}})#% endif %#</div>

#%- if tests %#

[![Tests]({{repo_url}}/actions/workflows/test.yml/badge.svg)]({{repo_url}}/actions/workflows/test.yml)
#%- endif %#
#%- if tests and public %#
[![Coverage](https://coverage-badge.samuelcolvin.workers.dev/{{github}}/{{repo}}.svg)]({{coverage_url}})
#%- endif %#
#%- if docs %#
[![Documentation Status](https://readthedocs.org/projects/{{rtd}}/badge/?version=latest)](https://{{rtd}}.readthedocs.io/en/latest/?badge=latest)
#%- endif %#
#%- if tidelift %#
[![Lifted?](https://tidelift.com/badges/package/pypi/{{pypi_project}})]({{tidelift_url}}&utm_medium=readme)
#%- endif %#

#%- if wip %#
#% if doc_mode %#
!!! warning
    **Work in Progress**. 🚧

    [Hit the `👁 Watch` button on GitHub]({{repo_url}}) to know when this project is ready to be tried out!
#% else %#
> [!Warning]
> **Work in Progress**. 🚧
>
> Hit the `👁 Watch` button to know when this project is ready to be tried out!
#%- endif %#
#%- endif %#

#% if description -%#
{{description}}
#% endif %#

#%- if tidelift %#

# For Enterprise

| [![Tidelift](https://nedbatchelder.com/pix/Tidelift_Logo_small.png)]({{tidelift_url}}utm_medium=referral&utm_campaign=readme) | [Available as part of the Tidelift Subscription.]({{tidelift_url}}&&utm_medium=referral&utm_campaign=readme)<br>This project and the maintainers of thousands of other packages are working with Tidelift to deliver one enterprise subscription that covers all of the open source you use. [Learn more here]({{tidelift_url}}&utm_medium=referral&utm_campaign=#% if doc_mode %#readthedocs#% else %#github#% endif %#). |
| - | - |

#% include "fragments/security.md" %#
#%- endif %#

#%- if pypi %#
# Installation
#%- else %#
# Installation for Contributors
#%- endif %#

#%- if pypi %#
#%- if cli %#
To use this globally as a CLI tool only, simply install it with [pipx](https://github.com/pypa/pipx):

```shell
pipx install {{pypi_project}}
```

But you might also simply install it with pip to access the library API:

```shell
pip install {{pypi_project}}
```

#%- else %#
You might simply install it with pip:

```shell
pip install {{pypi_project}}
```

#%- endif %#

If you use [Poetry](https://python-poetry.org/), then you might want to run:

```shell
poetry add {{pypi_project}}
```

## For Contributors
#%- endif %#
[![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)
[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/astral-sh/ruff/main/assets/badge/v2.json)](https://github.com/astral-sh/ruff)
#%- if precommit %#
[![Pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
#%- endif %#
#% include "fragments/guide.md" %#

#% if public -%#
For more information on how to contribute, check out [CONTRIBUTING.md]({{repo_url}}/blob/HEAD/CONTRIBUTING.md).<br/>
Always happy to accept contributions! ❤️
#%- endif %#

# Legal Info
© Copyright by {{copyright}} ([@{{author}}](https://github.com/{{author}})).
#%- if license != "Custom" %#
<br />This software is licensed under the terms of [{{license}} License]({{repo_url}}/blob/HEAD/LICENSE).
#%- elif private %#
<br />This software is closed-source. You are not allowed to share any of its contents to anyone under any circumstances.
#% endif %#
