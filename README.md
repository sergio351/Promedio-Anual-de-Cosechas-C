# Promedio-Anual-de-Cosechas-C
Tarea: Los dueños de un campo desean informatizar los informes sobre sus cosechas. Creen necesario disponer de un programa que permita almacenar en un arreglo unidimensional del tipo real las toneladas mensuales de cereales cosechadas durante el año 2019 en un campo. El programa tiene que emitir los siguientes informes a) El promedio anual de toneladas cosechadas b) ¿Cuántos meses tuvieron una cosecha superior al promedio anual? c) ¿En que mes o meses (mostrar NOMBRE DEL MES) se produjo el mayor número de toneladas? ¿Cuántas fueron? Usted ha sido seleccionado para crear un programa en lenguaje C que contemple lo solicitado por los dueños del campo, contamos con sus habilidades de programador para que realice un programa completo y eficiente.
#include <stdio.h>
#include <stdlib.h>
#define max 12
int main()
{
    int i,j,cantmes=0,mes,b[max],cantmayores=0;
    float v[max],suma=0,promedio,mayor=0;

    printf("ingrese cosecha mes: \n");
    for (i=0;i<max;i++)
    {
        switch (i)
        {
            case 0:
                printf("Enero: ");
                scanf("%f",&v[i]);
            break;

            case 1:
                printf("Febrero: ");
                scanf("%f",&v[i]);
            break;

            case 2:
                printf("Marzo: ");
                scanf("%f",&v[i]);
            break;

            case 3:
                printf("Abril: ");
                scanf("%f",&v[i]);
            break;

            case 4:
                printf("Mayo: ");
                scanf("%f",&v[i]);
            break;

            case 5:
                printf("Junio: ");
                scanf("%f",&v[i]);
            break;

            case 6:
                printf("Julio: ");
                scanf("%f",&v[i]);
            break;

            case 7:
                printf("Agosto: ");
                scanf("%f",&v[i]);
            break;

            case 8:
                printf("Septiembre: ");
                scanf("%f",&v[i]);
            break;

            case 9:
                printf("Octubre: ");
                scanf("%f",&v[i]);
            break;

            case 10:
                printf("Noviembre: ");
                scanf("%f",&v[i]);
            break;

            case 11:
                printf("Diciembre: ");
                scanf("%f",&v[i]);
            break;

            default: printf("error");

        }
    }


for (i=0;i<max;i++)
{
    suma+=v[i];

}

promedio=suma/max;

for (i=0;i<max;i++)
{

    if (v[i]>promedio)
    {
        cantmes++;
    }

}

for (i=0;i<max;i++)
{
    if (v[i]>mayor)
    {
        mayor=v[i];

    }
}

j=0;
for (i=0;i<max;i++)
{
    if(v[i]==mayor)
    {
        b[j]=i;
        j++;
        cantmayores++;
    }
}
printf("\n");
printf("promedio anual de cosechas: %.2f\n",promedio);
printf("cantidad de meses mayores al promedio: %d\n",cantmes);
printf("mayor numero es %.2f: \n",mayor);
printf("total de mejores meses %d\n",cantmayores);
printf("mejor(es) mes(es): ");

 for (i=0;i<j;i++)
    {

        switch (b[i])
        {
            case 0:
                printf("Enero ");

            break;

            case 1:
                printf("Febrero ");

            break;

            case 2:
                printf("Marzo ");

            break;

            case 3:
                printf("Abril ");

            break;

            case 4:
                printf("Mayo ");

            break;

            case 5:
                printf("Junio ");

            break;

            case 6:
                printf("Julio ");

            break;

            case 7:
                printf("Agosto ");

            break;

            case 8:
                printf("Septiembre ");

            break;

            case 9:
                printf("Octubre ");

            break;

            case 10:
                printf("Noviembre ");

            break;

            case 11:
                printf("Diciembre ");

            break;

            default: ;

        }
    }
}
