### A resource for getting started in data analytics

1. Install [Homebrew](http://brew.sh)
    - Homebrew is a package manager similar to Pip. It gives a good range of tools for working on Macs, such as an easy install of PostgreSQL.
    - Homebrew requires periodic updates to maintain links to current package versions.     Use ```brew update to ensure you have the most current version.

2. Install Python 3
    - Python 2 works well in most instances, but with large data it is useful to have better supported iteration function (amont other tools). The development of Python as a language is shifting to Python 3 so it will be the more supported tool in the future.
    - Upgrade pip at this point. Pip needs regular upgrading to maintain links to the most current packages
    - ` pip install --upgrade pip `
    - alternatively, depending on your python 3 install, you may need to specify your pip upgrade such as:
    -  ` pip3 install --upgrade pip `

3. Install PostgreSQL using brew. See [this site](https://www.moncefbelyamani.com/how-to-install-postgresql-on-a-mac-with-homebrew-and-lunchy/) for more instructions.
    - `brew install postgresql`
    - After postgres is installed, initialization is required before using PostgreSQL
        `initdb /usr/local/var/postgres`
    - Additional documentation is available [here](https://www.postgresql.org/docs/9.5/static/app-initdb.html)
    - Install [Psycopg2](http://initd.org/psycopg/docs/install.html) to use Python with Postgres:
        `pip install psycopg2`


4. Install Jupyter notebooks
    - Jupyter notebooks are an in-browser code development tool set. Code is split into cells allowing for fast iteration and graphing of data products. To start notebooks enter the following command into the terminal window:
        `jupyter notebook`
    A new browser tab will open showing the notebook directory. If both python 2 and 3 are installed you will have the option of choosing what type of notebook to create.
    - Code can also be easily exported using the nbconvert command:
     `jupyter nbconvert --to html mynotebook.ipynb`
    - See more on nbconvert [here](https://github.com/jupyter/nbconvert)

5. Check that [Pandas](http://pandas.pydata.org/pandas-docs/stable/), [Numpy](https://docs.scipy.org/doc/), [Sci-kit Learn](http://scikit-learn.org/stable/documentation.html) and [matplotlib](http://matplotlib.org/contents.html)are installed using:
    `pip freeze`
    - If they are not present, use pip to install them. These packages are the base set of python tools for data analysis and visualizaiton.
    - [bokeh](http://bokeh.pydata.org/en/latest/) provides an alternative in-browser visualization library, but does not allow graphics to be saved as .png or .jpg files.

6. Installing and using virtual environments [additional info on virtual environments](https://virtualenv.pypa.io/en/stable/)
    - Virtual environments allow segregation of projects and project requirements. Meaning that different modules or libraries are available in the established virtual space of projects allowing for cleaner requirements install and memory management.
    - For Python 2 install the virtual environment software:
        `pip install virtualenv'
    - To use the virtual environment navigate to the project directory and type the following:
        `source venv/bin/activate`
    - To deactivate the virtual environment type the following:
        `deactivate`
    - To produce a file with all installed packages in the virtual environment:
        `pip freeze > requirements.txt`
    - To install package requirements from a file:
        `pip install -r requirements.txt`

    - For Python 3:
        - Instructions TBD (I haven't used them in Python 3 yet)
7. GitHub and Bash
8. Stata/SASS


