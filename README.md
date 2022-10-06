# PROYECTO-FINAL

El codigo esta estructurado en cuatro archivos

    0- Presentacion
    1- Extraccion Resultados
    2- Prediccion Inicial
    3- Prediccion Maher
    4- Prediccion Dixon-Coles
    
0- PRESENTACION: (ARCHIVO A IGNORAR)

    - Archivo con unicamente los resultados y datos que se muestran en la presentacion.
    
1- EXTRACCION RESULTADOS:

    - Carga y limpieza de los datos que voy a querer analizar mas adelante. Fuente mencionada en el mismo codigo
    - Consigo una tabla con todos los resultados de las ultimas 30 temporadas de la liga española disputadas.
    - TEMPORADA / DIVISION / FECHA DEL PARTIDO / LOCAL / VISITANTE / GL / GV / RESULTADO
    
2- PREDICCION INICIAL

    - Basandonos en las temporadas 17-18, 18-19, 19-20, 20-21 intentamos predecir los resultados de la temporada 21-22
    - Analisis general de las 4 temporadas previas disputadas
    - Relacion entre el historico y la distribucion de Poisson
    - Definicion de parametros de ataque y defensa tanto en campo local como en campo visitante
    - Creacion modelo de prediccion y ejecucion para tratar de adivinar los resultados de la temporada 21/22
    - Comparacion de los datos obtenidos por el modelo con los resultados reales
    - FIABILIDAD: 50,53%         69,52 % derrotas/victorias acertadas      4,4 % empates acertados
    
3- PREDICCION MAHER

    - Maher trata de corregir el modelo de Poisson mediante un modelo de Poison Bivariante en el cual tiene en cuenta que las fuerzas de ataque y defensa de un equipo varian en funcion del rival con el que se enfrenten
    - Basandonos en las temporadas 17-18, 18-19, 19-20, 20-21 intentamos predecir los resultados de la temporada 21-22
    - Definicion de las funciones de la verosimilitud y sumatorio de estas
    - Maximicacion de los parametros FAL, FAV, FDL, FDV
    - Creacion modelo de prediccion y ejecucion para tratar de adivinar los resultados de la temporada 21/22
    - Comparacion de los datos obtenidos por el modelo con los resultados reales
    - FIABILIDAD: 50,53%         71,00 % derrotas/victorias acertadas      0,9 % empates acertados
    
4- PREDICCION DIXON-COLES

    - Maher trata de corregir el modelo de Maher en el cual se da cuenta de que los resultados bajos estan subestimados y en particular los empates muy subestimados
    - Basandonos en las temporadas 17-18, 18-19, 19-20, 20-21 intentamos predecir los resultados de la temporada 21-22
    - Definicion de las funciones de la correccion de rho, la verosimilitud y sumatorio de estas
    - Maximicacion de los parametros FAL, FAV, FDL, FDV
    - Creacion modelo de prediccion y ejecucion para tratar de adivinar los resultados de la temporada 21/22
    - Comparacion de los datos obtenidos por el modelo con los resultados reales
    - FIABILIDAD: 50,53%         71,00 % derrotas/victorias acertadas      0,9 % empates acertados  
    
COMENTARIOS:
    - Curioso como no mejora la fiabilidad del modelo, sin embargo si que varian las probabilidades de cada resultado.
    - Me queda pendiente mucho por hacer, como pulir estos modelos, probar el numero de temporadas previas optimo para una buena prediccion de resultados y la implementacion de la correccion que tambien hace Dixon Coles sobre el peso de cada resultado en funcion de la fecha de este, teniendo los resultados mas recientes mas relevancia en el modelo.
    - Seguimos IronHackers! 
