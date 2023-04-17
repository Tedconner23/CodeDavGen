
# README.md

## Installation

To install the required packages, run:

```bash
pip install openai autopep8 jsbeautifier Microsoft.CodeAnalysis.CSharp
```

## Usage

### CLI Arguments

You can use the script with CLI arguments by passing the required parameters as follows:

```bash
python script.py --context "public class Point2D {...}" --instructions "Add a method to the Point2D class that calculates the distance between two points." --language "C#" --platform ".NET" --project_details "A simple 2D point library for .NET applications." --output_folder "output_folder" --output_filename "generated_code.cs"
```

Replace the values of `--context`, `--instructions`, `--language`, `--platform`, `--project_details`, `--output_folder`, and `--output_filename` with your desired values.

### Within Script

You can also use the script by editing the parameters in the `if __name__ == "__main__"` block. Modify the values of `args` dictionary accordingly:

```python
if __name__ == "__main__":
    args = {
        "context": "public class Point2D {...}",
        "instructions": "Add a method to the Point2D class that calculates the distance between two points.",
        "language": "C#",
        "platform": ".NET",
        "project_details": "A simple 2D point library for .NET applications.",
        "output_folder": "output_folder",
        "output_filename": "generated_code.cs",
    }
    # ...
```

After modifying the values, run the script:

```bash
python script.py
```

The generated code will be saved in the specified output folder and filename.
