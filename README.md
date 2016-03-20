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

int new_list(char str[], array mas)
{
    int j=0; // кількість лексем у рядку
    char *del="., "; // покажчик на розділові символи
    char *p; // покажчик на поточну лексему
    cout<<"New string:"<<endl;
    p=strtok(m,del); //визначити першу лексему
    cout << p << " ";
    while (p!=NULL) //поки є рядку є лексеми
    { strcpy(mas[j],p); //копіювати поточну лексему в масив
    p=strtok(NULL,del); //продовжити пошук лексем
    if (j%2 != 0)
    cout << p << " "; //вивести поточну лексему на екран
    j++; //перейти до наступної лексеми
    }
    return j;
}


