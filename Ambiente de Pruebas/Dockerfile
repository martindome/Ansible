# Dockerfile para el contenedor de Ansible
FROM ubuntu:latest

# Instala Ansible y las dependencias necesarias
RUN apt-get update && \
    apt-get install -y ansible openssh-client sshpass net-tools && \
    apt-get clean

# Genera una clave SSH para conectarse al otro contenedor
RUN ssh-keygen -q -t rsa -N '' -f /root/.ssh/id_rsa

# Permite el acceso SSH sin contraseña
RUN echo "StrictHostKeyChecking no" >> /etc/ssh/ssh_config
