# TELCO-CHURN-PROJECT

A partir de un único archivo CSV de KAGGLE, sobre la rotación de clientes de una empresa de telefonía, realizo la transformación, modelado y análisis de los datos para formular y responder preguntas relevantes que permitan sacar conclusiones útiles sobre como afrontar el problema del CHURN, el principal caballo de batalla de las Telco.
* En un primer paso utilizo MySQL para visualizar los datos, obtener una primera visión de conjunto de los mismos y comprovar su integridad y coheréncia.
* Tras ellos utilizo POWER BI para hacer las transformaciones necesarias y normalizar el modelo, separando la información en varias tablas y relacionandolas entre si creando un modelo coherente, práctico y sin redundáncias.

  ![image](https://github.com/user-attachments/assets/6229c050-744d-456d-b688-5cfd455c92fd)

En este caso no se trata de un modelo típico en estrella o copo de nieve con relaciones varios a uno. Partiendo de los indicadores del Churn como eje vertebrador y, por tanto, como tabla de hechos principal y objetivo del análisis, organizo las otras tablas (Cuenta, Servicios, Facturación, Demografia, Facturación y Satisfacción del cliente) alrededor del Churn. Solo la tabla de lugares es una tabla de dimensiones propiamente dicha que se relaciona con Demografia. 
Se trata por tanto de un modelo atípico que representó un reto e implico una buena comprensión del contexto y del negocio para organizar los datos de manera coherente y eficiente.

* Realizo un primer análisis y busco las preguntas relevantes para preparar y organizar el análisis en profundidad.

* Organizo el análisis en 4 dashboards:
  * Customer: ¿Qué tipologia de clientes se quedan y cuales se van?
  * Billing: ¿Qué gastos realizan los clientes que se quedan y los que se van?
  * Account: ¿Qué tipo de cuentas tienen?
  * Services: ¿Qué servicios contratan?
* Para empezar a responder a estas preguntas empiezo a realizar medidas y a crear columnas calculadas con DAX:
  * Calculo la tasa de Churn:
  * 
  * Creo un Scoring de clientes en función de la cantidad y calidad de los servicios contratados:
  * 
  * Calculo la tasa de clientes Premium:
    ![image](https://github.com/user-attachments/assets/f492ac10-c077-42f8-bbb0-70593f683c9b)

    ![image](https://github.com/user-attachments/assets/2b9b58f0-f837-4afa-94f3-a620a58ceb01)

Hasta aquí lo realizado hasta el momento del proyecto, a continuación los próximos pasos:
   
* Realizar los dashboards, con sus correspondientes visualizaciones, en POWER BI para exponer los datos relevantes y resolver las preguntas importantes.
* Organizarlos en un informe de fácil navegación y usabilidad.
* Realizar una presentacion en video en POWER POINT para contar, de una manera concisa, coherente y que mueva a la acción, qué nos cuentan estos datos sobre el CHURN y como realizar acciones concretas para abordar este problema. 
