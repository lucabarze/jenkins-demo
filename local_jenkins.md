```
docker build -f Dockerfile-local_jenkins -t local_jenkins .

mkdir ~/jenkins_home

docker run --name jenkins -i -d -p 8787:8080 -p 50000:50000 -v /Users/luca/jenkins_home:/var/jenkins_home:rw local_jenkins
```

