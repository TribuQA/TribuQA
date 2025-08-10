# Segundo historial de prompts utilizados en el curso: Automatización de APIs con Karate DSL y ChatGPT

Este archivo recopila el **historial detallado de prompts** utilizados el curso.
También puede ver el historial [👉 AQUÍ](https://chatgpt.com/share/6871c0bf-b344-8010-baf9-357ff09ff84a)

---

## Prompt 01: Feature de creación con POST

**Contexto:**  
Solicita ejemplos de automatización usando Karate DSL + Java, para el endpoint POST `/pet` de la API Petstore. Se pide una feature con un background y dos escenarios: uno que valida solo el `id` y otro que valida todo el body.

**Prompt original y mejorado:**  
```prompt
Actúa como un experto en automatización de pruebas con karate dsl y java.

La notebook que uso tiene como sistema operativo Windows 10 de 64 bits.

¿Cómo instalo java versión 17 (archivo comprimido) del distribuidor oracle y luego como lo agrego en las variables de entorno? ¿Quiero que el path de java sea C:\recursos?

El contrato indica lo siguiente:
	- La base url es: https://petstore3.swagger.io/api/v3
	- El metodo POST tiene un path: /pet
	- Tiene un body de ejemplo:
		{
		  "id": 10,
		  "name": "doggie",
		  "category": {
			"id": 1,
			"name": "Dogs"
		  },
		  "photoUrls": [
			"string"
		  ],
		  "tags": [
			{
			  "id": 0,
			  "name": "string"
			}
		  ],
		  "status": "available"
		}
	- El código de respuesta es: 200
	- El ejemplo de respuesta es:
		{
		  "id": 10,
		  "category": {
			"id": 1,
			"name": "Dogs"
		  },
		  "name": "doggie",
		  "photoUrls": [
			"string"
		  ],
		  "tags": [
			{
			  "id": 0,
			  "name": "string"
			}
		  ],
		  "status": "available"
		}

Necesito una feature que contenga:
	- Un background.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200 y solo el id.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200 y el body de la respuesta.
```
---

## Prompt 02: Runner con @Karate.Test y estructura de proyecto

**Contexto:**  
Solicita la generación del runner con la anotación `@Karate.Test` para Karate DSL versión 1.5.1, mostrando estructura de carpetas y archivos.

**Prompt original y mejorado:**  
```prompt
Ahora necesito generar el runner con el @Karate.Test donde la versión de karate dsl es 1.5.1 y la estructura donde está la feature y el fichero java es:

src
└── test
    └── java
        └── examples
            └── pet
                ├── post-escenario-simple.feature
                └── PetRunner.java
```
---

## Prompt 03: Feature con Scenario Outline para POST

**Contexto:**  
Solicita una feature en Karate DSL para el endpoint POST, usando scenario outline para validar varios casos.

**Prompt original y mejorado:**  
```prompt
Sigo con el método POST y ahora necesito otra feature que contenga:
	- Un background.
	- Un escenario outline desarrollado con karate dsl que valide el status code 200 y solo el id.
	- Un escenario outline desarrollado con karate dsl que valide el status code 200 y todo el body de la respuesta.
```
---

## Prompt 04: ID dinámico con expresiones embebidas

**Contexto:**  
Solicita modificar el campo `id` para que sea dinámico usando expresiones embebidas de Karate DSL.

**Prompt original y mejorado:**  
```prompt
Ahora ¿Puedes modificar solamente el id para que sea dinámico y que cumpla el concepto de expresiones embebidas de karate dsl?
```
---

## Prompt 05: Feature GET /pet/{petId} con validaciones y expresiones

**Contexto:**  
Solicita una feature para el endpoint GET que valide tanto el status code como los tipos de datos en la respuesta mediante expresiones de Karate.

**Prompt original y mejorado:**  
```prompt
Ahora tengo otro endpoint en el contrato que indica lo siguiente:
	- La base url es: https://petstore3.swagger.io/api/v3
	- El método GET tiene un path: /pet/{petId}
	- El parámetro petId es integer y obligatorio
	- El código de respuesta es: 200
	- El ejemplo de respuesta es:
		{
		  "id": 10,
		  "name": "doggie",
		  "category": {
			"id": 1,
			"name": "Dogs"
		  },
		  "photoUrls": [
			"string"
		  ],
		  "tags": [
			{
			  "id": 0,
			  "name": "string"
			}
		  ],
		  "status": "available"
		}

Necesito una feature que contenga:
	- Un background.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200 y solo el id.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200 y el tipo de datos del body en la respuesta usando expresiones embebidas de karate dsl.
```
---

## Prompt 06: Feature PUT /pet con validaciones

**Contexto:**  
Solicita una feature para el endpoint PUT `/pet`, con escenarios de validación similares al POST.

**Prompt original y mejorado:**  
```prompt
Ahora tengo otro endpoint en el contrato que indica lo siguiente:
	- La base url es: https://petstore3.swagger.io/api/v3
	- El método PUT tiene un path: /pet
	- Tiene un body de ejemplo:
		{
		  "id": 10,
		  "name": "doggie",
		  "category": {
			"id": 1,
			"name": "Dogs"
		  },
		  "photoUrls": [
			"string"
		  ],
		  "tags": [
			{
			  "id": 0,
			  "name": "string"
			}
		  ],
		  "status": "available"
		}
	- El código de respuesta es: 200
	- El ejemplo de respuesta es:
		{
		  "id": 10,
		  "name": "doggie",
		  "category": {
			"id": 1,
			"name": "Dogs"
		  },
		  "photoUrls": [
			"string"
		  ],
		  "tags": [
			{
			  "id": 0,
			  "name": "string"
			}
		  ],
		  "status": "available"
		}

Necesito una feature que contenga:
	- Un background.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200 y solo el id.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200 y el body de la respuesta.
```
---

## Prompt 07: Feature DELETE /pet/{petId}

**Contexto:**  
Solicita una feature para el endpoint DELETE `/pet/{petId}` que valide el status code 200.

**Prompt original y mejorado:**  
```prompt
Ahora tengo otro endpoint en el contrato que indica lo siguiente:
	- La base url es: https://petstore3.swagger.io/api/v3
	- El método DELETE tiene un path: /pet/{petId}
	- El parámetro petId es integer y obligatorio
	- El código de respuesta es: 200

Necesito una feature que contenga:
	- Un background.
	- Un escenario simple desarrollado con karate dsl que valide el status code 200.
```
---

## Prompt 08: Feature GET /pet/{petId} - Pruebas negativas

**Contexto:**  
Solicita una feature para pruebas negativas del endpoint GET `/pet/{petId}`, validando status codes 404 y 400.

**Prompt original y mejorado:**  
```prompt
Ahora poniendo foco en pruebas negativa para el endpoint GET con el path: /pet/{petId}

Necesito una feature que contenga:
	- Un background.
	- Un escenario simple desarrollado con karate dsl que valide el status code 404 y otro el status code 400
```
---

## Prompt 09: Ejecución de escenarios mediante tags en Maven

**Contexto:**  
Solicita ejemplos de comandos Maven para ejecución selectiva de escenarios via tags.

**Prompt original y mejorado:**  
```prompt
Ahora quiero ejecutar mis escenarios mediante tags

Sigo con los escenarios del POST

Necesito:
	- Un comando maven que ejecute un escenario
	- Un comando maven que ejecute dos o más escenarios
	- Un comando maven que ejecute un escenario e ignore otros 
```
---

## Prompt 10: Customización avanzada de features y configuración

**Contexto:**  
Solicita mejoras para la feature de escenarios POST, incluyendo configuración en `karate-config.js`, ids dinámicos, importación de requestBody desde JSON y log de respuesta.

**Prompt original y mejorado:**  
```prompt
Ahora quiero customizar mis features. Esta es mi feature para los escenarios POST:

Feature: Validar creación de mascotas usando POST /pet
...

y este es mi karate-config.js
...

Necesito:
	- Que la url debe estar en karate-config.js
	- Que cada escenario tenga su propio requestBody con un id dinámico entre el 1 y 100
	- Que el requestBody se importe y esté en un archivo json
	- Al finalizar cada escenario se imprima la respuesta con un print o log

Importante: La versión de karate que uso es 1.5.1
```
---

## Prompt 11: README profesional para el proyecto

**Contexto:**  
Solicita un README profesional que incluya todos los requisitos, tecnologías, ejemplos, autor, emojis, links y buenas prácticas.

**Prompt original y mejorado:**  
```prompt
Ahora quiero informar lo que se necesita en mi proyecto para su ejecución si otros lo usan o lo ven

Entonces necesito un README profesional donde se indique: 
	- Título y tecnologías que se necesita con sus url correspondiente 
	- Indicar que se automatizó el endpoint (GET, POST, PUT y DELETE) de pet y el contrato: https://petstore3.swagger.io/
	- Indicar cómo instalar y ejecutar los test ya sea mediante el IDE y mediante la terminal con tags
	- Indicar que use CHATGPT y un ejemplo de prompt como el que pedí para el endpoint GET
	- Autor
	- Icono o emojis
	- Las urls que se documentan como hipervínculo 
	- Algo adicional según buenas prácticas
```
---

## Prompt 12: Subir proyecto a GitHub con git

**Contexto:**  
Solicita los pasos para configurar usuario y subir el proyecto a GitHub usando git.

**Prompt original y mejorado:**  
```prompt
Ahora quiero subir mi proyecto a GITHUB y ya tengo repositorio nuevo y git en mi máquina

Entonces necesito paso a paso:
	- Tener configurado mi usuario para no tener problemas al subir
	- Los comandos git necesarios
```
