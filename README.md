/***********************************************************
 File:Group-Project-FILE Authors:
 Trinidy Boyce & Brooklyn Eskew
 Version 1.0 Date: 3/4/2025
 Resources:
 **********************************************************/
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int randone() {
     return (rand() % 7+ 1);
 }
 int randtwo() {
     return (rand() % 5+ 1);
 }
 int randthree() {
     return (rand() % 4+ 1);
 }
 int randfour() {
     return (rand() % 3+ 1);
 }
int main() {
	srand(time(NULL));  // Seed random number generator
     int q = randone();
     int w = randtwo();
     int e = randthree();
     int r = randfour();
     int answer;
	int choice1;

	printf("You're on a vacation! Which destination do you choose?\n");
	printf("1. Hawaii\n2. Africa\n3. Italy\n4. Brazil\n");
	printf("Enter the corresponding number: ");

	do {
		scanf("%d", &choice1);
		printf("\n");
		if (choice1 == 1) {
			printf("You bought your plane ticket and you're on your way to beautiful Hawaii!\n");
		} else if (choice1 == 2) {
			printf("You bought your plane ticket and you're on your way to beautiful Africa!\n");
		} else if (choice1 == 3) {
			printf("You bought your plane ticket and you're on your way to beautiful Italy!\n");
		} else if (choice1 == 4) {
			printf("You bought your plane ticket and you're on your way to beautiful Brazil!\n");
		} else {
			printf("ERROR! Please choose a number between 1 and 4: ");
		}
	} while (choice1 < 1 || choice1 > 4);

	printf("While on the way to your destination, the plane experiences extreme turbulence!\n");
	printf("The pilot comes on the intercom and says the plane has lost both engines! BRACE FOR IMPACT!!!\n");
	printf("You duck down and brace for impact!\n\n");

	if (choice1 == 1) {
		printf("Your plane crashes, and you are stranded on a small island in the middle of the ocean!\n\n");
	} else if (choice1 == 2) {
		printf("Your plane crashes, and you are stranded in the middle of the Sahara Desert!\n\n");
	} else if (choice1 == 3) {
		printf("Your plane crashes, and you are stranded in the Alps!\n\n");
	} else if (choice1 == 4) {
		printf("Your plane crashes, and you are stranded in the middle of the Amazon Rainforest!\n\n");
	}

	printf("You stumble outside of the plane, disoriented... you have some minor cuts and bruises.\n");
	printf("You look behind you, but no one else is coming out of the plane...\n");
	printf("After sitting for a while, you are faced with some decisions to make...\n\n");

	int choice2;
	char ans;

	do {
		printf("What do you do first?\n");
		printf("1. Explore the plane wreckage and find supplies.\n");
		printf("2. Explore the area and travel away from the plane.\n");
		printf("3. Search the plane for survivors.\n");
		printf("Choose the corresponding number: ");

		do {
			scanf("%d", &choice2);
			printf("\n");

			if (choice2 == 1) {
				int choice3;
				printf("You chose to search the plane for supplies.\n");
				printf("You have 4 areas of the plane to search.\n");
				printf("Where do you search first?\n");
				printf("1. Cockpit\n2. First Class\n3. Main Cabin\n4. Flight Attendant Area\n");
				printf("Choose the corresponding number: ");

				do {
					scanf("%d", &choice3);
					printf("\n");
					if (choice3 == 1) {
						printf("You chose to search the cockpit. You find a compass and an emergency transmitter.\n\n");
					} else if (choice3 == 2) {
						printf("You chose to search first class. You find:\n");
						printf("%d drinks, %d bottles of alcohol, %d small dinners, %d pillows and blankets, a lighter, a life vest, and a Swiss army tool.\n\n",q,w,e,r);
					} else if (choice3 == 3) {
						printf("You chose to search the main cabin. You find:\n");
						printf("%d extra clothes, %d snacks, %d medications, a small pocketknife, and a flashlight.\n\n",r,q,w);
					} else if (choice3 == 4) {
						printf("You chose to search the Flight Attendant Area. You find:\n");
						printf("%d granola bars, %d soda cans, %d water bottles, a first aid kit, and an emergency axe.\n\n",q,w,e);
					} else {
						printf("ERROR! Please choose a number between 1 and 4: ");
					}
				} while (choice3 < 1 || choice3 > 4);
			}

			else if (choice2 == 2) {
				printf("You decide to search the area and wander too far from the plane!\n");
				printf("You ARE LOST!!!!\n");
				printf("You have a sense of where the plane is. Do you turn back? (y/n): ");

				do {
					scanf(" %c", &ans);
					if (ans == 'y') {
						printf("You return to the plane.\n");
					} else if (ans == 'n') {
						printf("You slowly die from lack of supplies. GAME OVER!\n");
					} else {
						printf("ERROR! Please choose 'y' for yes or 'n' for no: ");
					}
				} while (ans != 'y' && ans != 'n');
			}

			else if (choice2 == 3) {
				printf("You go back into the plane and look for survivors. However, all you find are empty seats and bodies.\n");
				printf("No one else survived, you are alone.\n");
				printf("You return to the plane.\n");
			}

			else {
				printf("ERROR! Please choose a number between 1 and 3: ");
			}
		} while (choice2 < 1 || choice2 > 3);
	} while (ans == 'y');
	return 0;
}
