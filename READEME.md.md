# Python/Django

- 1. Install Python3/pip/virtualenv
    
    [Welcome to Python.org](https://www.python.org/)
    
    ```jsx
    //install python3
    sudo apt install python3 or sudo apt upgrade python3
    
    //install pip
    sudo apt install python3-pip
    
    //install virtualenv
    sudo apt install python3-venv or pip install virtualenv
    
    //check versions
    python3 --version && pip --version && virtualenv --version
    ```
    
- 2. Create/acrivate virtualenv
    
    ```jsx
    //create
    virtualenv venv (convention name 'venv')
    
    //activate
    source venv/bin/activate
    
    //deactivate
    deactivate
    ```
    
- 3. Install Django
    
    ```jsx
    pip install django
    ```
    
- 4. Create dependencies
    
    ```jsx
    //show dependencies
    pip freeze
    
    //create file with dependencies
    //after installing any dependency run the folloing command
    pip freeze > requirements.txt
    ```
    
- 5. Python/Django commands
    - Start project (django-admin)
    
    ```jsx
    //Django main commands
    django-admin help
    
    //create setup project folder
    django-admin startproject setup . (setup or config)
    
    //venv interpreter
    //CTRL+SHIFT+P
    //select option with (venv:venv)
    ```
    
    - Run project (python manager.py)
    
    ```jsx
    python3 manage.py help
    
    python manage.py runserver
    ```
    
- 6. Django config
    - setup/setting.py
    
    [Django](https://docs.djangoproject.com/en/4.1/topics/i18n/timezones/)
    
    ```jsx
    LANGUAGE_CODE = 'pt-br'
    TIME_ZONE = 'America/Sao_Paulo'
    ```
    
    - Secret Key
    
    ```jsx
    //install dotenv
    pip install python-dotenv
    //pip-freeze > requirements.txt ***
    //create .env file in project root folder - values without quotation marks ***
    
    //in settings.py import dotenv
    from dotenv import load_dotenv
    //import os from pathlib
    //from pathlib import Path, os
    load_dotenv()
    SECRET_KEY = str(os.getenv('SECRET_KEY'))
    ```
    
- 7. Git
    
    [gitignore.io](https://www.toptal.com/developers/gitignore/)
    
    [](https://www.toptal.com/developers/gitignore/api/django)
    
    ```jsx
    #//create .gitignore in project root folder
    # Created by https://www.toptal.com/developers/gitignore/api/django
    # Edit at https://www.toptal.com/developers/gitignore?templates=django
    
    ### Django ###
    *.log
    *.pot
    *.pyc
    __pycache__/
    local_settings.py
    db.sqlite3
    db.sqlite3-journal
    media
    
    # If your build process includes running collectstatic, then you probably don't need or want to include staticfiles/
    # in your Git repository. Update and uncomment the following line accordingly.
    # <django-project-name>/staticfiles/
    
    ### Django.Python Stack ###
    # Byte-compiled / optimized / DLL files
    *.py[cod]
    *$py.class
    
    # C extensions
    *.so
    
    # Distribution / packaging
    .Python
    build/
    develop-eggs/
    dist/
    downloads/
    eggs/
    .eggs/
    lib/
    lib64/
    parts/
    sdist/
    var/
    wheels/
    share/python-wheels/
    *.egg-info/
    .installed.cfg
    *.egg
    MANIFEST
    
    # PyInstaller
    #  Usually these files are written by a python script from a template
    #  before PyInstaller builds the exe, so as to inject date/other infos into it.
    *.manifest
    *.spec
    
    # Installer logs
    pip-log.txt
    pip-delete-this-directory.txt
    
    # Unit test / coverage reports
    htmlcov/
    .tox/
    .nox/
    .coverage
    .coverage.*
    .cache
    nosetests.xml
    coverage.xml
    *.cover
    *.py,cover
    .hypothesis/
    .pytest_cache/
    cover/
    
    # Translations
    *.mo
    
    # Django stuff:
    
    # Flask stuff:
    instance/
    .webassets-cache
    
    # Scrapy stuff:
    .scrapy
    
    # Sphinx documentation
    docs/_build/
    
    # PyBuilder
    .pybuilder/
    target/
    
    # Jupyter Notebook
    .ipynb_checkpoints
    
    # IPython
    profile_default/
    ipython_config.py
    
    # pyenv
    #   For a library or package, you might want to ignore these files since the code is
    #   intended to run in multiple environments; otherwise, check them in:
    # .python-version
    
    # pipenv
    #   According to pypa/pipenv#598, it is recommended to include Pipfile.lock in version control.
    #   However, in case of collaboration, if having platform-specific dependencies or dependencies
    #   having no cross-platform support, pipenv may install dependencies that don't work, or not
    #   install all needed dependencies.
    #Pipfile.lock
    
    # poetry
    #   Similar to Pipfile.lock, it is generally recommended to include poetry.lock in version control.
    #   This is especially recommended for binary packages to ensure reproducibility, and is more
    #   commonly ignored for libraries.
    #   https://python-poetry.org/docs/basic-usage/#commit-your-poetrylock-file-to-version-control
    #poetry.lock
    
    # pdm
    #   Similar to Pipfile.lock, it is generally recommended to include pdm.lock in version control.
    #pdm.lock
    #   pdm stores project-wide configurations in .pdm.toml, but it is recommended to not include it
    #   in version control.
    #   https://pdm.fming.dev/#use-with-ide
    .pdm.toml
    
    # PEP 582; used by e.g. github.com/David-OConnor/pyflow and github.com/pdm-project/pdm
    __pypackages__/
    
    # Celery stuff
    celerybeat-schedule
    celerybeat.pid
    
    # SageMath parsed files
    *.sage.py
    
    # Environments
    .env
    .venv
    env/
    venv/
    ENV/
    env.bak/
    venv.bak/
    
    # Spyder project settings
    .spyderproject
    .spyproject
    
    # Rope project settings
    .ropeproject
    
    # mkdocs documentation
    /site
    
    # mypy
    .mypy_cache/
    .dmypy.json
    dmypy.json
    
    # Pyre type checker
    .pyre/
    
    # pytype static type analyzer
    .pytype/
    
    # Cython debug symbols
    cython_debug/
    
    # PyCharm
    #  JetBrains specific template is maintained in a separate JetBrains.gitignore that can
    #  be found at https://github.com/github/gitignore/blob/main/Global/JetBrains.gitignore
    #  and can be added to the global gitignore or merged into this file.  For a more nuclear
    #  option (not recommended) you can uncomment the following to ignore the entire idea folder.
    #.idea/
    
    # End of https://www.toptal.com/developers/gitignore/api/django
    ```