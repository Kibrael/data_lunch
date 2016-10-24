### A resource for getting started in data analytics

1. Install [Homebrew](http://brew.sh)
    - Homebrew is a package manager similar to Pip. It gives a good range of tools for working on Macs, such as an easy install of PostgreSQL.
    - Homebrew requires periodic updates to maintain links to current package versions.     Use ```brew update to ensure you have the most current version.

2. Install Python 3
    - Python 2 works well in most instances, but with large data it is useful to have better supported iteration function (amont other tools). The development of Python as a language is shifting to Python 3 so it will be the more supported tool in the future.
    - Upgrade pip at this point. Pip needs regular upgrading to maintain links to the most current packages
    - ` pip install --upgrade pip `
    - alternatively, depending on your python 3 install, you may need to specify your pip upgrade such as ` pip3 install --upgrade pip `

3. Install PostgreSQL using brew. See [this site](https://www.moncefbelyamani.com/how-to-install-postgresql-on-a-mac-with-homebrew-and-lunchy/) for more instructions.
    - `brew install postgresql`
    - Initializing postgres may take some additional work
    - Additional instructions TBD

4. Install Jupyter notebooks
    - Jupyter notebooks are an in-browser code development tool set. Code is split into cells allowing for fast iteration and graphing of data products. Code can also be easily exported using the nbconvert command:
    - `jupyter nbconvert --to html mynotebook.ipynb`
    - See more on nbconvert [here](https://github.com/jupyter/nbconvert)

5. Check that Pandas, Numpy, Sci-kit Learn are installed using:
    `pip freeze`
    If they are not present, use pip to install them.

