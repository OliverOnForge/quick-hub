
# Docker

Docker es una plataforma de código abierto que facilita la creación, el despliegue y la ejecución de aplicaciones al usar contenedores.

Los contenedores son unidades de software ligeras y portátiles que empaquetan una aplicación junto con todas sus dependencias segurando que funcione de manera consistente en cualquier entorno

---

## INDICE

- [Docker](#docker)
  - [INDICE](#indice)
  - [Repositorios de conetenedores](#repositorios-de-conetenedores)
  - [Sobre Docker](#sobre-docker)
    - [Cuándo usar Docker](#cuándo-usar-docker)
    - [Cuándo no usar Docker](#cuándo-no-usar-docker)
    - [Qué es Docker](#qué-es-docker)
    - [Qué es un Contenedor](#qué-es-un-contenedor)
    - [Cómo funciona](#cómo-funciona)
    - [Partes principales](#partes-principales)
    - [Docker Hub y Registros](#docker-hub-y-registros)
    - [Buenas prácticas de Docker](#buenas-prácticas-de-docker)
    - [Imágenes eficientes](#imágenes-eficientes)
    - [Herramientas útiles](#herramientas-útiles)
  - [Gestión de Imágenes](#gestión-de-imágenes)
    - [docker build](#docker-build)
    - [docker pull](#docker-pull)
    - [docker images](#docker-images)
    - [docker rmi](#docker-rmi)
    - [docker tag](#docker-tag)
  - [Ciclo de Vida de Contenedores](#ciclo-de-vida-de-contenedores)
    - [docker run](#docker-run)
    - [docker ps](#docker-ps)
    - [docker stop / start](#docker-stop--start)
    - [docker rm](#docker-rm)
    - [docker exec](#docker-exec)
  - [Estado e Inspección](#estado-e-inspección)
    - [docker logs](#docker-logs)
    - [docker inspect](#docker-inspect)
    - [docker stats](#docker-stats)
    - [docker port](#docker-port)
    - [docker top](#docker-top)
  - [Volúmenes y Persistencia](#volúmenes-y-persistencia)
    - [docker volume create](#docker-volume-create)
    - [docker volume ls](#docker-volume-ls)
    - [docker volume inspect](#docker-volume-inspect)
    - [docker volume rm](#docker-volume-rm)
    - [docker volume prune](#docker-volume-prune)
  - [Redes en Docker](#redes-en-docker)
    - [docker network ls](#docker-network-ls)
    - [docker network create](#docker-network-create)
    - [docker network connect](#docker-network-connect)
    - [docker network disconnect](#docker-network-disconnect)
  - [Mecanismos fundamentales](#mecanismos-fundamentales)
    - [Capas de imagen](#capas-de-imagen)
    - [Instrucciones del Dockerfile](#instrucciones-del-dockerfile)
    - [Contexto de construcción](#contexto-de-construcción)
    - [Modo Interactivo vs Detached](#modo-interactivo-vs-detached)
    - [Mapeo de puertos](#mapeo-de-puertos)
    - [Variables de entorno](#variables-de-entorno)
    - [Entrypoint vs CMD](#entrypoint-vs-cmd)
    - [Persistencia con Bind Mounts](#persistencia-con-bind-mounts)
    - [Docker Compose](#docker-compose)
    - [Limpieza del sistema](#limpieza-del-sistema)
  - [Ejercicios prácticos](#ejercicios-prácticos)
    - [Práctica crear un Dockerfile](#práctica-crear-un-dockerfile)
    - [Práctica construir una imagen](#práctica-construir-una-imagen)
    - [Práctica correr un contenedor](#práctica-correr-un-contenedor)
    - [Práctica mapeo de puertos](#práctica-mapeo-de-puertos)
    - [Práctica entrar a un contenedor](#práctica-entrar-a-un-contenedor)
    - [Práctica persistencia con volúmenes](#práctica-persistencia-con-volúmenes)
    - [Práctica conectar contenedores](#práctica-conectar-contenedores)
    - [Práctica ver logs en tiempo real](#práctica-ver-logs-en-tiempo-real)
    - [Práctica limitar recursos](#práctica-limitar-recursos)
    - [Práctica usar Docker Compose](#práctica-usar-docker-compose)
    - [Práctica subir imagen a Docker Hub](#práctica-subir-imagen-a-docker-hub)
    - [Práctica limpieza general](#práctica-limpieza-general)
  - [Hypervisor](#hypervisor)
  - [estructura](#estructura)
  - [estructura dos](#estructura-dos)
  - [instalacion](#instalacion)
  - [docker file](#docker-file)
  - [ejecutar contenedor](#ejecutar-contenedor)
  - [comandos](#comandos)
  - [modo interactivo](#modo-interactivo)
  - [puertos](#puertos)
  - [logs](#logs)
  - [inspeccionar contenedores](#inspeccionar-contenedores)
  - [variables de entorno](#variables-de-entorno-1)
  - [contenedores sin servicios](#contenedores-sin-servicios)
  - [Volumenes](#volumenes)
    - [que son los volumenes](#que-son-los-volumenes)
    - [Volumenes de docker](#volumenes-de-docker)
    - [compartir archivos entre conenedores](#compartir-archivos-entre-conenedores)
    - [Volumenes manuales](#volumenes-manuales)
    - [Redes](#redes)
    - [conectando contenedor a red](#conectando-contenedor-a-red)
    - [Red hosts](#red-hosts)
  - [imagenes](#imagenes)
    - [que son las imagenes](#que-son-las-imagenes)
    - [primer imagen](#primer-imagen)
    - [copiando archivos](#copiando-archivos)
    - [variables de entorno](#variables-de-entorno-2)
    - [ejecutar servicios](#ejecutar-servicios)
    - [endpoint vs CMD](#endpoint-vs-cmd)
    - [Dokerizar script python](#dokerizar-script-python)
    - [doker hub](#doker-hub)
    - [dockenizar script node](#dockenizar-script-node)
  - [Docker compose](#docker-compose-1)
    - [que es docker compose](#que-es-docker-compose)
    - [servicions](#servicions)
    - [redes](#redes-1)
    - [servicios](#servicios)
    - [volumenes](#volumenes-1)
    - [variables de entorno](#variables-de-entorno-3)
    - [stack local](#stack-local)
    - [docker compose build](#docker-compose-build)
  - [introducciona kubernetes](#introducciona-kubernetes)
    - [que son los orquestadores](#que-son-los-orquestadores)
    - [conceptos basicos](#conceptos-basicos)
    - [instalacion](#instalacion-1)
    - [primer pod](#primer-pod)
    - [port Forward](#port-forward)
    - [Terminal interactiva](#terminal-interactiva)
    - [eliminar pods](#eliminar-pods)
    - [log en pods](#log-en-pods)
  - [Consumir API docker](#consumir-api-docker)
  - [doker portainer](#doker-portainer)
  - [docker applicaciones graficas](#docker-applicaciones-graficas)
  - [entorno VScode](#entorno-vscode)

---

## Repositorios de conetenedores

Son repositorios especializados en almacenar contenedores de docker hay repositorios publicos y privados.

El repositorio publico mas popular es:
[Docker hub](https://hub.docker.com/)

Aquí tienes la estructura para tu manual de Docker, siguiendo exactamente la misma organización, jerarquía y estilo pedagógico que utilizaste en tu guía de Git.

## Sobre Docker

### Cuándo usar Docker

### Cuándo no usar Docker

### Qué es Docker

### Qué es un Contenedor

### Cómo funciona

### Partes principales

### Docker Hub y Registros

### Buenas prácticas de Docker

### Imágenes eficientes

### Herramientas útiles

## Gestión de Imágenes

### docker build

### docker pull

### docker images

### docker rmi

### docker tag

## Ciclo de Vida de Contenedores

### docker run

### docker ps

### docker stop / start

### docker rm

### docker exec

## Estado e Inspección

### docker logs

### docker inspect

### docker stats

### docker port

### docker top

## Volúmenes y Persistencia

### docker volume create

### docker volume ls

### docker volume inspect

### docker volume rm

### docker volume prune

## Redes en Docker

### docker network ls

### docker network create

### docker network connect

### docker network disconnect

## Mecanismos fundamentales

### Capas de imagen

### Instrucciones del Dockerfile

### Contexto de construcción

### Modo Interactivo vs Detached

### Mapeo de puertos

### Variables de entorno

### Entrypoint vs CMD

### Persistencia con Bind Mounts

### Docker Compose

### Limpieza del sistema

## Ejercicios prácticos

### Práctica crear un Dockerfile

### Práctica construir una imagen

### Práctica correr un contenedor

### Práctica mapeo de puertos

### Práctica entrar a un contenedor

### Práctica persistencia con volúmenes

### Práctica conectar contenedores

### Práctica ver logs en tiempo real

### Práctica limitar recursos

### Práctica usar Docker Compose

### Práctica subir imagen a Docker Hub

### Práctica limpieza general

## Hypervisor

se encarga del simulado del hardware

## estructura

linux > programas, librerias , etc

## estructura dos

- dockerfile

- imagen

- contenedor

- docker hub

- docker daemon/cli se ejecuta en segundo plano y es el que se encarga de gestionar 

> docekr es un cliente servidor

## instalacion

docker solo se puede ejecutar sobre linux, para los otros sitemas es necesaio una maquina virtual

instalr a unbunto usando apt

## docker file

a partir de el se genera una imagen

## ejecutar contenedor

## comandos

docker - comstrar comandos
--help
container -operaciones con contenerdores
run 
start
detach

## modo interactivo

## puertos

## logs

## inspeccionar contenedores

## variables de entorno

## contenedores sin servicios

## Volumenes

### que son los volumenes

### Volumenes de docker

### compartir archivos entre conenedores

### Volumenes manuales

### Redes

### conectando contenedor a red

### Red hosts

## imagenes

### que son las imagenes

### primer imagen

### copiando archivos

### variables de entorno

### ejecutar servicios

### endpoint vs CMD

### Dokerizar script python

### doker hub

### dockenizar script node

## Docker compose

### que es docker compose

### servicions 

### redes

### servicios 

### volumenes

### variables de entorno

### stack local

### docker compose build

## introducciona kubernetes

### que son los orquestadores

### conceptos basicos

### instalacion

### primer pod

### port Forward

### Terminal interactiva

### eliminar pods

### log en pods

## Consumir API docker

## doker portainer

## docker applicaciones graficas

## entorno VScode