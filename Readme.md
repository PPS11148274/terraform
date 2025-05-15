# TERRAFORM
## Provisionar una máquina virtual Ubuntu 24.04 en Virtualbox mediante Terraform
En esta práctica se realizan los pasos necesarios para instalar una VM de VirtualBox de forma automatizada. \
En primer lugar se descarga la versión para Windows, en mi caso amd64 (https://developer.hashicorp.com/terraform/install#windows). \
Se instala sobre Windows para poder ejecutar VirtualBox. \
Se debe crear un directorio para poner el ejecutable de terraform y después añadirlo al path del sistema.
Para montar la VM, se utiliza el archivo main.tf que se encuentra en el repositorio. \
Una vez hecho esto, se lanza terraform con:
```
terraform init
```
Se puede ver en la imagen siguiente.

![inicio_terraform](https://github.com/PPS11148274/terraform/blob/main/asset/inicio_terraform.png)

