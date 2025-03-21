/***********************************************************
/***********************************************************
File:Group-Project-FILE Authors:
Trinidy Boyce & Brooklyn Eskew
Version 1.0 Date: 3/4/2025
Resources:
**********************************************************/
#include <stdio.h>
#include <time.h>
#include <stdlib.h>
int randone() {
    return (rand() % 7+ 1);
}
int randtwo() {
    return (rand() % 7+ 1);
}
int randthree() {
    return (rand() % 7+ 1);
}
int randfour() {
    return (rand() % 7+ 1);
}
int main() {
    srand(time(NULL));
    int q = randone();
    int w = randtwo();
    int e = randthree();
    int r = randfour();
    int answer;
	int choice1;
	printf("Your one a Vacation! Which Destinations Do You Choose\n");
	printf("1. Hawaii\n2. Africa\n3. Italy\n4. Brazil\n");
	printf("Enter Coorisponding Number:");
	do {
		scanf ("%d", &choice1);
		printf("\n");
		if (choice1==1) {
			printf("You bought your plane ticket and your on your way to beautiful Hawaii!\n");
		}

		else if (choice1==2) {
			printf("You bought your plane ticket and your on your way to beautiful Africa!\n");
		}
		else if (choice1==3) {
			printf("You bought your plane ticket and your on your way to beautiful Italy!\n");
		}
		else if (choice1==4) {
			printf("You bought your plane ticket and your on your way to beautiful Brazil!\n");
		}
		else {
			printf("ERROR! Please Choose Choice 1-4: ");
		}
	} while ((choice1>4)||(choice1<1));

	printf("While on the way to your desitnation the plane begins to have extreme terbulance!\n");
	printf("The pilot comes on the intercome and says the plane has lost both engines! BRACE FOR IMPACT!!!\n");
	printf("You duck down and brace for impact!\n");
	do {
		printf("\n");
		if (choice1==1) {
			printf("Your Plane crashes and you are stranded on small island in the middle of the ocean!\n\n");
		}
		else if (choice1==2) {
			printf("Your Plane crashes and you are stranded on in the middle of the Sahara Desert!\n\n");
		}
		else if (choice1==3) {
			printf("Your Plane crashes and you are stranded in the Alps!\n\n");
		}
		else if (choice1==4) {
			printf("Your Plane crashes and you are stranded in the middle of the Amazon Rainforest!\n\n");
		}
		else {
			printf("ERROR! Please Choose Choice 1-4: ");
		}
	} while ((choice1>4)||(choice1<1));

	printf("You Stumbed outside of the plane disorented... you got some minor cuts and bruises.\n");
	printf("You look behind you and there is no one else coming out of the plane...\n");
	printf("After sitting for a while you are faced with some decisions to make...\n\n");

	int choice2;
	char ans;
	printf("What do you do first?\n\n1. Explore the plane wreckage and find supplies.\n");
	printf("2. Explore the area and travel away from the plane.\n3. Search the plane for survivors.\n");
	printf("Choose the coorisponding number:");
	do {
		scanf ("%d", &choice2);
		printf("\n");
		if (choice2==1) {
			int choice3;
			printf("You chose to search the plane for suppilies\n");
			printf("\n");
			if (choice2==1) {
				int choice3;
				printf("You chose to search the plane for suppilies\n");
				printf("You have 4 areas of the plane to search.\n");
				printf("Where are you searching first?\n\n1.Cockpit\n2.FirstClass\n3.MainCabin\n4.Flight Attendant Area\n");
				printf("Choose the coorsponding number:");
				do {
					scanf("%d",&choice3);
					printf("\n");
					if (choice3==1) {
						printf("You chose to search the cockpit. You find A compass and an emergency transmitter.\n\n");
					}
					else if (choice3==2) {
						printf("You chose to search first class. Here you search the luggage and seats and find:\n\n");
						printf("You find %d drinks, %d alcohol, %d small dinners",q,w,e);
						printf("%d pillows and blankets, A lighter, A life vest, and a swiss army tool\n",r);
					}
					else if (choice3==3) {
						printf("You chose to search main class. Here you search the luggage and seats and find:\n\n");
						printf("You find %d extra clothes,%d snacks,%d medication,",q,w,r);
						printf("a small pocketknife, and a flashlight");
					}
					else if (choice3==4) {
						printf("You chose to search Flight Attendant Area. Here you search the luggage and seats and find:\n\n");
						printf("You find %d granola bars, %d soda pop, %d waters,",r,e,w);
						printf("a first aid kit, and a emergency axe.");
					}
					else {
						printf("ERROR! Please Choose Choice 1-4: ");
					}
				} while ((choice3>4)||(choice3<1));
			}
		}
		else if (choice2==2) {
		    char ans;
			printf("You decide to search the area and you wander to far from the plane!\n");
			printf("You ARE LOST!!!!");
			printf("You have a sense of where the plane. Do you turn back?\n");
			printf("Choose y for yes and n for no:");
			do {
		     scanf("%c", &ans); 
			if (ans =='y') {
			    printf("You return to the plane");
			}
			else if (ans =='n') {
			    printf("You slowly die for lack of supplies. GAME OVER!");
			}
			else {
			    printf("ERROR! Please Choose Choice y for yes and n for no: ");
			}
			} while ((ans=!'y')||(ans=!'n'));
		}
		else if (choice2==3) {
			printf("You go back into the plane and look for survivors. However all you find is empty seats and bodies.");
			printf("No one else survived, you are alone\n");
		}
		else {
			printf("ERROR! Please Choose Choice 1-3: ");
		}
	} while ((choice2>3)||(choice2<1));

	
	return 0;
}
