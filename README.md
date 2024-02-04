# Python Package Cookie Cutter
1. modify the settings in cookiecutter.json
2. create project from the template
```sh
cookiecutter python-project-template
```
3. create a github named with `cookiecutter.project_name`
4. create a .env file
5. set three variables in the .env file
    - UID: Linux user id in a docker container
    - GID: Linux group id in a docker container
    - DOCKER_USER: Linux user name in a docker container
    - PROJ: the name of you project, the working directory in a docker container
6. build the docker image and first push to the github repo
```sh
make first_build
```
7. connect a dagshub repo with a github repo, setup credentials and then publish
```
dvc push
```
