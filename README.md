#include <iostream>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>

using namespace std;

char m[100]; // вихідний рядок
const int n=20;
typedef char array[n][n];
array arr; // масив слів

int new_list(char [], array); // визначення переліку і кількості слів

int main()
{
    int i; // кількість слів у рядку
    puts("enter string:");
    gets(m); //ввести рядок
    i=new_list(m,arr);
    system("pause");
}


