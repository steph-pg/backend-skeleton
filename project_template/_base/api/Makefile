PROJECTNAME=$(notdir $(shell dirname $(shell pwd)))

check:
	pytest -s -l --verbose --strict --pylama ${PROJECTNAME};\
	black ${PROJECTNAME};\
	isort ${PROJECTNAME};

run: migrate
	python manage.py runserver_plus

test: migrate
	pytest -s -l --verbose --strict --pylama ${PROJECTNAME}

migrate: mkmigrate
	python manage.py migrate

mkmigrate:
	python manage.py makemigrations

rcomp: requirements/common.txt requirements/dev.txt

requirements/common.txt: requirements/common.in
	pip-compile requirements/common.in

requirements/dev.txt: requirements/dev.in
	pip-compile requirements/dev.in

rsync: req-compile
	pip-sync requirements/*.txt
