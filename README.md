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
* [Referencias]()

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

Para saber que todo está correctamente instalado debemos abrir la terminal git-bash y ejecutar estos comandos:
    '$ node -v'
    '$ npm -v'

Dichos comandos deben de mostrar las versiones de cada recurso.
En caso de que no estén bien instaladas, saldrá un error.

Siempre puedes apoyarte en el profesor en caso de que surja algún problema.

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

Debes visualizar estas dos elementos:
    $ node_modules/  package-lock.json
    
Para poder ejecutar 'Jest' se necesita crear un fichero y añadir la dependencia.
    $ touch package.json

En la terminal, abrimos nuestro editor y copiamos el siguiente código:

'
{
  "scripts": {
    "test": "jest"
  }
}
'
Guardamos y cerramos el editor.

Para saber que todo se ha seguido correctamente, dentro de nuestra carpeta ejecutamos el comando:
    $ ls

Debes visualizar estos tres elementos:
    $node_modules/  package.json  package-lock.json
    
```

### Mi primer Test
```
Para proceder a nuestro primer test, necesitamos crear dos fichero de texto plano.

Un primer fichero debe de contener nuestro algoritmo (test01.js)
El segundo fichero es necesario para que 'Jest' pueda lanzar el test de nuestro algoritmo (suite.test.js).

```

#### Fichero Suite Test
```
En la propia carpeta '001-testing' ejecutamos el siguiente comando:
    $ touch suite.test.js

Dicho fichero va a permitir a 'Jest' ejecutar la bateria de Test que vamos a crear.
En la terminal, abrimos nuestro editor y copiamos el siguiente código:

' 
    const concatenar = require('./test01.js');                                       //L-1

    test('Concatena Hello + Victor to equal "Hello Victor"', function ()    {        //L-3
    // Arrange
    var expected = "Hello Victor";                                                   //L-5

    // Act
    var result = concatenar("Victor");                                               //L-8
    
    // Assert
    expect(result).toBe(expected);                                                   //L-11
    });                                                                              //L-12

'

Fíjese que estamos diseñando un test sin tener la implementación todavía.
Estamos dando por hecho que nuestra función 'concatenar' necesita un parámetro de entrada
y el resultado es la concatenación con la palabra "Hello".

A continuación describimos cada una de las líneas:

L-1  - Permite a 'Jest' acceder a la función de nuestro algoritmo de concatenación.
L-3  - Define la cabecera de una función de Testing para el framework de 'Jest'. 
L-5  - Inicializamos variables.
L-8  - Llamámos al método de nuestro Test.
L-11 - Comparamos nuestro resultado esperado con el resultado del método que hemos desarrollado.
L-12 - Cierre de la función.

Cerramos el editor y volvemos a la terminal.
````

#### Fichero de Test
```
Ahora vamos a desarrollar nuestro algoritmo de concatenación:

En la propia carpeta '001-testing' ejecutamos el siguiente comando:
    $ touch test01.js

En este fichero vamos añadir una pequeña función que devuelva una 'string' concatenendo un 
parámetro de entrada.

Abrimos nuestro editor y copiamos el siguiente código:

' 
    function concatenar(param) {                                                     //L-1
        return "Hello "+param;                                                       //L-2
    }                                                                                //L-3
   
    module.exports = concatenar;                                                     //L-5
'

A continuación describimos cada una de las líneas:


L-1  - Define la cabecera de nuestro algoritmo, junto con el parametro de entrada.
L-2  - Línea que indica la devolución del resultado de nuestro método.
L-3  - Cierre de nuestro algoritmo.
L-5  - Almacena la función 'concatenar' en una variable que luego 'Jest' recupera con 
       la línea 1 del fichero suite.test.js 
       
Cerramos el editor y volvemos a la terminal.
```

### Practicando en local
```
Ahora simplemente vamos a lanzar Jest por la terminal para comprar que nuestro test es correcto.

Ejecutamos el siguiente comando :
    $ npm run test
    
Debemos de obtener la siguiente salida:
    '
        > @ test C:\Users\vbolinches\Documents\001-testing
        > jest

        PASS ./suite.test.js
          √ Concatena Hello + Victor to equal "Hello Victor" (3ms)

        Test Suites: 1 passed, 1 total
        Tests:       1 passed, 1 total
        Snapshots:   0 total
        Time:        3.892s
        Ran all test suites.
    '

```

### Conclusiones
```
Esta práctica ha sido guiada para poder familiarizarse con el entorno de testing de Jest.
Se han usado comandos de bash.
Se ha instalado node-js y npm.
Se ha creado una solución de cero y se ha configurado la carpeta para el lanzamiento de un test con Jest.
Se ha explicado los elementos necesarios para poder definir una función y poder testearla.
```

### Referencias
* [Jest Framework](https://jestjs.io/)
* [Instalación node-js & npm Windows](https://tutobasico.com/instalar-nodejs-y-npm/)
* [Instalación node-js & npm Linux](https://luismasdev.com/instalar-nodejs-en-windows/)
* [Instalacion node-js & npm Mac](https://medium.com/javascript-comunidad/c%C3%B3mo-instalar-node-js-y-npm-en-mac-9d80f26fb88d)



