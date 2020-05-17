# UML Diagrams in Django Apps

I found out how to generate UML diagrams straight from Django's models.py files.
This is an obvious benefit because I can make all my changes directly on the models and the UML is automatically updated.

This uses pygraphviz to accomplish this.

```
brew install graphviz
pip install pygraphviz
# add 'django_extensions' to INSTALLED_APPS in settings.py
python manage.py graph_models <app_name> -o my-uml.png
```
