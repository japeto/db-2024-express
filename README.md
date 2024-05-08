# Contenedor de la base de datos

## Crear la imagen de docker con el esquema y los datos pre-guardados

```
cd database_postgres
docker build -t ${USER_NAME}/mande_db .
```

## Poner a correr el servidor de bases de datos

```
docker run --name mande_db -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d ${USER_NAME}/mande_db
```
# Contenedor para el backend

## Instalar las dependencias

Debes estar en la carpeta raíz del proyecto. 

```
cd backend_express
```

## Crear el contenedor para el backend

`docker build -t japeto/mande_ui .`

## Instalar las dependencias con npm

`docker run --rm --name mande_ui japeto/mande_ui /bin/bash`

# Probar la aplicación

Visite las direcciones

`localhost:3000/hello`
`localhost:3000/usuario`
`localhost:3000/usuario/1`
`localhost:3000/crear`

