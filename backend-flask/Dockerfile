#a file from dockerhub
FROM python:3.10-slim-buster

#inside the container
WORKDIR /backend-flask

#outside -> inside container (contains library that installs and runs the app)
COPY requirements.txt requirements.txt

#inside container
RUN pip3 install -r requirements.txt

#copying from outside the container to inside the container
#.(first) -> /backend_flask -> outside the container
# second . -> inside the container (copying everything in the current directory)
COPY . .

# set env variables inside the container
# set env variable to configure our application

ENV FLASK_ENV=development

EXPOSE ${PORT}

# To run flask (python3 -m flask run --host=0.0.0.0 --port=4567(To run locally))(m for module)
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]