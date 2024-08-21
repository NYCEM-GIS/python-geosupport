# python-geosupport 

[![PyPI version](https://img.shields.io/pypi/v/python-geosupport.svg)](https://pypi.python.org/pypi/python-geosupport/) [![Python 2.7 | 3.4+](https://img.shields.io/badge/python-2.7%20%7C%203.4+-blue.svg)](https://www.python.org/downloads/release/python-360/) 

Fork of the [python-geosupport from ishiland](https://github.com/ishiland/python-geosupport).\
Python bindings for NYC Planning's [Geosupport Desktop Edition](https://www1.nyc.gov/site/planning/data-maps/open-data/dwn-gde-home.page).

### [Read the docs](https://python-geosupport.readthedocs.io/en/latest/) 

## Installation

Clone this repository, `cd` into it and:

```commandline
$ pip install .
```

## Environment Variables

By default, a clean installation of Geosupport Desktop Edition will set the appropriate environmental variables. If you are experiencing issues setting up your environment, you will want to ensure the following environment variables are set.

- **GEOFILES**: Path to the *fls* directory of Geosupport. Example: ``C:\Program Files (x86)\Geosupport Desktop Edition\fls\``

- **PATH**: Add the *bin* directory of Geosupport to the *path* variable. Example: ``C:\Program Files (x86)\Geosupport Desktop Edition\bin``

Alternatively see the :ref:`configuration` section for other (easier) options on specifying a path to the Geosupport directory.

## Quickstart

```python
# Import the library and create a `Geosupport` object.
from geosupport import Geosupport
g = Geosupport()

# Call the address processing function by name
result = g.address(house_number=125, street_name='Worth St', borough_code='Mn')
```

`result` is a dictionary with the output from Geosupport. For example:

```
{
    '2010 Census Block': '1012',
    '2010 Census Tract': '31',
    'Assembly District': '65',
    'Atomic Polygon': '112',
    'B10SC - First Borough and Street Code': '14549001010',
    'BOE Preferred B7SC': '14549001',
    'BOE Preferred Street Name': 'WORTH STREET',
    'BOROUGH BLOCK LOT (BBL)': {
        'BOROUGH BLOCK LOT (BBL)': '1001680032',
        'Borough Code': '1',
        'Tax Block': '00168',
        'Tax Lot': '0032'
    },
    'Blockface ID': '0212261942',
    ...
}
```

## License

This project is licensed under the MIT License - see the [license.txt](license.txt) file for details

## Contributors
Thanks to [Jeremy Neiman](https://github.com/docmarionum1) for a major revision incorporating all Geosupport functions and parameters.

If you see an issue or would like to contribute, pull requests are welcome.
