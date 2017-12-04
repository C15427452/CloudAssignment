# Cloud Computing Assignment 2

- Yasmina Nunez
- C15427452
- DT228/3


Github Link: https://github.com/C15427452/CloudAssignment

Youtube Link: https://youtu.be/6AH3zO66AKE


- Clone Repo
- cd into mainapp directory
- run the python script (python3 mainapp.py)
- then go to http://35.205.113.16:8080


DockerCMS :

* Running initial page : curl http://35.205.113.16:8080


* List containers : curl http://35.205.113.16:8080/containers
* Inspect specific container : curl http://35.205.113.16:8080/containers/<ID>
* List running containers : curl http://35.205.113.16:8080/containers?state=running
* Dump specific containers logs : curl http://35.205.113.16:8080/containers/ID/logs
* Create container : curl -X POST -H 'Content-Type: application/json' http://35.205.113.16:8080/containers -d '{"image": "ID"}'
* Update container : curl -X PATCH -H 'Content-Type: application/json' http://35.205.113.16:8080/containers/ID -d '{"state": "stopped"}'
* Delete container : curl -s -X DELETE -H ‘Content-Type: application/json’ http://35.205.113.16:8080/containers/ID
* Delete all containers : curl -s -X DELETE -H ‘Content-Type: application/json’ http://35.205.113.16:8080/containers
  
  
* List images : curl http://35.205.113.16:8080/images
* Create image : curl -H 'Accept: application/json' -F file=@Dockerfile http://35.205.113.16:8080/images
* Update image : curl -s -X PATCH -H 'Content-Type: application/json' http://35.205.113.16:8080/images/ID -d '{"tag": "L"}'
* Delete image : curl -s -X DELETE -H ‘Content-Type: application/json’ http://35.205.113.16:8080/images/ID
* Delete all images : curl -s -X DELETE -H ‘Content-Type: application/json’ http://35.205.113.16:8080/images


* List nodes : curl http://35.205.113.16:8080/nodes
* List services : curl http://35.205.113.16:8080/services
