.PHONY: first_build build clean pytest pydoc jupyter mlflow


first_build:
	git init
	dvc commit
	docker compose build
	git add .
	git commit -m "first commit"
	git branch -M main
	git remote add origin https://github.com/githubjacky/{{cookiecutter.project_name}}.git
	git push -u origin main


build:
	docker compose build


clean:
	docker rmi --force 0jacky/{{cookiecutter.project_name}}:latest


pytest:
	docker compose run --rm pytest


doc:
	docker compose run --rm doc


jupyter:
	docker compose run --rm --service-ports jupyter-lab