# markdown2html.py Documentation

`markdown2html.py` is a script that converts Markdown files into HTML files, handling headings, lists, text formatting, and custom tags.

---

## Requirements

### 1. `README.md` File
   - **Requirement**: A `README.md` file must be present contain documentation.
   - **Instructions**: Ensure `README.md` exists in the root of your project and is not empty.
   - **Verification Command**:
     ```bash
     test -s README.md && echo "README.md exists and is not empty" || echo "README.md missing or empty"
     ```
   - **Expected Result**: The command should output "`README.md exists and is not empty`".

### 2. First Line Shebang
   - **Requirement**: The first line of `markdown2html.py` must contain the shebang:
     ```bash
     #!/usr/bin/python3
     ```
   - **Instructions**: Confirm that this line is at the top of `markdown2html.py`.
   - **Verification Command**:
     ```bash
     head -n 1 markdown2html.py
     ```
   - **Expected Result**: The command should output `#!/usr/bin/python3`.

### 3. Documentation for `markdown2html.py`
   - **Requirement**: The script must be well-documented, explaining each function and the purpose of the script.
   - **Instructions**: Add a top-level docstring and docstrings for each function.
   - **Example Docstring**:
     ```python
     """
     markdown2html.py

     A script that converts Markdown text files to HTML files.
     """
     ```
   - **Expected Result**: Open `markdown2html.py` and verify docstrings for overall functionality and individual functions.

---

## Test Cases

Each test case below verifies that `markdown2html.py` handles arguments and file requirements correctly.

### Case 1: No Arguments
   - **Command**:
     ```bash
     ./markdown2html.py
     ```
   - **Expected Output**:
     ```
     Usage: ./markdown2html.py README.md README.html
     ```
   - **Instructions**: Run `markdown2html.py` without arguments to ensure it prompts with usage instructions.
   - **Expected Score**: 1 out of 1 if successful.

### Case 2: One Argument
   - **Command**:
     ```bash
     ./markdown2html.py bla.md
     ```
   - **Expected Output**:
     ```
     Usage: ./markdown2html.py README.md README.html
     ```
   - **Instructions**: Run `markdown2html.py` with a single argument to verify that it prompts for missing arguments.
   - **Expected Score**: 1 out of 1 if successful.

### Case 3: Nonexistent Input File
   - **Command**:
     ```bash
     ./markdown2html.py bla.md blu.html
     ```
   - **Expected Output**:
     ```
     Missing bla.md
     ```
   - **Instructions**: Ensure the `bla.md` file does not exist, then run the command to check for the "Missing" message.
   - **Expected Score**: 1 out of 1 if successful.

### Case 4: Valid Input and Output Files
   - **Command**:
     ```bash
     echo "Sample Markdown Content" > bla.md
     ./markdown2html.py bla.md blu.html
     ```
   - **Instructions**: Create a `bla.md` file with sample content. Run the command and check that `blu.html` is generated with the expected content.
   - **Expected Score**: 1 out of 1 if successful.

---

## PEP 8 Compliance

### Requirement
   - **Requirement**: The code should follow PEP 8 guidelines for readability and maintainability.
   - **Instructions**: Use a linter like `pycodestyle` or `flake8` to check PEP 8 compliance.
   - **Verification Command**:
     ```bash
     pycodestyle markdown2html.py
     ```
   - **Expected Result**: No PEP 8 errors should be reported.

---

## Example Usage

```bash
# Convert a markdown file to HTML
./markdown2html.py input.md output.html
