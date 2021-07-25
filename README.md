# RESTOnAzure
A web app using FastAPI and deployed to Microsoft Azure

## Current setup machine
MacOS 10.15.6
Python 3.6+

## Setup Python virtual environment
<!-- python3 -m venv [path_to_directory] -->
Inside current directory, run following commands:
```
python3 -m venv env
source env/bin/activate
```

## Setup commands
```
pip install fastapi
pip install uvicorn
brew install tesseract # install Tesseract OCR engine
pip install pytesseract # install pytesseract wrapper
```

### Commennts
Using requirements.txt for installing python packages is also a good choice.
#### Puts local packages into virtualenv
```
pip freeze --local > requirements.txt
pip install -r requirements.txt 
```


## Start server
```
uvicorn main:app --reload
```

## Relevant RESTful services
GET, POST, PUT, DELETE


### Troubleshooting
Q: MacOS issue - "Could not fetch URL https://pypi.python.org/simple/uvicorn/: There was a problem confirming the ssl certificate: [SSL: TLSV1_ALERT_PROTOCOL_VERSION] tlsv1 alert protocol version (_ssl.c:645) - skipping"
A: Use command - curl ```https://bootstrap.pypa.io/pip/3.5/get-pip.py | python ```

## Upgrade Python version on MacOS
brew install python3 && cp /usr/local/bin/python3 /usr/local/bin/python
## Upgrade Python version after activating virtual environment
```
Step 1: Freeze requirement & take a back-up of existing env

pip freeze > requirements.txt
deactivate
mv env env_old

Step 2: Install Python 3.7 & activate virutal environment
sudo apt-get install python3.7-venv
python3.7 -m venv env
source env/bin/activate
python --version

Step 3: Install requirements
sudo apt-get install python3.7-dev
pip3 install -r requirements.txt
```


## Credit
https://stackoverflow.com/questions/10218946/upgrade-python-in-a-virtualenv
https://stackoverflow.com/questions/64561770/cant-run-uvicorn-version
