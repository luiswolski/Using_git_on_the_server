# Using_git_on_the_server
## In your server :desktop_computer:

```
mkdir repository
```
* Verify if your repository is created
```
ls
```
* Enter in repository
```
cd repository
```
* Create git
```
git init --bare
```
* Come back to server home
```
cd ..ls
```
* Now go to you project directory
```
cd yourproject
```
* Initialize git there
```
git init
```
* Connecting these two directories
```
git remote add origin /home/YOUR_USER_NAME/repository/
```
* Add files
```
git add .
```
* Now create te .gitignore
```
nano .gitignore
```
* Past this file

```
# Byte-compiled / optimized / DLL files
__pycache__/
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
pip-wheel-metadata/
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
.hypothesis/
.pytest_cache/

# Translations
*.mo
*.pot

# Django stuff:
*.log
local_settings.py
db.sqlite3
db.sqlite3-journal

# Flask stuff:
instance/
.webassets-cache

# Scrapy stuff:
.scrapy

# Sphinx documentation
docs/_build/

# PyBuilder
target/

# Jupyter Notebook
.ipynb_checkpoints

# IPython
profile_default/
ipython_config.py

# pyenv
.python-version

# pipenv
#   According to pypa/pipenv#598, it is recommended to include Pipfile.lock in version control.
#   However, in case of collaboration, if having platform-specific dependencies or dependencies
#   having no cross-platform support, pipenv may install dependencies that don't work, or not
#   install all needed dependencies.
#Pipfile.lock

# celery beat schedule file
celerybeat-schedule

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


```
* To save: Ctrl+O > Enter > Ctrl+X
### With the .gitignore ready, let's make the first commit
* Set your account
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
* Now make the commit
```
git add .
```
```
git commit -am 'Initial'
```
* Send files to maste
```
git push origin master
```
## Now go in your computer
* Make a new file
* Mouse right click
* Open in Terminal
```
git init
```
* Edit before paste
```
git remote add origin serv_user@site_url:/home/youruser/repository
```
* If your site just have the ip try this: https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/adding-a-```
new-ssh-key-to-your-github-account
```


### If you still having problems :desktop_computer:
* Download Git bash (https://git-scm.com/downloads)
* Try this commands again:
```
git init
```
```
git remote add origin serv_user@site_url:/home/youruser/repository
```
* You will probably get a message that the roots have already been defined, now try that
```
eval $(ssh-agent)
```
* Change ssh_key to your file name
```
ssh-add ~/.ssh/ssh_key
```


### If you are ussing PuTTY :desktop_computer:
* Open PuTTYgen > File > Load private key
* Convesions > ExportOpenSSh key
* Save this key in ~/.ssh/
* Now try again whith the files you created
```
eval $(ssh-agent)
```
```
ssh-add ~/.ssh/ssh_key_you_created
```

### Git bash
```
git pull origin master
```
## Now you have all the files of your server
