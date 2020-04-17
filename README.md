Proyecto para la asignatura del Máster "Planificación y Gestión de Infraestructuras TIC" 
Utilización de Vagrant y Ansible para creación, aprovisionamiento y configuración de máquinas virtuales en un suministrador importante de servicios en la nube.

## Instalación
Instalación aplicada a máquina **Ubuntu 19**
Pasos previos a la ejecución del "Vagrant up"
``` 
$ sudo apt update
```

### Instalación Ansible:
[Guía oficial de instalación Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#)
```
$ sudo apt install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt install -y ansible
$ ansible --version
```

### Instalación Vagrant:
[Guía oficial de instalación Vagrant](https://www.vagrantup.com/docs/installation)
```
$ wget https://releases.hashicorp.com/vagrant/2.2.7/vagrant_2.2.7_x86_64.deb
$ sudo dpkg -i vagrant_2.2.7_x86_64.deb
$ vagrant --version
```
Creamos la imagen dummy:
```
vagrant box add aws-dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box
```

## Ejecución:
Nos dirigimos al directorio /src que es donde encontramos tanto el playbook de Ansible como de Vagrant y ejecutamos:
```
$ vagrant up --provider=aws
```

## Licencia:
Proyecto bajo licencia [LICENSE.md](LICENSE.md)

---
_Proyecto realizado por:_
* **Miguel de la Cal Bravo** - [Miguel de la Cal Bravo](https://github.com/miguelcal97)
* **Félix Ángel Martínez Muela** - [Félix Ángel Martínez](https://github.com/FelixAngelMartinez)
