# ansible

Ansible is a configuration tool which works on both pull and push mechanism


### INVENTORY FILE

Inventory is nothing but the list of machine ip or dns names that you want ansible to be managed.

Ansible by default installs 2.9 as by default on AMI's we will get python2.
Always go with latest version, which can be installed from tools/ansible/install.sh

"all" is a group which included all the entries in INVENTORY file.

#### ANSIBLE IS ALL ABOUT MODULES ( collections )

ANSIBLE has lot of pre-defined variables and we need to use them to supply userName and password it has to use to authenticate to the nodes.

ans
### ansible_user     : Predefined variable for userName 
### ansible_password : Predefined variable for password  
Variables should be passed to ansible by using the flag -e

    Ex: ansible -i INVENTORY all  -e ansible_user=userName -e ansible_password=password 
    $ ansible -i inv all  -e ansible_user=centos -e ansible_password=xyz123 -m shell -a uptime


##### Automated Approach : This uses Playbook
Playbooks are written using a language called YAML.

YAML is just  markup languaga ; Markup language is nothing a presentation language

YAML is indendation specific.

indendation specific is nothing but "spacing".


### YAML IS ALL ABOUT:
DIctionary: A Key with a value/key value pair
List: A Key with multiple values
Map: A key with multiple key value pairs

#### What is a playbook ?
* Playbook : A Playbook is a list of plays ( and that's why it always starts with - )
* Play     : A Play is a list of tasks.
* Task     : A Task is nothing but an action that we wish to perfom.

### variables: 

if would like to just print a variable, then it has to be enclosed in double quotes {{variable}}, there is no concept of single quotes.
and if the variable is present in between the string of words there is no need of giving double quotes.


