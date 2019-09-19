# recipe-app-api
Recipe app api source code

After adding Dockerfile and requirements.txt run -
    docker build .

Create docker-compose.yml and run following to build image using docker-compose configuration -
    docker-compose build
    
Create django project -
    docker-compose run app sh -c "django-admin.py startproject app ."

Create .travis.yml file to configure travis-ci and flake8
flake8 is configured in .flake8 file

To run test case -
docker-compose run app sh -c "python manage.py test"
To run test case and lint -
docker-compose run app sh -c "python manage.py test && flake8"

Create new app -
docker-compose run app sh -c "python manage.py startapp core"

Creation migration file
docker-compose run app sh -c "python manage.py makemigrations core"