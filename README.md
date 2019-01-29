# Django Crud with Docker
Expense control crud application made it Django, Virtualenv and Docker

### Running the application:
To run this application without having to install all dependencies, use Docker and Docker Compose. Follow the instructions below:
- If you don't have [Docker](https://docs.docker.com/install/) and [Docker Compose](https://docs.docker.com/compose/install/), install them by clicking on their respective link.
- Next, clone or download this project. If you choose to clone, type:
``` bash
$ git clone https://github.com/isacmoura/django-crud-with-docker.git
```
- Enter on the project folder:
```bash
$ cd django-crud-with-docker
```
- Then, run the **docker-compose** command:
```bash
$ docker-compose up -d
```
You might have to use `sudo` and the command above.

This command will build the containers. Then will install pip (if you don't have) and using pip we'll isntall Virtualenv and Django. Finally, our server will start to work and run on the `0.0.0.0:8000` ip adress.

### Post-instalation running
You can use your application as well at the `0.0.0.0:8000` adress, but, if you want, you could make some changes.
To do this, follow the instructions:
- Create the module:
`docker exec -it {CONTAINER_ID} python3 manage.py startapp app`. **change "app" to a name fo your preference and CONTAINER_ID for the container_id in `docker ps`**
- Run migrations:
`docker exec -it {CONTAINER_ID} python3 python3 manage.py migrate`
- Create a superuser for Django Admin area:
`docker exec -it {CONTAINER_ID} python3 manage.py createsuperuser`

#### Contributions
Feel free to contribute with this project, send a Pull Request or open a issue.
