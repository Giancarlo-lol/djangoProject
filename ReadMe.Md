## Create a Virtual Environment
1. Da CMD creare la cartella del progetto:<br> <code>mkdir project_name</code>
2. Spostarsi all'interno della cartella: <br><code>cd project_name</code>
3. Installare il Virtual Enviroment<br> <code>python -m venv env</code>
4. Attivare il venv:<br> <code>source env/Scripts/activate</code>
5. Controllare che sul proprio progetto sia attivo nella console il tag (env) o (venv)
6. Installare Django:<br> <code>pip install django</code>

## Creating a Django Project
1. Creare un nuovo progetto: <br><code>django-admin startproject project_name</code>
2. Avviamo il progetto <br><code>python manage.py runserver</code>

## Starting the new Project
1. Creo la cartella dell'app <br><code>python manage.py startapp app_name</code>
2. Aggiungo la nuova App in fondo alla sezione <b>INSTALLED_APPS</b> che si trova nel file <b>djangoProject/settings.py</b>

## Changing in our Models
1. Vai su app_name/models.py e crei il nuovo modello
2. ogni volta che si crea un nuovo modello, da CMD si effettua una migrazione: <br><code>python manage.py makemigrations</code>
3. poi si effettua avvia la migrazione con: <br> <code>python manage.py migrate</code>
4. Dopo aver creato il primo modello, registriamo l'amministratore andando su <b>app_name/admin.py</b> e importiamo i modelli che ci interessano scrivendo nel file:<br> <code>from .models import model_name</code> <br>(oppure * per importarli tutti ) 
5. creiamo un superuser tramite questo comeando: <br><code>python manage.py createsuperuser</code>
6. avviamo la nostra applicazione tramite il comando <br><code>python manage.py runserver</code>
7. verifichiamo andando su <b>localhost/admin</b> di riuscire ad accedere con le credenziali Superuser

## Modifica degli URL
1. andiamo su app_name/views.py e qui definiamo le nostre view indicando il file .html a cui fanno riferimento e che abbiamo creato nella sezione templates
2. andiamo su djangoproject/urls.py e qui all'interno di urlpatterns creiamo l'alberatura della nostra app


