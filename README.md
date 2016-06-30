# Documentación App Móvil

## Actualización de la información del usuario

> Para lograr la actualización de datos del usuario en la app móvil de debe seguir apuntando a la URL que ya es conocida.
Está vez se debe llamar al metodo **actualizaInfoUsuario** el cual será el encargado de hacer la actualización.

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

:::css
(
	{
		"mensaje":"No se pudo actualizar la información",
		"data":[],
		"continuar":0
	}
)

##### Éxito

:::css
(
	{
		"mensaje":"La información del usuario fue actualizada con éxito",
		"data":"",
		"continuar":1
	}
)