# example_project

This is a example project for packaging a python project.

Clone this repository
```
git clone https://github.com/Brownian-Motion-99/example_project.git
```
Create a new virtual environment
```
# use conda as the example here
conda create -n example_project_env
```
```
conda activate example_project_env
```
```
conda install -c conda-forge python pytest numpy
```

## Unit testing
This repository use ```pytest``` as the unit testing framework.
```
cd example_project
```
```
# run unit tests
python -m pytest tests/
```
You may modify the source code and see how the outcome of unit testing changes.

## Generating distribution archives
We use ```build``` to generate the distribution archives.
```
# upgrade to the latest version
python -m pip install --upgrade build
```
```
# run this command at the project root directory
python -m build
```
After the building process is done, you will see the distribution archives stored in ```dist``` folder.
```
dist
├── example_package_bm99-0.0.1-py3-none-any.whl
└── example_package_bm99-0.0.1.tar.gz
```

## Uploading the distribution archives to PyPI
We use ```twine``` to upload the distribution archives.

Before you upload the files, you have to create an account on TestPyPI, then follow the instruction on TestPyPI to finish necessary configurations.
TestPyPI: https://test.pypi.org/

After the necessary configurations are done, you are ready to upload your first package.
```
# upgrade to the latest version
python3 -m pip install --upgrade twine
```
```
# run this command at the project root directory
python3 -m twine upload --repository testpypi dist/*
```

## Notes
```Pytest```: https://docs.pytest.org/en/stable/

This implementation is done following the official tutorial, this repository only provides BASIC instruction and doesn't guarantee the practicability. So before starting your own implementation, make sure you have read the official tutorial.
https://packaging.python.org/en/latest/tutorials/packaging-projects/






