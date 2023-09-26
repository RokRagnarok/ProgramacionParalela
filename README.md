# ProgramacionParalela
## Se realizo un codigo para hacer una multiplicacion de matrices de 10x10 en el lenguaje de C.
###Definicion de Matrices
Las matrices son un conjunto bidimensional de números o símbolos distribuidos de forma rectangular, en líneas verticales y horizontales, de manera que sus elementos se organizan en filas y columnas. Sirven para describir sistemas de ecuaciones lineales o diferenciales, así como para representar una aplicación lineal.
#Multiplicacion de Matrices
La multiplicación de matrices consiste en combinar linealmente dos o más matrices mediante la adición de sus elementos dependiendo de su situación dentro de la matriz origen respetando el orden de los factores.
#Codigo
#include <stdio.h>
int main()
{
  int mat1[10][10];
    int mat2[10][10];
    int mat3[10][10];

     //Dar valores a mat1,2,3
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            mat1[i][j] = i * 10 + j;  
        }
    }
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            mat2[i][j] = j * 10 + i;  
        }
    }
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            mat3[i][j] = 0;
        }
    }

    //Funcion para multiplicar matricees
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            for (int k = 0; k < 10; k++) {
                mat3[i][j] += mat1[i][k] * mat2[k][j];
            }
        }
    }
    
    //Imprime el resultado de la matriz
    printf("Resultado de la matriz 10 X 10:\n");
    for (int i = 0; i < 10; i++) {
        for (int j = 0; j < 10; j++) {
            printf("%d ", mat3[i][j]);
        }
        printf("\n");
    }

    return 0;
}

#Proceso para Multiplicar
Verifica que el número de filas de la primera matriz es igual al número de columnas de la segunda matriz.
De la primera matriz: toma una fila i
De la segunda matriz: toma una columna j
Multiplica cada un elemento de cada fila y de cada columna, en orden.
Coloca el resultado en la posición ( ﻿i , ﻿j) en la matriz resultante.
Regresa al paso 2, hasta terminar con toda la matriz. :)

#Aplicacion de la multiplicacion de matrices
La multiplicación de matrices es muy útil para la resolución de sistemas de ecuaciones de muchas variables, dado que son muy cómodas para ser implementadas mediante un computador. 

#Analisis de Complejidad Temporal
Se crearon 3 variables con el tamaño de 10 dentro de un arreglo
se crearon 6 for para darles valores especificos alas variables mat1, mat 2 y mat 3
Se creo un septimo for para multiplicar los valores de las tres matrices con I,J y K
por ultimo se creo un printf para mostrar en pantalla el resultado de la multiplicacion de la matriz junto con dos for mas
y dentro de estos un printf que muestra el resultado de la variable mat3


