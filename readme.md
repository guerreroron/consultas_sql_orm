# COMANDOS CONSULTAS SQL A ORM

# django-admin start project consultas_sql_orm
# cd consultas_sql_orm
# code .
# python manage.py startapp django_wizard_app
# in settings.py add app 'django_wizard_app' & change local-time
# in models.py (app), create a table 'wizard'
# class Wizard(models.Model):
    name = models.CharField(max_length=45)
    house = models.CharField(max_length=45)
    pet = models.CharField(max_length=45)
    year = models.IntegerField()
# python manage.py makemigrations
# python manage.py migrate
# python manage.py shell
# from django_wizard_app.models import Wizard
# Wizard.objects.all()
# Wizard.objects.create(name="Harry Potter", house="Griffindor", pet="Hedwig", year=5)
# Wizard.objects.create(name="Hermione Granger", house="Griffindor", pet="Crookshanks", year=5)
# Wizard.objects.create(name="Luna Lovegood", house="Ravenclaw", pet="None", year="4")
# Wizard.objects.create(name="Padma Patil", house="Ravenclaw", pet="None", year="5")
# Wizard.objects.all()
# select * from django_wizard_app_wizard;
# select * from django_wizard_app_wizard WHERE id = 1;
# Wizard.objects.get(id=1)
# Wizard.objects.first()  
# Wizard.objects.last()  
# Wizard.objects.filter(house="Griffindor")
# Wizard.objects.exclude(house="Griffindor")
# select * from django_wizard_app_wizard ORDER by name;
# Wizard.objects.all().order_by("name")
# Wizard.objects.all().order_by("-name")
# Wizard.objects.get(name="Luna Lovegood")
# Wizard_for_update = Wizard.objects.get(name="Luna Lovegood")
# Wizard_for_update.pet = "Garfield"
# Wizard_for_update.save()
# Wizard.objects.get(name="Luna Lovegood")
# Wizard_for_delete = Wizard.objects.get(id=5)
# Wizard_for_delete = Wizard.objects.filter(house="Ravenclaw") 

