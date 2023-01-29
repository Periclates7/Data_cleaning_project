![Shark](https://i.pinimg.com/564x/3b/d3/8b/3bd38b1e5023bd66096faa2f777d8de6.jpg)

# PROYECTO DE LIMPIEZA DE DATOS -> SHARKS🦈🦈🦈

El objeto del presente proyecto es la utilización e interiorización de determinadas técnicas y metodologías de limpieza de datos. Para ello me he servido del *dataset* "Global Shark Attacks" el cual contiene registros de ataques de tiburones a personas en todo el mundo. 
Link del dataset: https://www.kaggle.com/datasets/teajay/global-shark-attacks?resource=download

## OBJETIVOS DEL PROYECTO
1. Crear un repositorio en GitHub con una buena organización de los recursos.
2. Aplicar herramientas, técnicas y metodologías para la limpieza de datos:
    - Exploración del conjunto de los datos
    - Limpieza de valores nulos
    - Toma de decisiones
    - Corrección de valores erroneos
    - Obtención de consistencia en los datos
    - Transformación del tipo de dato para la optimización de memoria
    - Librerías utilizadas: Pandas, Numpy, regex, pylab y seaborn
3. Aplicar restricciones para la limpieza:
    - No se pueden eliminar columnas
    - No pueden quedar menos de 1500 filas
4. Analizar descriptivamente el conjunto de datos para determinar el perfil de la víctima de ataque de tiburón.

## ANÁLISIS DE LOS DATOS
### Exploración general
Nos encontramos con un *dataset* muy heterogeneo, con un gran porcentaje de valores nulos o en su defecto, información poco consistente o con valores 0, tal y como se muestra en el gráfico, siendo la parte coloreada de amarillo la correspondiente a los valores nulos.  
  
  
![Graphic](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/gr%C3%A1fico.png)

### Limpieza de valores nulos
Hay muchos registros con todos o casi todos sus valores nulos por lo que directamente los eliminamos. También se considera eliminar los registros con más del 75% de sus valores nulos o 0.  
  
A partir de este momento, exploramos columna a columna intentando completar los valores nulos restantes. En su mayoría se desconoce el dato. Sin embargo hay otras columnas que guardan cierta relación como puedan ser 'Injury' (tipo de lesión) la cual usaremos para intentar determinar si la victima murió o sobrevivió en la columna 'Fatal (Y/N)'. También pudimos completar los valores de la columna 'Year', a partir de la columna 'Date'.  
### Limpieza de valores erroneos
En este momento hemos limpiado nuestro *DataFrame* de valores nulos pero en su mayoría siguen siendo inconsistentes y de poca utilidad, ya sea por su ambigüedad o por su formato.  
  
Ejemplo de mal formato es la columna 'Date', la cual intentamos redefinir. En la columna 'Case Number' decido numerarla de manera ordenada ya que la información que proporciona se repite identicamente en 3 columnas más.  
  
Así mismo, se llevan acabo procesos de limpieza en la como 'Country' en la cual sus valores se encontraban dispersos. Trato de acumularlos para su mejor manejo.  
En la columna 'Sex' ocurre algo similar a 'Country' por lo que sigo un proceso similar.  
  
La columna 'Species' es probablemente la más dispersa de todas y para mí es de las que más valor tienen, ya que me interesa saber cual es la especie más involucrada en los ataques. Intento encontrar un patrón para sacar cosas en claro.
### Transformación del tipo de dato
Aunque nuestro *DataFrame* no es tan extenso como para ocupar mucho espacio, siempre viene bien transformar los datos que se puedan para optimizar el uso de memoria.

## CONCLUSIONES
El perfil de la víctima de ataque de tiburón es el siguiente:  

  - Hombre  

![Sex](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Sex.png)  
  
  
  - 27 años de edad  
  
![Age](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Age.png)
  
  
  - Estadounidense  
  
![Country](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Country.png)  


  - Surfeando  
  
![Activity](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Activity.png)  


  - En otoño  
  
![Season](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Season.png)  


  - Atacado por un tiburón blanco  
  
![Specie](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Specie.png)  


  - Sobrevivió al ataque  
  
![Fatality](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Fatal.png)

