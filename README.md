# Jenkins project
Set up three environments 

1.Production

2.Testing

3.Quality Assurance

The developer will deploy the code first on github and as soon as the changes are made it will be deployed on the testing environment after this this code will be checked by the Quality assurance team anf if this code is without errors then it will be automatically deployed in the production environment.

# Process
1. Make a local git repository and the desired index file in it.

2. Create a repository in gitHub and run the following commands in git bash.

    git commit -m "message"

    git remote add origin https://github.com/Sumeet36/devopsal.git

    git push -u origin master

3. Now create a new branch using the command - git branch dev(branch_name) and switch to it using command - git checkout dev

4. Now add code files you want to add and run the following commands

    -git add .
  
    -git commit -m message
    
    -git push --all
    
5. Now if you want that the the push is automatically done as soon as any changes are committed , then go to the .git/hooks/ folder inside your local git repository and make a file post-commit there (this file should not have any entension). 

  post-commit :-

    #!/bin/bash

    echo "pushing"

    git push --all

6. Start jenkins and create new job named job1 for the testing environment and follow the configrations shown in the figure.

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image1.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image2.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image3.png)

7. After this make another job for the Quality Assurance and follow along.

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image4.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image5.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image6.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image7.png)

8.  And lastly create a third job that will be deployed only if the second job builds successfully.

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image8.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image9.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image10.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image11.png)

![](https://github.com/Sumeet36/jenkins_proj/blob/master/images/image_docker_ps.png)
