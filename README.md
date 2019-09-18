# recipe-app-api
Recipe app api source code

After adding Dockerfile and requirements.txt run -
    docker build .

Create docker-compose.yml and run following to build image using docker-compose configuration -
    docker-compose build
    
Create django project -
    docker-compose run app sh -c "django-admin.py startproject app ."
