# resful api with a datebase behind it

1. make sure you have the basics installed
	$ sudo aptitude update install curl sqlite
	$ sudo pip install 
    $ sudo pip install flask
    $ sudo pip install flask_sqlalchemy
    $ sudo pip install flask_marshmallow
    $ sudo pip install flash_restful

2. make sure you run 'run-me-first.py' first

3. then run api-db.py


Testing:
1. add a user: 
	$ export MESSAGE='{"username": "myuser", "password": "12345", "first_name": "first", "last_name": "last", "age": 32}'
    $ curl -X POST -H "Content-Type:application/json" -d "${MESSAGE}"  http://localhost:5000/api/users

2. see what you added: 
    - bring this up in your browser: http://127.0.0.1:5000/api/users
	- or: $ curl http://127.0.0.1:5000/api/users

3. delete a user: 
    $ curl -X DELETE -H "Content-Type:application/json"   http://localhost:5000/api/users?id=1
