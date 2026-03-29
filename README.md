# calculadora-en-c
calculadora en c, Distintas funciones y valores, Basica y variada
#include<stdio.h>
#include<stdlib.h>
#include<math.h>
void ejecutarOpcionSuma();
void ejecutarOpcionResta();
void ejecutarOpcionMultiplicacion();
void ejecutarOpcionDivision();
void ejecutarOpcionRaizCuadrada();
void ejecutarOpcionPotencia();
void mostrarMenu();

int main()
{
    //declaración de variables//
    short opcionSeleccionada;


    do{
            //el do while sirve para que el menú se ejecute al menos una vez y continue...
    // ...repitiendose siempre que la condición de opcionSeleccionada sea distinta de cero//
    mostrarMenu();
//seleccion del menú//
    printf("\n\nSeleccione una opcion para continuar:");
    scanf("%d",&opcionSeleccionada);
//ejecución de las opciones//
    switch(opcionSeleccionada)
    {
        case 1:
            //El case llama a la opción suma y busca el void correspondiente//
            ejecutarOpcionSuma();
            break;
            //el break no deja que entre en los demas cases, y el contenido del void se destruye//
        case 2:
            ejecutarOpcionResta();
            break;
        case 3:
            ejecutarOpcionMultiplicacion();
            break;
        case 4:
            ejecutarOpcionDivision();
            break;
        case 5:
            ejecutarOpcionRaizCuadrada();
            break;
        case 6:
            ejecutarOpcionPotencia();
            break;
    }
    }while(opcionSeleccionada!=0);

return (0);
}

void mostrarMenu()
{
    //menú principal//
    printf("\n\n----CALCULADORA----\n");
    printf("\n1- SUMA");
    printf("\n2- RESTA");
    printf("\n3- MULTIPLICACION");
    printf("\n4- DIVISION");
    printf("\n5- RAIZ CUADRADA");
    printf("\n6- POTENCIA");
    printf("\n0- SALIR");
}

void ejecutarOpcionSuma()
{
    float numero1;
    float numero2;
    float resu;
            printf("\n---SUMA---:");
            printf("\nIngrese el primer numero:");
            scanf("%f",&numero1);
            printf("\nIngrese el segundo numero:");
            scanf("%f",&numero2);
            resu= numero1+numero2;
            printf("\nLa suma es: %2.f", resu);

}

void ejecutarOpcionResta()
{
    float numero1;
    float numero2;
    float resu;
            printf("\n---RESTA---:");
            printf("\nIngrese el primer numero:");
            scanf("%f",&numero1);
            printf("\nIngrese el segundo numero:");
            scanf("%f",&numero2);
            resu= numero1-numero2;
            printf("\nLa resta es: %2.f", resu);
}

void ejecutarOpcionMultiplicacion()
{
    float numero1;
    float numero2;
    float resu;
            printf("\n---MULTIPLICACION---:");
            printf("\nIngrese el primer numero:");
            scanf("%f",&numero1);
            printf("\nIngrese el segundo numero:");
            scanf("%f",&numero2);
            resu= numero1*numero2;
            printf("\nEl resultado es: %2.f", resu);
}

void ejecutarOpcionDivision()
{
    float numero1;
    float numero2;
    float resu;
            printf("\n---DIVISION---:");
            printf("\nIngrese el primer numero:");
            scanf("%f",&numero1);
            printf("\nIngrese el segundo numero:");
            scanf("%f",&numero2);
            if(numero2!=0)
                {resu= numero1/numero2;
                 printf("\n%2.f divido %2.f es: %2.f", numero1,numero2,resu);
                 }else
                 {
                     printf("\n---No se puede dividir por cero---");
                 }
}

void ejecutarOpcionRaizCuadrada()
{
    float numero1;
    float numero2;
    float resu;
            printf("\n---RAIZ CUADRADA---:");
            printf("\nIngrese el numero:");
            scanf("%f",&numero1);
            if(numero1>=0)
            {
                resu=sqrt(numero1);
                printf("\nLa raiz es: %2.f",resu);
            }else
            {
                printf("\nNo se puede realizar la raiz de un numero negativo:");
            }
}

void ejecutarOpcionPotencia()
{
    float numero1;
    float numero2;
    float resu;
            printf("\n---POTENCIA---:");
            printf("\nIngrese la base:");
            scanf("%f",&numero1);
            printf("\nIngrese el exponente:");
            scanf("%f",&numero2);
            resu=pow(numero1,numero2);
            printf("\nLa potencia es: %2.f",resu);
}
