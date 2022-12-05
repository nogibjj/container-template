
## Template for Containers

### Lesson 2:  Persistent Storage with Containers

* [persisting_data/](https://docs.docker.com/get-started/05_persisting_data/)

Really cool command that randomly creates a number:

`docker run -d ubuntu bash -c "shuf -i 1-10000 -n 1 -o /data.txt && tail -f /dev/null"`

Note, you must run `docker ps` to see the daemons", then you run `exec` to invoke running container

`docker exec e294cdd4a76e cat /data.txt`

See no file!

`docker run -it ubuntu ls /`

Create a volume for sqlite:

`docker volume create todo-db`
`docker build -t getting-started .`

#first test it
`docker run -p 3000:3000 getting-started`

#then run it for real!

`docker run -dp 3000:3000 -v todo-db:/etc/todos getting-started`


