Levantar:
    docker-compose up -d

Una vez que los contenedores están en ejecución, puedes acceder al contenedor de Ansible:
    docker exec -it ansible_controller bash

Copia la clave pública SSH al contenedor objetivo para permitir la autenticación:
    sshpass -p "password" ssh-copy-id root@ansible_target

Ejecutar:
ansible-playbook -i /ansible/hosts /ansible/playbook.yml -vvvv
