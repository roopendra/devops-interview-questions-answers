# devops-interview-questions-answers
   Reference: https://techieroop.com/top-10-devops-interview-questions/
- What is the need for DevOps?
- What is meant by Continuous Integration?
- What is the difference between Continuous Delivery vs Continuous Deployment?
- How is devOps different from Agile/SDLC?  
## Git:
- What is the need of Git? What is the difference between Git vs Github?
- How to create a new branch in Git? 
- What is the branching and merging Strategy you are following in your company?
- How will you resolve the conflict in Git?
- Difference between git pull vs git fetch?
- How to revert un-pushed changes in Git?
- How to update the last commit message in git?
- How to update the second last commit message in git? ( Hint: using git rebase)
- How will you merge changes from one branch to another branch?
- How to merge multiple sequence commits into a single commit in git? ( Hint : git squash)
## Maven
- What is Maven?
- What aspects are managed by Maven?
  ( Hint: Builds, Documentation, Reporting,SCMs,Releases,Distribution)

- What is the command to install the JAR file in a local repository?
  ( Hint: mvn install )

- What is difference b/w mvn install vs mvn package
- What is the purpose of the mvn clean command?
- What is POM?
- What are the build phases in Maven?
- What is a Maven artifact?
- Name the three build lifecycle of Maven.
- What is a Maven Repository and types of Maven repository?
## Jenkins 
- What is Jenkins ? How will you use Jenkins to automate CI/CD ?
- How to configure your Github or Bitbucket repository to trigger the build when any changes happen in code ? Please explain all types of Build Trigger In Jenkins?
- Explain End to End java application Pipeline?
- How will you configure Junit to run the test with Jenkins Pipeline ?
- How to integrate the Selenium test with Jenkins Pipeline ?
- What are the differences between Jenkins and TeamCity ?
- How to configure slave nodes in Jenkins ?
- What is the difference between declarative and scripted pipeline ?
- Where to store the global credentials in jenkins??
- How does your UAT build trigger when your Dev build completes? How did you configure the dependency ? 
## Docker
- How to stop all docker containers?
```
docker kill $(docker ps -q)
```
- How to stop docker containers and remove them?
```
docker rm $(docker ps -a -q)
```
- How to remove all Docker Images?
```
docker rmi $(docker images -q)
```
- List & Remove all exited containers   
```
docker ps -a -f status=exited
docker rm $(docker ps -a -f status=exited -q)
```

- List & Remove containers using more than one filter
```
docker ps -a -f status=exited -f status=created
docker rm $(docker ps -a -f status=exited -f status=created -q)
```  

- List & Remove containers according to a pattern
```
docker ps -a | grep "pattern"
docker ps -a | grep “pattern” | awk '{print $1}' | xargs docker rm
```  

- Remove one or more specific volumes
```
docker volume ls
docker volume rm volume_name
```

- Remove dangling volumes
```
docker volume ls -f dangling=true
docker volume prune
```

- Remove a container and its volume
```
docker rm -v container_name
```
- How to create a multistage Dockerfile? 
- What is benefit of Multi-Layer Docker file ?
- What are the benefits of a Container platform over a Virtual machine?  
- Can we run multiple containers within a single pod? What are the use cases when we should use it?  

## Ansible
- What is Roles in Ansible?
- What are the uses of ansible templates? 
- Write an ansible playbook to deploy the Apache in DEV, UAT and PROD environment? 
- Write down Ansible playbook to install Ngnix server?
- What are the advantages of Ansible over other configuration management tools? 
- How can you run ansible tasks from root user? 
- What is a handler and how can we use it in Ansible ? 
- Can we create generic playbook to install software/package in Debian and CentOS?https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_conditionals.html
- How do you access Shell Environment Variables?
- How to keep sensitive configuration in Ansible? ( Hint : Check ansible vault)

## Kubernetes 
- What types of Services are present in Kubernetes ? 
- What are the roles of master and data nodes in Kubernetes ? 
- What are the advantages to having a namespace in any cloud platform? 
- If any application requires web application code, database then how will they communicate to each other? 
- When any pods die and it creates a new pod automatically then what all events happened in the backend to bring the pod back?
- How to configure auto-scaling in Kubernetes?
   https://kubernetes.io/blog/2016/07/autoscaling-in-kubernetes/
- How do pods communicate internally in Kubernetes? 
- How to expose your web-application to the external world? 
- Difference between Ingress and Ingress controller?
- Can you explain the differences between Docker Swarm and Kubernetes?

## Basic Linux and Bash Scripting
- How to check processes which are taking more memory and CPU? 
- How to check which files/directory are taking more space?
- Please tell us how you will check if a file exists on the filesystem?
