<p align="center">
  <img src="https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/5de65519-5c31-4104-bd77-0df4fc17549a"  width="150" height="150"/>
  <img src="https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/b7bb4bae-056f-43f6-bd96-f131b5cff95f"  width="150" height="150"/>
</p>

`Laravel` Laravel is a popular open-source PHP web application framework used for building web applications and APIs. It follows the Model-View-Controller (MVC) architectural pattern and provides a set of tools and features that make web development more efficient and organized.

`Ansible` Ansible is an open-source automation tool that simplifies the process of configuration management, application deployment, and task automation. It allows you to define and manage your infrastructure as code, making it easier to provision, configure, and maintain servers and other IT resources, I'll try to implement with Ansible.


## Pre-Requisite

| Name | Values |
|---|---|
| Server VPS | 1 vCpu 1 GiB |
| Ansible Engine | https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html |
| SCM | GIT |

## Deficiency

* Each repository is public, does not use Password and Username

## Provide Information

| Name |
|---|
| package php, etc |
| Mariadb |
| Config Your App |
| Apache2 |
| Letsencrypt |

## How To Setup

### 🔧  Git Clone

Clone this Repository on your local Mechine ```git clone https://github.com/fahmifiqih1/Ansible-Deploy-Laravel.git``` | ```cd Ansible-Deploy-Laravel```

### ⚙  Change Setting

1. Prepare ansible.cfg file, host and key like key.pem or id_rsa.
   
```
Adjust the config with the existing one, starting from inventory, private_key_file.
```
![Screen Shot 2023-08-17 at 16 03 15](https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/a00d32a0-d56f-462c-b577-2a3e1fcb8ad2)

```
Enter your target server's hostname and customize your server user, but usually it defaults to ubuntu user.
```
![Screen Shot 2023-08-17 at 16 03 33](https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/8f75744c-f310-42a6-95bb-cfd7587806a9)

2. Then set up additional configurations.

```
Change key Repo, Domain, Version and Email, with what you have.
```
![Screen Shot 2023-08-17 at 16 12 55](https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/3ce6109a-05ab-419e-b3cd-fa57e9e9e740)


3. Before starting don't forget to replace .env with your own.

```
To change the .env.example you can ~/ansible-laravel/roles/site-laravel/templates
```
![Screen Shot 2023-08-17 at 16 20 46](https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/11687dce-c927-4558-8d80-152cd799559e)

4. Provide databases
```
We also provide a database for your configuration in .env, if you want to use it you can find it here, ~/ansible-laravel/roles/mariadb/vars
```
![Screen Shot 2023-08-17 at 16 26 20](https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/55309a9c-5b3f-44e1-adb7-06a533bd7600)
![Screen Shot 2023-08-17 at 16 26 39](https://github.com/fahmifiqih1/Ansible-Webserver/assets/53596721/662595d8-08a7-4b8f-9e5a-4a5429ce81eb)

```
you can hide the credential database if you want, it can use "ansible-vault"
```

5. Done Configure
```
When everything is ready, you can execute commands to auto-configure with Ansible. you can run the
"ansible-playbook main.yaml" command
```
