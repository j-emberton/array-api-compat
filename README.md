# NumPy Array API compatibility library

This is a small wrapper around NumPy that is compatible with the [Array API
standard](https://data-apis.org/array-api/latest/). See also [NEP 47](https://numpy.org/neps/nep-0047-array-api-standard.html).

Unlike `numpy.array_api`, this is not a strict minimal implementation of the
Array API, but rather just an extension of the main NumPy namespace with
changes needed to be compliant with the Array API. See
https://numpy.org/doc/stable/reference/array_api.html for a full list of
changes. In particular, unlike `numpy.array_api`, this package does not use a
separate Array object, but rather just uses `numpy.ndarray` directly.

Note that some of the functionality in this library is backwards incompatible
with NumPy.

Library authors using the Array API may wish to test against `numpy.array_api`
to ensure they are not using functionality outside of the standard, but prefer
this implementation for end users who use NumPy arrays.

## Usage

To use this library replace

```py
import numpy as np
```

with

```py
import numpy_array_api_compat as np
```
