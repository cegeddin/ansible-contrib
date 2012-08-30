This repo contains a santitized version of the playbooks I am using for
general systems configuration. In addition to some general config
management plays/tasks, there are also some plays specifically 
targetted toward bootstrapping and maintaining sit down computer
lab machines.

By and large, I have excluded my managed files, with the exception
of the gdm configuration script to go along with the appropriate
set of tasks found in 'update_gdm_configuration.yml'

The idea is to call ansible-playbook on:
    - 'tester.yml' when testing new playbooks and tasks
    - 'site.yml' around every hour
    - 'site-daily.yml' once a day. (And also includes 'site.yml'

As the number of tasks grows, frugal and targeted use of 'site.yml'
will be necessary to not have ansible runs overun each other.  

Let me know if you have suggestions or questions.

