# datasette-hmf2-vis

[![PyPI](https://img.shields.io/pypi/v/datasette-hmf2-vis.svg)](https://pypi.org/project/datasette-hmf2-vis/)
[![Changelog](https://img.shields.io/github/v/release/hcarter333/datasette-hmf2-vis?include_prereleases&label=changelog)](https://github.com/hcarter333/datasette-hmf2-vis/releases)
[![Tests](https://github.com/hcarter333/datasette-hmf2-vis/actions/workflows/test.yml/badge.svg)](https://github.com/hcarter333/datasette-hmf2-vis/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/hcarter333/datasette-hmf2-vis/blob/main/LICENSE)

Visualizes hmF2 data from various instruments using czml loaded Cesium maps

## Installation

Install this plugin in the same environment as Datasette.
```bash
datasette install datasette-hmf2-vis
```
## Usage

To start datasette for the largish db use:

```python3 -m datasette glotec.db --plugins-dir=plugins --template-dir plugins/templates --root --static assets:static-files/ --setting sql_time_limit_ms 17000 --setting max_returned_rows 100000```

## Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:
```bash
cd datasette-hmf2-vis
python -m venv venv
source venv/bin/activate
```
Now install the dependencies and test dependencies:
```bash
pip install -e '.[test]'
```
To run the tests:
```bash
python -m pytest
```
