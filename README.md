[![](https://img.shields.io/badge/IBM%20Cloud-powered-blue.svg)](https://cloud.ibm.com)
[![Platform](https://img.shields.io/badge/platform-nodejs-lightgrey.svg?style=flat)](https://developer.ibm.com/node/)
[![](https://img.shields.io/discord/734849667174498465?logo=discord)](https://discord.gg/Q9At74C)

# Desafio 05  | Empresa XYZ

- [1. Reto de negocio](#2-reto-de-negocio)
- [2. Objetivo](#3-objetivo)
  - [2.1. Tecnología](#31-tecnología)
- [3. Desarrollando la solución](#4-desarrollando-la-solución)
  - [3.1. Pre-requisitos](#41-pre-requisitos)
  - [3.2. Resumen de las tareas](#42-resumen-de-las-tareas)
  - [3.3. Desarrollo](#43-desarrollo)
- [4. Envío](#5-envío)
- [5. Sobre la evaluación](#6-sobre-la-evaluación)

## Para Ayudarte

- [Material de apoyo](#material-de-apoyo)
- [Solución de problemas](#solución-de-problemas)
- [Licencia](#licencia)


## 1. Reto de negocio

El proceso de transformación digital de Empresa XYZ, demanda una búsqueda continua de talento con skills digitales. El reclutamiento de este talento, escaso en el mercado, representa un enorme desafío para el equipo de RRHH y de IT. El time-to-fill promedio para el reclutamiento de recursos con estos perfiles es actualmente de 6 meses. Una de las barreras que impide mejorar estos tiempos es la falta de disponibilidad de los supervisores y team leads para realizar las entrevistas a los candidatos.
 
El desafío que propone el Empresa XYZ es crear un entrevistador virtual, basado en IA, que pueda ser usado para reclutar candidatos tanto para posiciones entry-level como para niveles de experiencia senior y semi-senior. El entrevistador virtual, a través de una app, deberá llevar una entrevista de forma 100% autónoma y al finalizarla ser capaz de establecer un score y una recomendación de hiring o no. El objetivo es reducir el esfuerzo inicial de pre-selección de candidatos y sólo realizar la entrevista con los que haya seleccionado el algoritmo.

## 2. Objetivo

Empresa XYZ cuenta constantemente con vacantes para desarrollo de software, por lo que este desafío se centrará en una entrevista a desarrolladores con conocimientos en Angular y Java. El participante entrenará un servicio de IA para calificar o soportar las respuestas de los candidatos.

Para este desafío Empresa XYZ usará la herramienta [Watson Discovery](https://cloud.ibm.com/catalog/services/discovery) para construir un modelo de busqueda de conocimiento que le permita validar las respuestas de los candidatos con la evidencia propicia.

La idea principal del reto es entrenar una colección con documentos acerca de Angular y Java que responden a las preguntas que se hacen en la entrevista. El participante mejorará el entendimiento que tiene Watson Discovery entre las posibles respuestas y los documumentos provistos.

### 2.1. Tecnología

[Watson Discovery](https://cloud.ibm.com/catalog/services/discovery) es un motor de análisis de contenido y búsqueda cognitiva a las aplicaciones para identificar patrones, tendencias e información útil que impulse una mejor toma de decisiones. Unifica de forma segura datos estructurados y no estructurados con contenido enriquecido y utiliza un lenguaje de consulta simplificado para eliminar la necesidad de filtrar manualmente los resultados.


<div align="center">
    <a href="https://youtu.be/rNlGm26k95o">
       <img width="50%" src="./doc/source/images/THUMB-TUTORIAL-5-ES.png" alt='video'>
    </a>
</div>


## 3. Desarrollando la solución

### 3.1. Pre-requisitos

Para poder realizar este desafío, se deben cumplir con los siguientes requisitos previos:

- Regístrate en [Maratón Behind the Code](https://maratona.dev/es) y confirma tu e-mail de registro.
- Tener una cuenta en [IBM Cloud](https://ibm.biz/registro-maratona), que puede ser una cuenta GRATUITA o de pago (no es necesario registrarse en el evento con el mismo correo electrónico utilizado para crear tu cuenta IBM Cloud).

### 3.2. Resumen de las tareas

1. Crear servicio de [Watson Discovery](https://cloud.ibm.com/catalog/services/discovery) en IBM Cloud
2. Acceder a las páginas cuyas URLs estan listadas en el númeral [4.3](#43-desarrollo)
3. Crear documentos en formato JSON con la forma especificada en el númeral [4.3](#43-desarrollo)
4. Crear una colleción nueva en Watson Discovery y hacer upload de sus documentos
5. Entrenar un modelo de relevancia con _queries_ en Watson Discovery basado en los documentos previstos
6. Accede a la página https://Empresa XYZ.maratona.dev, prueba y envia tu solución.

### 3.3. Desarrollo

Durante el desafío, enfrentará dos problemas comunes para un científico de datos, el de estructurar datos y curar modelos de Machine Learning. El primero se encontrará al extraer información de las páginas web que se enumeran a continuación, y el segundo se encontrará al probar el modelo en Watson Discovery con consultas personalizadas. 


- https://desarrolloweb.com/articulos/introduccion-componentes-angular2.html
- https://www.acontracorrientech.com/directives-en-angular-guia-practica
- https://medium.com/@ogomez/guia-rapida-para-entender-el-patron-redux-y-angular-con-ngrx-e60d39d35f1b
- https://profile.es/blog/angular-templates-las-directivas-ng-template-ng-container-y-ngtemplateoutlet/
- https://guru99.es/java-interface/
- https://www.oscarblancarteblog.com/2017/02/28/ordenar-listas-en-java/
- https://www.javanicaragua.org/2019/09/21/introduccion-a-maven-primeros-pasos/
- https://desarrolloweb.com/articulos/servicios-angular.html
- https://desarrolloweb.com/articulos/trabajar-modulos-angular.html
- https://www.adictosaltrabajo.com/2015/09/25/introduccion-a-colecciones-en-java
- https://experto.dev/patron-de-diseno-java-singleton/
- https://experto.dev/patron-de-diseno-strategy-en-java/


A partir de estas URLs (_exclusivamente_), pedimos que cree documentos JSON con las siguientes claves y valores:

```json
{
  "body": "Cuerpo del contenido ",
  "title": "Título de la página o sección",
  "url": "URL original del contendio"
}
```
**Los nombres de las claves deben ser exactamente los mismos para garantizar que su modelo pueda evaluarse correctamente**. Usted es responsable por la creación consitente de los documentos, recuerde que la `url` debe estar dentro del listado provisto y el `title` debe ser de la página o sección según usted lo considere. Recuerde que el formato JSON no permite saltos de lineas ni algunos caracteres especiales los cuales deben ser manipulados correctamente. (Cree los documentos según el contexto del proceso de selección de Empresa XYZ)

[Encuente aqui un ejemplo de documento JSON completo](./doc/source/dataset/que_es_angular.json).

Después de crear los documentos, debe crear una colección en Watson Discovery e insertarlos en su colección. Después de cargar los documentos, debe entrenar un modelo de relevancia con los resultados de querias a algunas frases, identificando qué documentos son relevantes para esa frase y cuáles no. 

> Consejo: el paso de cargar documentos en Watson Discovery puede tardar unos minutos y, a veces, fallar. Se recomienda que solo se cargue un documento a la vez para asegurarse de que no haya fallas.

A continuación encuentra las preguntas que Empresa XYZ usa en la entrevista y algunos ejemplos de respuestas posibles para cada una. Usted debe usar su propio conocimiento o conocimiento que encuentre en fuentes de información para entrenar el modelo de relevancia con **posibles frases de respuestas** (_queries_) que los candidatos puedan usar contra los documentos que usted ha cargado en la colección de Watson Discovery. 


<div align="center">
  <h3>Ejemplo de respuestas a la entrevista</h3>
  <table class="tg">
  <thead>
    <tr>
      <th class="tg-c3ow">Pregunta</th>
      <th class="tg-c3ow">Ejemplo de respuesta</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="tg-c3ow">¿Qué es un componente en Angular? </td>
      <td class="tg-c3ow"> ... </td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es una directiva en Angular? </td>
      <td class="tg-c3ow">Una directiva es una instrucción que modifica el DOM</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es un servicio en Angular? </td>
      <td class="tg-c3ow"> ... </td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es un módulo en Angular? </td>
      <td class="tg-c3ow"> Es una clase que sirve para organizar la aplicación ordendando la en bloques </td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es el patrón redux en Angular?  </td>
      <td class="tg-c3ow"> ... </td>
    </tr>    
    <tr>
      <td class="tg-c3ow">¿Cuál es la diferencia entre ng-container y ng-template en Angular? </td>
      <td class="tg-c3ow"> ... </td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Diferencia entre clase abstracta y una interfaz? </td>
      <td class="tg-c3ow">Son lo mismo</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Cómo se ordena una colección de objetos en java? </td>
      <td class="tg-c3ow">Hay que desarrollar un codigo con un comparando cada objeto</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es la Interfaz Map? </td>
      <td class="tg-c3ow"> ... </td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es la Interfaz Set? </td>
      <td class="tg-c3ow">En Java Set representa a un conjunto, es decir que es como una lista, pero sin repetidos</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es la Interfaz List? </td>
      <td class="tg-c3ow">En Java List es una lista simplemente enlazada que permite repetidos</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué es el patrón singleton?</td>
      <td class="tg-c3ow">Es el patrón de los solteros</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Comó implementaría el patrón Singleton?</td>
      <td class="tg-c3ow">Buscaria ayuda de un amigo</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Qué entendes por el patrón de diseño Strategy? </td>
      <td class="tg-c3ow">El patron Strategy es un patrón de diseño que permite definir una estrategia a diferentes objetos y que luego cuando se los invoque, el objeto haga lo que se definió en la estrategia</td>
    </tr>
    <tr>
      <td class="tg-c3ow">¿Para qué sirve un pom.xml y qué relación tiene con Maven? </td>
      <td class="tg-c3ow">Un pom.xml sirve para identificar dependencias y plugins. Maven resuelve las dependencias definidas en el pom.</td>
    </tr>
  </tbody>
  </table>
</div>

Su modelo de relevancia debe tener al menos **50 _queries_** entrenadas, cada uno con un documento marcado como mínimo con uno relevante o no relevante, para que pueda ser entrenado. Hemos proporcionado algunos ejemplos de _queries_ para comenzar el entrenamiento (tenga en cuenta que algunas frases de respuestas no están relacionadas con ninguno de los documentos, para estos, todas las sugerencias deben marcarse como no relevantes y no cuentan entre los 50 minimos)

> Recomendación: Entrenar primero los 50 _queries_ relacionados a los documentos y despues adicionar con frases no relacionadas al tema si asi lo considera ;)


## 4. Envío

Para realizar el envío, primero debe acceder a la siguiente aplicación: https://Empresa XYZ.maratona.dev/ y completar el formulario con las credenciales de su instancia de **Watson Discovery** y los **IDs** de su colección. En esta página podrá probar su modelo antes de enviarlo.

🚨 **PRUEBA TU SOLUCIÓN ANTES DE PRESENTARLA** 🚨

Después de realizar las pruebas, haga clic en el botón en la esquina inferior derecha para ENVIAR su solución, como se muestra en la imagen a continuación, y complete el formulario con su dirección de correo electrónico utilizada para la inscripción en MARATONA 2020.

Credenciales:
<img align='center' src="./doc/source/images/Empresa XYZ_CREDS.png" alt="submissão"></img>
Enviar:
<img align='center' src="./doc/source/images/Empresa XYZ_SEND.png" alt="submissão"></img>


## 5. Sobre la evaluación

Nuestro sistema de evaluación automática realizará consultas para su modelo y analizará si las respuestas obtenidas son consistentes con los documentos esperados. Los documentos de su solución **deben** contener las claves con los nombres especificados aquí, `body`, `title`, `url`, con sus respectivos valores, para que la validación sea exitosa.

La rapidez de entrega no se incluye en el cálculo de la puntuación del desafío. Sin embargo, para todos los participantes que presenten este desafío en la primera semana después del lanzamiento, recibirán una bonificación del 10% de la puntuación final.

Recuerde que tiene 3 oportunidades de envío de la solución del reto donde se le tomará en cuenta el envío que obtenga mejor puntuación.

## Material de apoyo

- [Watson Discovery Docs](https://cloud.ibm.com/docs/discovery?topic=discovery-about)

## Solución de problemas

Mira el [video explicativo](#31-tecnología) provisto en la Sección 3, o si lo deseas, revisa la documentación de los servicios involucrados en este desafío

> Situación común: El reentrenamiento del modelo de relevancia puede durar un largo tiempo en reactivarse.
> Situación común: Si presenta algún error en el entrenamiento de relevacia, corrija los errores que le sugiere la erramienta. El sistema comenzará a entrenar despúes de un tiempo largo.


Accede al discord oficial de la Maratón 2020 para hacer preguntas y/o interactuar con otros participantes: [Discord](https://discord.gg/Q9At74C).

## Licencia

Copyright 2020 Maratona Behind the Code

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
