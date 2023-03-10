![Shark](https://i.pinimg.com/564x/3b/d3/8b/3bd38b1e5023bd66096faa2f777d8de6.jpg)

# PROYECTO DE LIMPIEZA DE DATOS -> SHARKS馃馃馃

El objeto del presente proyecto es la utilizaci贸n e interiorizaci贸n de determinadas t茅cnicas y metodolog铆as de limpieza de datos. Para ello me he servido del *dataset* [Global Shark Attacks](https://www.kaggle.com/datasets/teajay/global-shark-attacks?resource=download) el cual contiene registros de ataques de tiburones a personas en todo el mundo. 


## OBJETIVOS DEL PROYECTO
1. Crear un repositorio en GitHub con una buena organizaci贸n de los recursos.
2. Aplicar herramientas, t茅cnicas y metodolog铆as para la limpieza de datos:
    - Exploraci贸n del conjunto de los datos
    - Limpieza de valores nulos
    - Toma de decisiones
    - Correcci贸n de valores erroneos
    - Obtenci贸n de consistencia en los datos
    - Transformaci贸n del tipo de dato para la optimizaci贸n de memoria
    - Librer铆as utilizadas: Pandas, Numpy, regex, pylab y seaborn
3. Aplicar restricciones para la limpieza:
    - No se pueden eliminar columnas
    - No pueden quedar menos de 1500 filas
4. Analizar descriptivamente el conjunto de datos para determinar el perfil de la v铆ctima de ataque de tibur贸n.

## AN脕LISIS DE LOS DATOS
### Exploraci贸n general
Nos encontramos con un *dataset* muy heterogeneo, con un gran porcentaje de valores nulos o en su defecto, informaci贸n poco consistente o con valores 0, tal y como se muestra en el gr谩fico, siendo la parte coloreada de amarillo la correspondiente a los valores nulos.  
  
  
![Graphic](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/gr%C3%A1fico.png)

### Limpieza de valores nulos
Hay muchos registros con todos o casi todos sus valores nulos por lo que directamente los eliminamos. Tambi茅n se considera eliminar los registros con m谩s del 75% de sus valores nulos o 0.  
  
A partir de este momento, exploramos columna a columna intentando completar los valores nulos restantes. En su mayor铆a se desconoce el dato. Sin embargo hay otras columnas que guardan cierta relaci贸n como puedan ser 'Injury' (tipo de lesi贸n) la cual usaremos para intentar determinar si la victima muri贸 o sobrevivi贸 en la columna 'Fatal (Y/N)'. Tambi茅n pudimos completar los valores de la columna 'Year', a partir de la columna 'Date'.  
### Limpieza de valores erroneos
En este momento hemos limpiado nuestro *DataFrame* de valores nulos pero en su mayor铆a siguen siendo inconsistentes y de poca utilidad, ya sea por su ambig眉edad o por su formato.  
  
Ejemplo de mal formato es la columna 'Date', la cual intentamos redefinir. En la columna 'Case Number' decido numerarla de manera ordenada ya que la informaci贸n que proporciona se repite identicamente en 3 columnas m谩s.  
  
As铆 mismo, se llevan acabo procesos de limpieza en la como 'Country' en la cual sus valores se encontraban dispersos. Trato de acumularlos para su mejor manejo.  
En la columna 'Sex' ocurre algo similar a 'Country' por lo que sigo un proceso similar.  
  
La columna 'Species' es probablemente la m谩s dispersa de todas y para m铆 es de las que m谩s valor tienen, ya que me interesa saber cual es la especie m谩s involucrada en los ataques. Intento encontrar un patr贸n para sacar cosas en claro.
### Transformaci贸n del tipo de dato
Aunque nuestro *DataFrame* no es tan extenso como para ocupar mucho espacio, siempre viene bien transformar los datos que se puedan para optimizar el uso de memoria.

## CONCLUSIONES
El perfil de la v铆ctima de ataque de tibur贸n es el siguiente:  

  - Hombre  

![Sex](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Sex.png)  
  
  
  - 27 a帽os de edad  
  
![Age](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Age.png)
  
  
  - Estadounidense  
  
![Country](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Country.png)  


  - Surfeando  
  
![Activity](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Activity.png)  


  - En oto帽o  
  
![Season](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Season.png)  


  - Atacado por un tibur贸n blanco  
  
![Specie](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Specie.png)  


  - Sobrevivi贸 al ataque  
  
![Fatality](https://github.com/Periclates7/Data_cleaning_project/blob/main/img/Fatal.png)

