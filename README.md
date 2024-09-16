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
    
    ![image](https://github.com/user-attachments/assets/644b45f7-e063-4e8c-ab2f-2a5e47d03cbe)

    ![image](https://github.com/user-attachments/assets/51949780-1fbb-432f-b0a8-dfbf2072233c)

  * Creo un Scoring de clientes en función de la cantidad y calidad de los servicios contratados:
 
    ![image](https://github.com/user-attachments/assets/16485cd1-7b23-4b6d-a2ad-a323f95e3494)
 
    ![image](https://github.com/user-attachments/assets/5d752d1b-9d4c-4775-ba00-f890ace913b0)
 
    ![image](https://github.com/user-attachments/assets/2f9729a7-442d-4a32-9eee-bf8ebc546a15)



 
    ![image](https://github.com/user-attachments/assets/62b482e8-2473-4277-82c2-89651059ff76)

    ![image](https://github.com/user-attachments/assets/737e188b-cd40-48c2-9ed3-0bd058ba7e73)

  * Calculo la tasa de clientes Premium en función del scoring:
 
    ![image](https://github.com/user-attachments/assets/1c385c69-42f2-4228-9d9c-d0a4a7fdd4c5)

    
    ![image](https://github.com/user-attachments/assets/2b9b58f0-f837-4afa-94f3-a620a58ceb01)
    
    ![image](https://github.com/user-attachments/assets/5699557b-ecd1-4092-90d1-c6a908facbb3)
    
  * Creo una columna calculada para categorizar "monthly charge" para facilitar el análisis de "billing" respecto al churn rate.

    ![image](https://github.com/user-attachments/assets/466d2068-9e86-46b4-9951-e4b6d4804bc6)

    
  * Hago lo mismo con las columnas de cargos por consumo de datos (dividiendo antes el total cobrado por los meses de contrato) y por consumo de llamadas internacionales.

    ![image](https://github.com/user-attachments/assets/98fb0d69-dc7e-4f9b-827e-32ef34d934d6)
    
    ![image](https://github.com/user-attachments/assets/372943b3-6d5a-4b01-bcd2-4e8607f0d00f)

    ![image](https://github.com/user-attachments/assets/add2ad8b-8e56-4284-925b-9d0ed02fa508)


  * Realizo varias medidas para calcular el churn rate promedio de los clientes que tienen un determinado servicio activo.

    ![image](https://github.com/user-attachments/assets/0324738c-a0bd-439a-8a1d-e6252fffc657)

   
* Realizo los dashboards, con sus correspondientes visualizaciones, en POWER BI para exponer los datos relevantes y resolver las preguntas importantes.

* Organizo los dashboards en un informe de fácil navegación y usabilidad.
  

    ![image](https://github.com/user-attachments/assets/03eb8901-748b-4367-819a-05682b74831d)


    ![image](https://github.com/user-attachments/assets/5f36960b-ac10-422a-af47-9af40bfd135d)


    ![image](https://github.com/user-attachments/assets/5f8bc2cc-5f20-4514-af7f-593788bdbcc2)


    ![image](https://github.com/user-attachments/assets/36e9dd78-7a02-4c44-93e0-8dffd3c730cf)


    ![image](https://github.com/user-attachments/assets/f37f500b-2ee0-44cf-b90d-2845aece66c7)


    ![image](https://github.com/user-attachments/assets/cc900e2f-1fcf-4257-9d61-d515d7ee4dbe)


    ![image](https://github.com/user-attachments/assets/e3238e8d-5088-4fc8-8dce-d98969575154)


* Realizo una presentacion en video en POWER POINT para contar, de una manera concisa, coherente y que mueva a la acción, qué nos cuentan estos datos sobre el CHURN y como    realizar acciones concretas para abordar este problema. 
