Steps:
1. Install nodejs ==> install npm
2.Use n module from npm in order to upgrade node
        sudo npm cache clean -f
        sudo npm install -g n
        sudo n stable
3. Install angular and create app
        npm install -g @angular/cli
        ng new my-dream-app
        cd my-dream-app
        ng serve -o
        npm outdated  // for outdated packages 

4. create dockerfile shown in the angularapp
    chmod a+rwx angularapp/
5. install docker
6. crete docker image: 
    docker build --rm -f angularapp/Dockerfile -t angularapp:v1 angularapp
7. Run docker image
    docker run --rm -d -p 80:80 angularapp:v1
8. stop docker container
      docker ps
      docker stop 58ba2953c0e5
      
9. push it to dockerhub
    dockerid: lakhandutt
    #tag the image
    docker tag angularapp:v1 lakhandutt/angularapp:v1 
    docker login
    #push the image
    docker push lakhandutt/angularapp:v1
    docker image ls

10 configure git :
   git init
   git add .
    git config --global user.email "you@example.com"
     git config --global user.name "Your Name"
     git remote add origin git@github.com:username/new_repo
    git push -u origin master
    