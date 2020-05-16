# Study django
# Download Visual Studio Code https://code.visualstudio.com/download
- 1.1  Python - Microsoft
- 1.2  Django - Djaneiro
- 1.3  Django - Intellisense
- 1.4  Better Jinja 
- 1.5  vscode-icon
- 1.6  Bracket Pair Colorizer 2
- 1.7  vscode-icons
- 1.8  HTML Boilerplate
- 1.9  Gitlens

# Download Python  https://www.python.org/downloads/windows/
* Edit User Variables
- 2.1  C:\Python38
- 2.2  C:\Python38\Scripts
- 2.3  C:\Python38\Lib\site-packages
* Edit System Variables
- 2.4  C:\Python38
- 2.5  C:\Python38\Scripts
- 2.6  C:\Python38\Lib\site-packages

# Pip install
- 3.1 Django -> python -m pip install Django
- 3.2 pylint
- 3.3 pylint-django
- 3.3 bootstrap4
- 3.4 Beautifulsoup4
- 3.5 request
- 3.6 django-crispy-forms
- 3.7 wheel
- 3.8 virtualenv
- 3.9 pillow

# Upgrade pip list
- 4.1 pip install --upgrade pip
- 4.2 pip install --upgrade (package name)

# virtualenv venv
- virtualenv venv
- .\venv\scripts\activate

- pip install django==3.0
- pip install pylint
- pip install wheel
- pip install django-crispy-forms
- pip install bootstrap4
- pip install beautifulsoup4
- pip install request
- pip install pillow

# django-admin startproject djangoproject
# python manage.py startapp school

- python manage.py runserver

# settings.py
<br> INSTALLED_APPS = [
<br>    'school',
<br> TEMPLATES = [
<br>    {
<br>        'BACKEND': 'django.template.backends.django.DjangoTemplates',
<br>        'DIRS': [os.path.join(BASE_DIR, 'school/template')],

# create folder Template under school app
# create folder school under template
# create file home.html
# home.html
<br>{% extends 'school/base.html' %}
<br>{% block content %}
<br>    <div class="container">
<br>       
<br>            Welcome to Admin Chumphon
<br>       
<br>        <p>We are getting Better</p>
<br>    </div>
<br>{% endblock content %}
# views.py
<br>from django.shortcuts import render
<br>
<br>def HomePage(request):
<br>    return render(request, 'school/home.html')
	
# djangoproject urls.py
<br>
<br>from django.contrib import admin
<br>from django.urls import path, include
<br>
<br>urlpatterns = [
<br>    path('admin/', admin.site.urls),
<br>    path('', include('school.urls')),
<br>]

# school urls.py
<br>from django.urls import path
<br>from .views import HomePage
<br>
<br>urlpatterns = [
<br>    path('', HomePage, name='home-page'),
<br>]






































