#### Original repository
    https://github.com/lightweightdjango/examples

#### First time pre-steps
```text
(*) -> run first time only
/etc/hosts -> 127.0.0.1	db
add to pycharm run profile -> runserver 0.0.0.0:8001
bash_profile -> alias d-c="docker-compose" alias d-r="docker-compose run web"
```

#### Setup Environment (*)
```bash
rmvirtualenv lightweight_django_chapter3 
deactivate
mkvirtualenv --python=/Library/Frameworks/Python.framework/Versions/3.6/bin/python3 lightweight_django_chapter3 
sudo easy_install pip
pip install --upgrade pip
pip install -r docker/requirements.txt
```

#### Roll out
```bash
d-c up -d --build
docker ps
curl http://0.0.0.0:8000/
d-c stop web
```


#### Diagnose
```bash
d-r bash
```