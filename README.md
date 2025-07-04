# Building

Build this project with the following commands: 

```bash
python -m venv .venv
source .venv/bin/activate 
python -m pip install -r requirements.txt --no-build-isolation
python -m pip install torch-scatter torch-sparse -f https://data.pyg.org/whl/torch-2.7.1+cu126.html --no-build-isolation
```

The version of Python I used was 3.13.3. If any of your commands fail above, you can investigate either (1) changing your Python version to match mine, or (2) editing the `requirements.txt` file to remove exact versions. For example, try replacing `==` with `>=`, or try removing the `==${version}` parts altogether. For whatever reason, `torch-scatter` and `torch-sparse` cannot be added to the `requirements.txt` list like the other packages; if these two packages give you problems, then installing them from source may work for you, as it did for me one time. (Also, note that `venv` isn't required, and can be easily replaced by other methods like Conda/Miniconda or otherwise directly installing the packages to the global environment.) 
