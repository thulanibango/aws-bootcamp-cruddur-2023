#Inside container
FROM python:3.10-slim-buster

WORKDIR /backend-flask


#Outside container -> Inside container
#Contains library want to install to run the app
COPY requirements.txt requirements.txt

#Inside Container
#Install python library used for app
RUN pip3 install -r requirements.txt

#Outside container -> inside container
#. Means everything in current directory
#first period : /backend-flask (outside container)
#Second period : /backend-flask (inside container)

COPY . .

# Env for the entire environment
#Inside container and will remain set when container is running
ENV FLASK_ENV=development

EXPOSE ${PORT}

# python3 -m flask run --host=0.0.0.0 --port=45667 // cmd used to start up flask
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]