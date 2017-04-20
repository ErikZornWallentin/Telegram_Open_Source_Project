# Telegram Open Source Project
****************************************************
Erik Zorn-Wallentin  0864583
CIS*3760             Telegram - Sprint 4
Thursday, Mar. 31 / 2016
****************************************************

****************************************************
			GENERAL INFO FOR READER                     -- IMPORTANT TO READ THIS PART
****************************************************

** I did not upload the source code as it is an open source project from Telegram.

I worked on an open source project called Telegram, it is a web based mobile application.
I worked in a scrum with other teammates where we had a Scrum Master and a Project Leader.
In this scrum we used Redmine as our project management tool.
	Redmine Info: http://www.redmine.org/
We also followed a sprint, and I gave the code from the end of our Sprint 4 (biweekly sprint).
I am only giving the full details to this specific Sprint (Sprint 4), other Sprint details are in another directory.
In this sprint I continued to work with my team, but the specific things I worked on were:
	Created star icon to be displayed in Telegram
	Implemented Favourites Button (UI) and code to support it
	Implemented Testing Framework using JASMINE
	
	Jasmine is a Behavior-driven development framework for testing JavaScript code. It does not depend on any other JavaScript framework.
	Jasmine link: http://jasmine.github.io/
	
All of Sprint 4 was not pushed to the real Telegram directory, this was a personal project for the team.
You can see the full implementation and source code here in this directory to see what I did by following the screenshots.
	
See screenshots in directory for more info on the sprint and proof!


*********************** IMPORTANT video to see ***********************


	Our group made a video on the Telegram project, you can see link here:
		https://www.youtube.com/watch?v=6QK-SzS70as
	I am in the video, you can see me at 1:56min in, I am the curly haired guy in the back!
	It is hosted on the SOCS Guelph youtube channel (University of Guelph)
	
	
*********************** IMPORTANT video to see ***********************


**********************
GIT INFO FOR TELEGRAM
**********************

****************************************************
Pushing to Git branch -- adding files to repository
****************************************************
	
	Add Files:
	
		git add <file(s) changed>
		
		Example:
		
			git add test/spec/FilterSpec.js
		
	Commit Files:
	
		git commit -m "<message detailing changes>"
		
		Example:
		
			git commit -m "Added the testing framework"
		
	Push Files:
	
		git push origin <branch-name>
		
		Example:
		
			git push origin ISSUE1012
	
****************************************************
Pulling / updating your local repository from branch
****************************************************
	
	Cloning

	If you're starting a new working copy of the project, you'll need to clone the repo to your computer. Your HEAD pointer will be set up to our develop branch.

		Git clone into main branch:
		
			git clone https://<username>@cis3760.socs.uoguelph.ca/telegram.git
			
			Example:
			
				git clone https://ezornwal@cis3760.socs.uoguelph.ca/telegram.git
		
		Git clone into specific branch:
		
			git clone -b <branchname> https://<username>@cis3760.socs.uoguelph.ca/telegram.git
			
			Example:
			
				git clone -b ISSUE1012 https://ezornwal@cis3760.socs.uoguelph.ca/telegram.git
		

************************
Updating your local copy
************************

	If there have been changes made to a branch and you wish to merge them into your local copy, you can perform a pull.

		git pull origin <from-branch>

	Git will attempt to merge the changes into your copy automatically, but may need your interaction. If this gets too complicated, you may want to cancel the pull:

		git reset --hard
		
***************
Troubleshooting
***************

	If you were not aware already, we've changed the default branch to origin/develop. Check to see that you're set up for this change:

	Run:

		git branch -r

	Is your origin/HEAD pointing at origin/master? If so, your git is out-of-date. Do the following (may be out of order...):

		git remote prune origin
		git remote set-head origin -a
		git pull origin develop

	Then you should be able to checkout as usual.

	Reverting to an older snapshot

	If you want to work based on an older snapshot of the project get the hex ID of the snapshot you want and reset your local copy:

		git reflog
		git reset --hard <hex-value>

	Notice that HEAD@{2} means "where HEAD used to be two moves ago", so the top of the list is the most recent.

*****************************
Building Webogram from Source
*****************************

    More info: https://github.com/zhukov/webogram#technical-details

You may need to install node.js:

    Ubuntu / Debian

		curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
		sudo apt-get install -y nodejs

    Fedora-based

		curl --sL https://rpm.nodesource.com/setup_4.x | bash -
		yum -y install nodejs

    OSX (https://nodejs.org/en)

	And then, once you're in your repo,
	
		*** IMPORTANT STEPS ***
			sudo npm install
			sudo npm install gulp
			gulp watch
		*** IMPORTANT STEPS ***

	Open a browser and type in this to start up Telegram:
		http://localhost:8000/app/index.html 
		
		Now you can test out your source code!
		You will notice this uses the Desktop version, you can make screen smaller if you want to try out the Mobile version.
		You will need a phone to be able to login to Telegram as it will send you a text to confirm your login info.
	

************************************	
Troubleshooting - After installation
************************************
	Cannot find module 'event-stream'? These steps may help you. Close the Telegram process.

		sudo npm cache clean
		sudo npm install

	Then close the terminal and run the process again.
	
*******************
Committing changes
*******************
    NOTE: Need updated information here once we begin branches.

	Save your work locally and commit your changes

		git commit -m "<insert message>" 

	When you're ready to push the changes to everyone else in your branch:

		git push origin

	Alternatively, if you want to push to a specific branch to the Redmine repository:

		git push origin <branch>

**************
Git Branching
**************

	Create the branch on your local machine and switch to this branch :

		git checkout -b <new-branch-name> <from-branch-name>

	Push the branch on github :

		git push origin name_of_your_new_branch

	You can see all the branches created by using :

		git branch -r

	To delete a branch locally:

		git branch -D <branch-name>

	To delete a branch globally (do not do this unless you've talked to the rest of the team!):

		git push --delete origin <branch-name>
		git remote prune origin

********************************
USEFUL GREP COMMAND FOR PROJECT
********************************
			grep -r "text here" .
			
			Example:
				grep -r "emoji-spriesheet" .
				
			This command is useful because we worked on Telegram source code without the main developers help,
			and we needed to find where everything we located to fix bugs or add features.
			Using "Inspect Code" to see the html/css code and using this grep command to find the files was useful.
			Use this grep command where you want to find the files using the line of text in the file.
		
*****************		
Tools we can use
*****************

	https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches
	http://jasmine.github.io/

	

*************************************
Running the program(s) - COMPILATION
*************************************

	Make sure you have node.js installed on your computer, npm and gulp (LOOK ABOVE FOR DETAILS).
	change directory (cd) to the telegram main directory and type in:
		
		gulp watch
	
********************************************
TESTING -- JASMINE FRAMEWORK
********************************************

	Testing framework in Jasmine has been automatically setup for you, and can test in a click of a button!
	Go to your Telegram main directory, and right click and open SpecRunner.html in FIREFOX.
		* May not work properly for you in chrome, as it may give a security error *
	Once you open SpecRunner.html, it will show all the test cases on the code!
	There were also test's done on the UI, this was done on Redmine ISSUE in sprint 4.
	
	*Note: You need node.js to be installed for testing framework to work! *
	
	Files to inspect for testing framework to see code:
		SpecRunner.html              --> where you run the testing framework and pops up in a browser
		test/spec/FavoriteSpec.js    --> tests being done in Jasmine on specific JavaScript files
		test/lib/*                   --> Jasmine Library, must have this for Jasmine to work!!
		
**************************
Bibliography / References
**************************

	https://telegram.org/
	https://github.com/zhukov/webogram
	https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches
	http://jasmine.github.io/

*****************
Known Limitations
*****************

	NONE
