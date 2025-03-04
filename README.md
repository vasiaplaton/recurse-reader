# RecurseReader CLI Utility

RecurseReader is a powerful and user-friendly command-line tool for recursively traversing directories to print file paths and their contents. It is designed with flexibility in mind, offering robust filtering and output options to suit a wide range of use cases.

## Features 🚀
- **Recursive Traversal**: Walk through directories and list files along with their contents.
- **Dot Directory Filtering**: Optionally ignore directories starting with a dot (e.g., `.git`).
- **Hidden File Support**: Choose whether to include hidden files (starting with a dot) in the output.
- **Depth Limitation**: Control how deep the traversal goes.
- **Logging**: Save the output to a log file for later review.
- **Encoding Safety**: Handle files with different encodings gracefully.

## Installation 📦
Ensure you have Python 3.8+ installed on your system. Clone the repository and use the script directly:
```bash
git clone https://github.com/your-repo/recurse-reader.git
cd recurse-reader
python recurse_reader.py --help
```

## Usage 🛠️
RecurseReader offers a variety of command-line arguments to customize its behavior. Here are some examples:

### Basic Usage
Traverse a directory and display file paths and contents:
```bash
python recurse_reader.py /path/to/directory
```

### Ignore Dot Directories
Skip directories that start with a dot:
```bash
python recurse_reader.py /path/to/directory --ignore-dot-dirs
```

### Include Hidden Files
Include hidden files in the output:
```bash
python recurse_reader.py /path/to/directory --show-hidden-files
```

### Limit Depth
Restrict the depth of traversal to two levels:
```bash
python recurse_reader.py /path/to/directory --max-depth 2
```

### Log Output to File
Save the output to a log file:
```bash
python recurse_reader.py /path/to/directory --log-to-file output.log
```

## Full Argument Reference 🗂️
```plaintext
usage: recursereader [-h] [--ignore-dot-dirs] [--show-hidden-files] [--max-depth MAX_DEPTH] [--gitignore GITIGNORE]
                     [--ignore-subfolders IGNORE_SUBFOLDERS [IGNORE_SUBFOLDERS ...]] [--log-to-file LOG_TO_FILE]
                     root_dir

Recursively print file paths and contents from a directory.

positional arguments:
  root_dir              The root directory to start the search.

options:
  -h, --help            show this help message and exit
  --ignore-dot-dirs     Ignore directories starting with a dot (e.g., '.git').
  --show-hidden-files   Include hidden files (files starting with a dot) in the output.
  --max-depth MAX_DEPTH
                        Maximum depth to traverse (e.g., 2 for two levels deep).
  --gitignore GITIGNORE
                        Path to a .gitignore-like file with patterns to ignore.
  --ignore-subfolders IGNORE_SUBFOLDERS [IGNORE_SUBFOLDERS ...]
                        Specific subfolders to ignore (provide a space-separated list).
  --log-to-file LOG_TO_FILE
                        Specify a file to log the output instead of printing to the console.

```

## Example Output ✨
Here is what the output might look like when running RecurseReader:
```plaintext
Path: /example/project/README.md
Contents:
# Welcome to My Project

---
Path: /example/project/src/main.py
Contents:
print("Hello, World!")

---
```

## License 📜
RecurseReader is licensed under the MIT License.

## Contributing 🤝
We welcome contributions! Feel free to submit issues or pull requests to improve RecurseReader.
