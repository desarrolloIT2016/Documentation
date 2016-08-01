# Documentación App Móvil

## Actualización de la información del usuario

> Para lograr la actualización de datos del usuario en la app móvil de debe seguir apuntando a la URL que ya es conocida.
Está vez se debe llamar al metodo `actualizaInfoUsuario` el cual será el encargado de hacer la actualización.

http://www.tu...com/Movil/actualizaInfoUsuario

Se deben enviar los siguientes parámetros:


#### Campos que se van a actualizar

**nombre1**: Primer nombre de la persona

**nombre2**: Segundo nombre de la persona

**apellido1**: Primer apellido de la persona

**apellido2**: Segundo apellido de la persona

**email**: Email de la persona

**genero**: Genero de la persona 1 Femenino, 2 Masculono, 3 Otro

**imagen**: Imagen de la persona en formato Base64

#### Campo condicional

Este campo es el encargado de hacer la condición y decidir a que persona se va a actualizar

**idPersona**: Id único de la persona que se va a actualizar.


#### Debe quedar así la url


http://www.tu...com/Movil/actualizaInfoUsuario?nombre1=XXXX&nombre2=XXX&apellido1=XXX&apellido2=XXX&email=XXX&genero=XXX&imagen=XXX&idPersona=XXX


#### Respuesta del API

##### Error

```javascript
(
	{
		"mensaje":"No se pudo actualizar la información",
		"data":[],
		"continuar":0
	}
)
```

##### Éxito
```javascript
(
	{
		"mensaje":"La información del usuario fue actualizada con éxito",
		"data":"",
		"continuar":1
	}
)
```

## Recordar clave de usuario

Si el usuario de la app móvil ha olvidado debe tener la forma de recordarla, por medio de este pequeño funcionamiento del api podrá hacerlo. Este funcionamiento es para aplicaciones móviles.

Para poder acceder a la información debe hacer referencia a la URL que ya es conocida `http://www.tu...com/Movil/recordarClave`, luego de acceder a ella debe llamar al método `recordarClave`. Los parámetros que debe enviar a esta url son los siguientes:

* email (Este será el email del usuario que olvidó la clave)

la URL debe quedar de la siguiente manera:

http://www.tu...com/Movil/recordarClave?email=XXXX

El sistema empezará a hacer una verificación del email para ver si existe en la base de datos, el sistema retornara un arreglo en formato JSON con el estado de la transacción, la estructira del arreglo será la siguiente: 

```javascript
(
	{
		"mensaje":"Mensaje que avisará el estado de la transacción",
		"data":"",
		"continuar":1
	}
)
```

Las variables retornadas en el JSON indican lo siguiente:

* **mensaje:** Indica un mensaje de éxito o error dependiendo el caso.
* **data:** retornará información referente al proceso que se esté realizando, si es necesario.
* **continuar:** Variable que indicará 1 si es correcto el proceso ó 0 si es incorrecto


- - -
