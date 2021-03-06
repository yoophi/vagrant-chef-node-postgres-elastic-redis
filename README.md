## A Node.js and Rails dev Virtual Machine provisioned by Chef

This is a personal experiment to simplify spinning up a dev box for Node.js 
projects. I intend to expand the provisioning to deploy Yeoman to aid
in scaffolding new web applications.

Please, please, please feel free to contribute.


The VM image created currently has the following properties:
 - Ubuntu 12.10 64 bit
 - nginx
 - Node.js
 - Postgres
 - Java 7 (openjdk)
 - ElasticSearch
 - ElasticSearch Head 
 - Ruby 2.0.0
 - Rails 4.0

### Requirements
  - VirtualBox (https://www.virtualbox.org)
  - Vagrant (http://docs.vagrantup.com/v2/installation/index.html)
  - Git 

### Usage

	git clone https://github.com/GordyD/vagrant-chef-node-postgres-elastic-redis.git
	cd vagrant-chef-node-postgres-elastic-redis
	vagrant up
	vagrant reload
	vagrant ssh

#### Optional 

You can install Librarian Chef to install new cookbooks provided you have Ruby installed. Use the following command:

 	gem install librarian-chef --no-ri --no-rdoc

 You can then add cookbooks to your Cheffile and run 

 	librarian-chef install

 This will store the cookbooks added into your
 cookbooks folder. You can then use these cookbooks for provisioning your VM by specifying requirements in your Vagrantfile.
 A very useful point of reference for this is on the [Opsdoce community site](http://community.opscode.com/cookbooks)

  

