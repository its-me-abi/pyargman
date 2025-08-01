# pyargman

**pyargman** is a lightweight Python module for managing command-line arguments,


## Features

- **Simple API** for building command-line arguments
- **Supports duplicate and boolean arguments**
- **Easy conversion to CLI list or string format**

## Installation

Install pyargman using pip:

```bash
pip install pyargman
```
install from github

```
git clone https://github.com/its-me-abi/pyargman.git
cd pyargman
```

## Quick Start

Below is an example demonstrating how to use pyargman to manage and convert CLI arguments:

```python
from pyargman import ArgManager

# Initialize argument manager for a CLI command (e.g., "java")
a = ArgManager("java")

# Add arguments
a.set_arg("--helo_duplicate", 1)
a.set_arg("--helo_duplicate", 2)  # Supports duplicate arguments
a.set_arg("--helo_boolean_value", True)  # Argument without a value
a.set_arg("script_path_like", True)

# Convert arguments to list and string formats
print("Converted to CLI list:", a.tolist())
print("Converted to CLI string:", a.toString())
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

Developed and maintained by [its-me-abi](https://github.com/its-me-abi).