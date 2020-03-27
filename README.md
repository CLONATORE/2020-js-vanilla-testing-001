# 2020-js-vanilla-testing-001

<p align="center">
    <img src="https://github.com/GeeksHubsAcademy/hello-world/blob/master/assets/media/logo/logo.png" >	
</p>

## Temario

* [Estructura de un proyecto Testing]()
* [Requisitos]()
* [Node-js & npm]()
* [Jest - Framework Testing]()
* [Mi primer Test]()
* [Practicando en local]()
* [Conclusiones]()

### Estructura de un proyecto Testing
```
Para la realización de un desarrollo guiado por pruebas aka 'Development Testing' se necesita 
tener un entorno configurado para la realización de las mismas en local.

En la practica vamos a usar JavaScript Vanilla como lenguaje de programación.
Por encima usaremos un Framework de Testing denominado 'Jest'. Éste permite de manera muy simple
hacer pequeñas pruebas para llegar a nuestro propósito de desarrollo.
```

### Requisitos
```
Es necesario para poder ejecutar estas pruebas en tu local que tengas instalado un pequeño stack.
También apoyarte en la parte de teoria de Git y Github que distes semanas atrás.
```

#### Node-js & npm
```
Para la instalación de estos recursos hemos dejado los enlaces en las referencias.
Hemos elegido unos pequeños tutoriales muy fáciles de seguir dependiendo de la plataforma que uses (Win/Lin/Mac).

Siempre puedes apoyarte en el profesor en caso de que surja algún problema.

Para saber que todo está correctamente instalado debemos abrir la terminal git-bash y ejecutar estos comandos:
    '$ node -v'
    '$ npm -v'
```

#### Jest - Framework Testing
```
Una vez hayas instalado Node-js y npm simplemente tienes que abrir la terminal de git-bash.

Crea una carpeta llamada '001-testing':
    $ mdkir 001-testing
    
Accede a ella :
    $ cd 001-testing

Instala 'Jest' con el siguiente comando:
    $ npm install --save-dev jest
 
Valida que la terminal te ha mostrado un mensaje terminado como este:
      npm WARN 001-testing No description
      npm WARN 001-testing No repository field.
      npm WARN 001-testing No README data
      npm WARN 001-testing No license field.
     
      + jest@25.2.3
      added 474 packages from 282 contributors and audited 1095501 packages in 31.784s
      found 0 vulnerabilities

Para saber que todo se ha instalado correctamente, dentro de nuestra carpeta ejecutamos el comando:
    $ ls

Debes visualizar estas dos carpetas:
    $ node_modules/  package-lock.json
     
```

### Mi primer Test
```
Para proceder a nuestro primer test, necesitamos crear dos fichero de texto plano.

Un primer fichero debe de contener nuestro algoritmo (test01.js)
El segundo fichero es necesario para que 'Jest' pueda lanzar el test de nuestro algoritmo (suite.test.js).

En la propia carpeta '001-testing' ejecutamos el siguiente comando:
    $ touch suite.test.js

Dicho fichero va a permitir a 'Jest' ejecutar la bateria de Test que vamos a crear.
En la terminal, abrimos nuestro editor y copiamos el siguiente código:

'
    const concatenar = require('./test01.js');

    test('Concatena Hello + Victor to equal "Hello Victor"', function () => {
    // Arrange
    var expected = "Hello Victor";

    // Act
    var result = concatenar("Victor");

    // Assert
    expect(result).toBe(expected);
    });

'

Fíjese que estamos diseñando un test sin tener la implementación todavía.
Estamos dando por hecho que nuestra función 'concatenar' necesita un parámetro de entrada
y el resultado es la concatenación con la palabra "Hello".

Ahora vamos a rellenar de contenido el fichero 


En la propia carpeta '001-testing' ejecutamos el siguiente comando:
    $ touch test01.js

En este fichero vamos añadir una pequeña función que devuelva una 'string' concatenendo un 
parámetro de entrada.


```

### Practicando en local
```
```

### Conclusiones
```
```

### Referencias
* [Jest Framework](https://jestjs.io/)
* [Instalación node-js & npm Windows](https://tutobasico.com/instalar-nodejs-y-npm/)
* [Instalación node-js & npm Linux](https://luismasdev.com/instalar-nodejs-en-windows/)
* [Instalacion node-js & npm Mac](https://medium.com/javascript-comunidad/c%C3%B3mo-instalar-node-js-y-npm-en-mac-9d80f26fb88d)


