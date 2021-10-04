# docker-simple

## creation du conteneur:
docker run -it ubuntu

## initialisation des information 
apt-get update
apt-get -y install python3 python3-pip nano 
pip3 install flask

## creation de l'application dans /otc/app.py

import os
from flask import Flask
app = Flask(__name__)
@app.route("/")
def main():
    return "Welcome!"
@app.route('/how are you')
def hello():
    return 'I am good, how about you?'
if __name__ == "__main__":
    app.run()
    
## lancement de l'application
FLASK_APP=/opt/app.py flask run --host=0.0.0.0

