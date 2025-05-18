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
## Configurar archivo de inventario
El archivo de inventario contiene información sobre los hosts que administrará con Ansible. Puede incluir de uno a varios cientos \
de servidores en su archivo de inventario y los hosts pueden organizarse en grupos y subgrupos. El archivo de inventario a menudo  
se utiliza también para configurar variables que serán válidas sólo para hosts o grupos específicos, \
a fin de usarse dentro de los playbooks y las plantillas.
Las claves generadas, se añaden también al archivo /etc/ansible/hosts. \
![crea archivo hosts](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/crea_archivo_hosts.png) \
Ahora se hace una prueba de conexión. \
![prueba de conexion](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/crea_archivo_hosts.png) \
El siguiente paso es crear el playbook para automatizar la configuración (apache.yml).
Una vez generado este archivo se lanza para configurar el nodo.
![lanza playbook](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/crea_archivo_hosts.png).
En la siguiente imagen, se puede ver que funciona correctamente.
![apache funcionando](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/apache_funcionando.png) 
# _______________________________________________________________________
Configurar una máquina virtual Ubuntu 24.04 en Virtualbox mediante Ansible.
- Crear un index.html con el contenido: ‘Ansible rocks’ en el directorio del servidor web para
poder ser mostrado y reiniciar el servicio.
- Realizar un curl al servidor web y verificar el mensaje ‘Ansible rocks’.

Para esta tarea solo hay que modificar la parte de página de prueba del playbook apache.yml
Comentar todos los apartado (o eliminarlos) excepto ese, debe quedar así.

![ansible_rocks](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/ansible_rocks.png)

Se comprueba ahora que funciona correctamente haciendo un curl.

![curl comprobacion](https://github.com/PPS11148274/terraform/blob/main/ansible/asset/ansible_rocks.png)


