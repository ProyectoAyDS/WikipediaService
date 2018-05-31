# Wikipedia Service

Librería que obtiene el significado de un término en específico, a partir de la información almacenada en la Wikipedia. 

## Primeros pasos

Las siguientes instrucciones permitirán obtener una copia del repositorio en cualquier aplicacion particular.

### Prerequisitos

Para utilizar la libreria es necesario clonar el repositorio. Es posible realizarlo mediante el siguiente comando git:

```
git submodule add <URL del repositorio> <path_carpeta_destino>
```

Si la librería ya se encuentra en uso, para obtener la última versión del módulo se deberá realizar los siguientes comandos git: 

```
//Cambiar al directorio del submodulo 
cd submodule_dir 

//Chequear la rama deseada 
git checkout master 

//Actualizar
git pull
```

### Modo de uso

En un principio, para establecer la conexión con la aplicación de Wikipedia se debe realizar la siguiente instrucción: 

```
APIConnection apiConnection = WikipediaServiceModule.getInstance().getAPIConnection(); 
```

Para obtener la definición de un término en particular se debe llamar a la función 'getDefinition(String <termino_a_buscar>)'. Esta función lanza una excepción del tipo Exception cuando hubo un error al conectarse con la Wikipedia. A continuación se muestra un ejemplo de como se utilizaría: 

```
 try{
	[...]
	WikiDefinition def = apiConnection.getDefinition("hola");
	[...]
 }
 catch (Exception e) {
	[...] 
	e.getMessage();
	[...]
 }
```

Las operaciones que se pueden realizar con un objeto WikiDefinition son las siguientes: 

* String getTerm(): Retorna el término que el usuario buscó. 

* String getMeaning(): Retorna la definición del término buscado. 
	
## Autores

* **Fritz Jonathan** [Github](https://github.com/jonifritz)

* **Panzone Caterina** [Github](https://github.com/Caterina-Panzone)

* **Sly Agustin** [Github](https://github.com/Sly-Agustin)




