# Wikipedia Service

Librería para utilizar la API de Wikipedia. 

## Primeros pasos

Las siguientes instrucciones permitirán obtener una copia del repositorio funcionando en la aplicación de quien lo requiera. 

### Prerequisitos

Para utilizar la libreria es necesario clonar el repositorio. Es posible realizarlo mediante el siguiente comando git:

```
git submodule add <URL del repositorio> <Carpeta de destino>
```

Si la librería ya se encuentra en uso, para obtener la última versión del módulo se deberá realizar el siguiente comando git: 

```
git submodule foreach git pull origin master
git submodule update --init
```

### Modo de uso

En un principio, para establecer la conexión con la aplicación de Wikipedia se debe realizar la siguiente instrucción: 

```
APIConnection apiConnection = WikipediaServiceModule.getInstance().getAPIConnection(); 
```

Para obtener la definición de un término en particular se debe llamar a la función 'getDefinition(<termino_a_buscar>)'. Esta función lanza una excepción del tipo Exception cuando hubo un error al conectarse con la Wikipedia. A continuación se muestra un ejemplo de como se utilizaría: 

```
 try{
	[...]
	WikiDefinition def = apiConnection.getDefinition(term);
	[...]
 }
 catch (Exception e) {
	[...] 
	e.getMessage();
	[...]
 }
```

Las funciones que se pueden realizar con un objeto WikiDefinition son las siguientes: 

* String getTerm(): Se obtiene el término que el usuario buscó. 

* String getMeaning(): Se obtiene la definición del término buscado. 
	
## Autores

* **Fritz Jonathan** [Github](https://github.com/jonifritz)

* **Panzone Caterina** [Github](https://github.com/Caterina-Panzone)

* **Sly Agustin** [Github](https://github.com/Sly-Agustin)




