# README.md

## codedavinci002.py

A Python script that generates code using OpenAI's Code Davinci 002 engine. It supports various programming languages, including Python, JavaScript, and C#. The generated code is then beautified using appropriate formatters before being saved to a file. Additionally, the script provides functionality to abbreviate names in the code context and prompt for better token efficiency.

### Installation

```bash
pip install openai autopep8 jsbeautifier aiohttp
```

### How to use

#### As CLI arguments

```bash
python codedavinci002.py --context_file "context.txt" --instructions "Add a method to the Point2D class that calculates the distance between." --language "C#" --platform ".NET" --project_details "A simple 2D point library for .NET applications." --output_folder "output_folder" --output_filename "generated_code.cs"
```

#### Within the script

Modify the `args` dictionary in the `main()` function:

```python
args = {
    "context_file": "context.txt",
    "instructions": "Add a method to the Point2D class that calculates the distance between.",
    "language": "C#",
    "platform": ".NET",
    "project_details": "A simple 2D point library for .NET applications.",
    "output_folder": "output_folder",
    "output_filename": "generated_code.cs",
}
```

Then run the script:

```bash
python codedavinci002.py
```

The generated code will be saved in the specified output folder and file.

### Advanced usage

Now you can use the `--abbreviate` flag when running the script from the command line, and the function will abbreviate names in both the code context and the prompt for better token efficiency.

```bash
python codedavinci002.py context.txt "Add a method to the Point2D class that calculates the distance .NET "A simple 2D point library for .NET applications." output_folder generated_code.cs --abbreviate
```
