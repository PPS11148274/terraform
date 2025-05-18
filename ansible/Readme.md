# ANSIBLE
Configurar una máquina virtual Ubuntu 24.04 en Virtualbox mediante Ansible.
- Realizar update & upgrade del sistema de forma automática.
- Instalar el servicio apache.
El servicio se instala sobre un Ubuntu desktop 24.04 como manager y se va a controlar otra VM también \
con Ubuntu 24.04.
## Generación de Keys y copia al nodo controlado
![crea keys](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/crea_keys.png)
Ahora se copia la clave pública al nodo.
```
ssh-copy-id -i ~/ansible.pub usuario@IP de nodo_controlado
```
## Instalación de Ansible
Se utiliza el método habitual de instalación y nada más, es simple.
```
sudo apt update
sudo apt install ansible -y
```


