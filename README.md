# Laboratorio Ansible + Docker

## Descripción

Este laboratorio demuestra cómo administrar múltiples servidores Linux utilizando Docker y Ansible.

## Requisitos

- Docker
- Docker Compose
- Ansible

## Estructura

```
ansible-lab/
├── docker-compose.yml
├── inventory.ini
├── playbook.yml
└── README.md
```

## Crear los servidores

```bash
docker compose up -d
```

## Instalar Python

```bash
docker exec -it server1 bash
apt update
apt install -y python3
exit

docker exec -it server2 bash
apt update
apt install -y python3
exit
```

## Verificar conexión

```bash
ansible docker -i inventory.ini -m ping
```

## Ejecutar el playbook

```bash
ansible-playbook -i inventory.ini playbook.yml
```

## Tareas realizadas

- Mostrar el nombre del host.
- Mostrar el sistema operativo.
- Crear el directorio `/tmp/ansible-demo`.
- Crear el archivo `info.txt`.
- Escribir el nombre del servidor y sistema operativo en el archivo.
- Crear mediante un loop los directorios:
  - logs
  - backup
  - config
- Mostrar un mensaje únicamente cuando el sistema operativo sea Ubuntu.

##captura de pantalla 



<img width="364" height="334" alt="{441126FF-7466-4DF3-BE07-A09984040718}" src="https://github.com/user-attachments/assets/8d799e72-c3a4-4e85-a854-8d5d68733483" />



## Autor
 
Yolquin Grullon
