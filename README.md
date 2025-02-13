runtime.txt file add python verion -> python-3.12.5

requirements.txt add packages used in this project -> 
asgiref==3.8.1
Django==5.1.6
django-crispy-forms==2.3
gunicorn==23.0.0
packaging==24.2
sqlparse==0.5.3
tzdata==2025.1
whitenoise==6.9.0

procfile -> web: gunicorn todo_site.wsgi:application --bind 0.0.0.0:$PORT

.gitignore file in root directory -> myenv/

settings.py file ->
ALLOWED_HOSTS = [
    "todo-app-production-1ee3.up.railway.app"
    ]

MIDDLEWARE = [
'whitenoise.middleware.WhiteNoiseMiddleware',
]

STATICSTORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'

CSRF_TRUSTED_ORIGINS = [
    "https://todo-app-production-1ee3.up.railway.app"
]

TIME_ZONE = 'Asia/Kolkata'

INSTALLED_APPS = [
    'todo',
    'crispy_forms'
]

upload project on github using git bash -> 

git init
git status
git remote add origin https://github.com/siddharthgaud/ToDo-App.git
git add .
git commit -m "Initial commit"
git branch -M main
git push -u origin main


To update anything in the code and then push to github ->

git add .
git commit -m "updated file commit"
git push -u origin main


To deploy on Railway app  ->

configure todo app from github 
settings -> deploy start command -> gunicorn todo_site.wsgi:application --bind 0.0.0.0:$PORT



    
