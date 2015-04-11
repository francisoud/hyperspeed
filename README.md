* Prerequisites

Install Java or Ruby ? (TODO embedded it)
Install VirtualBox (TODO: auto download / install using puppet ?)
  +=> autodownload/install git on VM or prerequisite on local computer ? 

Puppet, Vagrant ?
  
* Installation

	Case 1: If someone already installed it on a project using the wrapper 
	(TODO add link to wrapper doc), 
	you don't have to install anything.
	Just svn checkout or git clone the project and run hg(.bat|.sh) at the project root

	Case 2: You are using it regularly or you're the first one to use it on a project
	Download archive, unzip somewhere
	add "/my/install/folder/bin/" to path
	done!
	For usage see section New Project

* New Project
	$ hs init https://github.com/francisoud/my-project.git --git command line option (user.name & co)
	$ gradle hs:init https://github.com/francisoud/my-project.git --git command line option (user.name & co)
	Create the manifest (with scm: section)

* Checkout / Clone existing project (not already on computer)
	$ hs restore https://github.com/francisoud/my-project.git
	$ gradle hs:restore https://github.com/francisoud/my-project.git
	
* Hibernate project
	Clean existing local project keep only minimal bootstrap file to recreate from scratch when needed
	$ hs hibernate
	$ gradle hs:hibernate

* Rebuild from local bootstrap file after hibernate
	$ hs restore
	$ gradle hs:restore

* Setup Continuous Integration
	$ hs ci
	$ gradle hs:ci

* Setup your favorite IDE
	$ hs ide [eclipse|intellij|...]

* Scaffold project screens for team members based of work separation or backlog attribution
	$ hs team:tasks "/path/to/tasks.csv"

* Publish locally
	$ hs pub:local vagrant up

* Publish to receipt env1 for tester to test
	$ hs pub:env1 


Layout:
	my-project
	  |__manifest
	  |__.hs/
	  |__.git/
	  |__my_files...
