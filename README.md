# Lab Report: Continuous Integration/Delivery With Jenkins
## Problemen
With installing all the required software. I found out that the Fedora repositories don't include the latest version of vagrant. This was something I had to noticed since when I did vagrant up, I got an error that basically said that the vagrant file wasn't compatible with the older version of the software. I fixed this by adding the hashicorp repository to my repository list and installing it directly from the developers.
## 1.1 Set up the lab environment
I did this by creating a new folder and copying the files found in the origininal repository.

After I initialized the folders as a git repository with

```
	git init
	git add .
	git commit -m Initial
	git brach -M main
	git remote add origin git@github.com:UbeUyttendaele/cicd-sample-app.git
	git push -u origin main
```
## 1.2 Build and verify the sample application
First I startup the the VM using **vagrant up**.
Then I used **vagrant ssh** to establish an ssh connection and went to the /vagrant/cicd-sample-app directory. I added execute permission using **chmod +x sample-app.sh** and executed the script using **./sample-app.sh**. After running the script I could access the webpage that was running in the docker container on my host device (http://192.168.56.20:5050/).

After testing, I stopped the testing docker using **docker container stop samplerunning** and removed it using **docker comtaimer prune** which removes all stopped docker containers.

![testpage](./reportScreenshots/testpage.png)

## 1.3 Download and run the Jekins Docker image
First I installed the docker container using the code provided to us.

```
Login username:
Admin
Provied password:
7266b9df94a941cba102821b57b02917
```

## 1.4 Configure Jekins
In this step I followed the instructions provided to initialize the jenkins evironment.
## Resources

List all sources of useful information that you encountered while completing this assignment: books, manuals, HOWTO's, blog posts, etc.
