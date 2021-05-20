PlayBook
=========

This playbook was written to satisfy the requirements of the wheel technical interview.

Requirements
------------

Since we will be using ansible to solve this problem, we should first configure our environment to run ansible.

To install Ansible:
`pip install ansible`

We will need some additional libraries as well to power the modules we use for talking to AWS.

Install the following:
`pip install boto3`

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).


ReadMe.md

### Ansible Role For Wheel Homework ###

To Run:
Install Ansible
`pip install ansible`



How I started:
`mkdir -p wheel-homework`
`git init`
`git remote add origin git@github.com:matthewcmorgan\wheel-homework`
`ansible-galaxy init nginx` 
# This command creates the basic structure for a sharable ansible role
# We we first create modules for each of the pieces of infrastructure we desire to create
# then we will write a playbook to tie the modules together.
The power of ansible comes in creating repeatable patterns
To that end, I have designed this playbook to work with a pattern like
{service}-{env}-{domain}, though it is easy to adjust to any pattern.

I will assume that we pass in a VPC to work in

remeber to set external ip: 
# export EXTERNAL_IP=`curl ipv4.icanhazip.com`
