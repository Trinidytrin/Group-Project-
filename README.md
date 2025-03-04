/***********************************************************
File:Group-Project-FILE
Authors: Trinidy Boyce & Brooklyn Eskew
Version 1.0
Date: 3/4/2025
Resources: 
**********************************************************/
#include <stdio.h>
#include <time.h>
#include <stdlib.h>
//int generaterandnumb(){//


int main(){
  int choice1;
  printf("Your one a Vacation! Which Destinations Do You Choose\n");
  printf( "1. Hawaii\n 2. Africa\n 3. Italy\n 4. Brazil\n); 
  printf("Enter Coorisponding Number:"); 
  scanf ("%d", &choice1);
  do {
    if (choice1==1){
      printf("You bought your plane ticket and your on your way to beautiful Hawaii!");
    }
    
    if (choice1==2){
      printf("You bought your plane ticket and your on your way to beautiful Africa!");
    }
    if (choice1==3){
      printf("You bought your plane ticket and your on your way to beautiful Italy!");
    }
    if (choice1==4){
    printf("You bought your plane ticket and your on your way to beautiful Brazil!");
    else (choice1>4){
      printf("ERROR! Please Choose Choice 1-4");
    }
    }
  }
    while (choice1>4);
    return 0;
  }
