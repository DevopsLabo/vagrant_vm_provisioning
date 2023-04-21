## Qué hace este proyecto?
El propósito de este proyecto es probar las funciones básicas de aprovisionamiento de VMs (sobre un entorno de Virtualbox), utilizando las características de IaC ofrecidas por [Vagrant](https://developer.hashicorp.com/vagrant/docs).

## Qué se incluye?
Se incluyen archivos:
- **Vagrantfile**: Archivo descriptivo de infraestructura con la definición de 3 VMs (512MB RAM, 1 CPU) sobre una misma red 
- **hosts**: Archivo con definición de hosts y direcciones IP para funciones de networking

## Prerequisitos
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) instalado en forma local
- [Vagrant](https://developer.hashicorp.com/vagrant/downloads) instalado en el mismo equipo (actualmente v2.3.4)
- [Virtualbox](https://www.virtualbox.org/wiki/Downloads) instalado con la versión adecuada (a la fecha, Vagrant es compatible con [Virtualbox hasta la versión 6.1](https://developer.hashicorp.com/vagrant/docs/providers/virtualbox)) y configurado con un adaptador de red con dirección 192.168.56.1/24 (las VMs funcionarán sobre esta red)


## Paso a paso
1. Clonar el repositorio en un directorio local
```
git clone https://github.com/DevopsLabo/vagrant_vm_provisioning.git
```

2. Ejecutar el aprovisionamiento, desde el directorio del proyecto
```
cd ./vagrant_vm_provisioning
```
```
vagrant up
```

4. Controlar las VMs creadas verficando mediante comandos `ping` o `ssh` (por ejemplo a vm1)
```
ping 192.168.56.10
```
```
vagrant ssh vm1
```

5. Jugar con las VMs mediante los comandos disponibles en Vagrant
- [Guía útil de comandos de Vagrant](https://gist.github.com/wpscholar/a49594e2e2b918f4d0c4)
