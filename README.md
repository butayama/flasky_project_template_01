# flasky_project_template_01
# Docker deploy

## Installation von docker
Achtung, Fehler bei Installation von docker über Snap. Siehe meinen Kommentar in stack overflow:
https://stackoverflow.com/questions/51729836/error-response-from-daemon-cannot-stop-container/64120350#64120350
   
# after changes: create a new image
 docker build -t yetigo/flasky_project_template_01:latest .  
 
# test the new image locally   
 docker run --name test -d -p 8000:5000 --rm yetigo/flasky_project_template_01:latest  
 
# upload docker container image  
 docker push yetigo/flasky_project_template_01:latest  

# download docker container image 
 docker pull yetigo/flasky_project_template_01:latest  
 docker run --name test -d -p 8000:5000 --rm yetigo/flasky_project_template_01:latest   
 
## display active containers 
 docker ps  
 docker container ls  
 
 ## stop Container:
docker container stop test   

## remove Container:
docker container rm test  

## display Images:
docker images

## remove Image:
docker image rmi yetigo/flasky_project_template_01:latest
