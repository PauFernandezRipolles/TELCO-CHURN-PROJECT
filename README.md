# TELCO-CHURN-PROJECT

A partir de un único archivo CSV de KAGGLE, sobre la rotación de clientes de una empresa de telefonía, realizo la transformación, modelado y análisis de los datos para formular y responder preguntas relevantes que permitan sacar conclusiones útiles sobre como afrontar el problema del CHURN, el principal caballo de batalla de las Telco.
* En un primer paso utilizo MySQL para visualizar los datos, obtener una primera visión de conjunto de los mismos y comprovar su integridad y coheréncia.
* Tras ellos utilizo POWER BI para hacer las transformaciones necesarias y normalizar el modelo, separando la información en varias tablas y relacionandolas entre si creando un modelo coherente, práctico y sin redundáncias.

![image](https://github.com/user-attachments/assets/1263e5b1-d86a-4d7d-993e-57cfe41c8791)


En este caso no se trata de un modelo típico en estrella o copo de nieve con relaciones varios a uno de partida. Tomando los indicadores del Churn como eje vertebrador y, por tanto, como tabla de hechos principal y objetivo del análisis, organizo las otras tablas (Cuenta, Servicios, Facturación, Demografia y Satisfacción del cliente) alrededor de la tabla Churn. Todas se relacionan con Churn a través de ID de Cliente que presenta solo valores únicos en la tabla Churn. Solo la tabla de lugares es una tabla de dimensiones propiamente dicha que se relaciona con Demografia. 

Para una mayor coheréncia del modelo, modifico la cardinalidad de las relaciones de Churn a las de "dimensiones" a varios a uno. También opto por crear un ID de Churn con la idea de que, en el futuro, se puedan añadir datos de posibles churn parciales (si un cliente se lleva una linea pero no toda la cuenta), incluir clientes que retornan después de churn o añadir los datos de los clientes nuevos para tener los datos de captación netos. Así la relación de Churn con las otras tablas sería de manera natural de varios a uno. 

Se trata por tanto de un modelo atípico que representó un reto e implicó una buena comprensión del contexto y del negocio para organizar los datos de manera coherente y eficiente.

* Realizo un primer análisis y busco las preguntas relevantes para preparar y organizar el análisis en profundidad.

* Organizo el análisis en 5 dashboards:
  * Churn Motivation: ¿Que motiva a los clientes a cambiar?
  * Demographics: ¿Qué tipologia de clientes se quedan y cuales se van?
  * Billing: ¿Qué gastos realizan los clientes que se quedan y los que se van?
  * Account: ¿Qué tipo de cuentas tienen?
  * Services: ¿Qué servicios contratan?
    
* Para empezar a responder a estas preguntas empiezo a realizar medidas y a crear columnas calculadas con DAX:
  * Calculo la tasa de Churn:
    
    ![image](https://github.com/user-attachments/assets/51949780-1fbb-432f-b0a8-dfbf2072233c)


  * Creo un Scoring de clientes en función de la cantidad y calidad de los servicios contratados:
 
    ![image](https://github.com/user-attachments/assets/62b482e8-2473-4277-82c2-89651059ff76)

    
    ![image](https://github.com/user-attachments/assets/737e188b-cd40-48c2-9ed3-0bd058ba7e73)

  * Calculo la tasa de clientes Premium en función del scoring:
    
    ![image](https://github.com/user-attachments/assets/2b9b58f0-f837-4afa-94f3-a620a58ceb01)
    
    ![image](https://github.com/user-attachments/assets/5699557b-ecd1-4092-90d1-c6a908facbb3)


Hasta aquí lo realizado hasta el momento del proyecto, a continuación los próximos pasos:
   
* Realizar los dashboards, con sus correspondientes visualizaciones, en POWER BI para exponer los datos relevantes y resolver las preguntas importantes.

![image](https://github.com/user-attachments/assets/768379be-ce7a-4a43-abaf-eb67bdf760fe)


![image](https://github.com/user-attachments/assets/f876d97f-d49b-495a-8a51-9dbb325ad0e3)


![image](https://github.com/user-attachments/assets/8779a53d-13b3-4372-a2b3-9c029c4f5572)




* Organizarlos en un informe de fácil navegación y usabilidad.
* Realizar una presentacion en video en POWER POINT para contar, de una manera concisa, coherente y que mueva a la acción, qué nos cuentan estos datos sobre el CHURN y como realizar acciones concretas para abordar este problema. 
