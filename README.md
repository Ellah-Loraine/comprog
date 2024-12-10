#include <stdio.h>
#include <string.h>
#include <stdlib.h>  
#include <time.h>

int main() {
    int choice, foodChoice, quantity, dineChoice;
    float total = 0;
    char items[100][50];
    int quantities[100];
    float prices[100];
    int cartSize = 0;

    // Seed the random number generator
    srand(time(0));

    printf("----- Welcome to Foodie Companion!! -----\n");

    while (1) {
        printf("\nSelect a food category:\n");
        printf("1. Mexican Foods\n");
        printf("2. Filipino Foods\n");
        printf("3. Italian Foods\n");
        printf("4. Korean Foods\n");
        printf("5. Dessert\n");
        printf("6. Drinks\n");
        printf("7. Checkout\n");
        printf("\nEnter the number of your choice: ");
        scanf("%d", &choice);

        if (choice == 7) {  // For checkout
            break;
        }

        char itemName[50];
        float itemPrice = 0;

        switch (choice) {
            case 1:
                printf("\nMexican Foods Menu:\n");
                printf("1. Beef Empanada - ₱65.00\n");
                printf("2. Nachos Supreme - ₱155.00\n");
                printf("3. Trout Tacos - ₱695.50\n");
                printf("4. Chicken Chalupas - ₱320.78\n");
                printf("5. Churros - ₱344.60\n");
                printf("6. Sopapillas - ₱135.43\n");
                printf("\nEnter the number of your choice: ");
                scanf("%d", &foodChoice);

                if (foodChoice == 1) {
                    strcpy(itemName, "Beef Empanada");
                    itemPrice = 65.00;
                } else if (foodChoice == 2) {
                    strcpy(itemName, "Nachos Supreme");
                    itemPrice = 155.00;
                } else if (foodChoice == 3) {
                    strcpy(itemName, "Trout Tacos");
                    itemPrice = 695.50;
                } else if (foodChoice == 4) {
                    strcpy(itemName, "Chicken Chalupas");
                    itemPrice = 320.78;
                } else if (foodChoice == 5) {
                    strcpy(itemName, "Churros");
                    itemPrice = 344.60;
                } else if (foodChoice == 6) {
                    strcpy(itemName, "Sopapillas");
                    itemPrice = 135.43;
                } else {
                    printf("Invalid choice.\n");
                    continue;
                }
                break;

            case 2:
                printf("\nFilipino Foods Menu:\n");
                printf("1. Adobo - ₱110.00\n");
                printf("2. Sinigang - ₱120.00\n");
                printf("3. Lechon Kawali - ₱250.00\n");
                printf("4. Lumpia - ₱150.00\n");
                printf("5. Sizzling Sisig - ₱270.00\n");
                printf("6. Kare-Kare - ₱290.00\n");
                printf("\nEnter the number of your choice: ");
                scanf("%d", &foodChoice);

                if (foodChoice == 1) {
                    strcpy(itemName, "Adobo");
                    itemPrice = 110.00;
                } else if (foodChoice == 2) {
                    strcpy(itemName, "Sinigang");
                    itemPrice = 120.00;
                } else if (foodChoice == 3) {
                    strcpy(itemName, "Lechon Kawali");
                    itemPrice = 250.00;
                } else if (foodChoice == 4) {
                    strcpy(itemName, "Lumpia");
                    itemPrice = 150.00;
                } else if (foodChoice == 5) {
                    strcpy(itemName, "Sizzling Sisig");
                    itemPrice = 270.00;
                } else if (foodChoice == 6) {
                    strcpy(itemName, "Kare-Kare");
                    itemPrice = 290.00;
                } else {
                    printf("Invalid choice.\n");
                    continue;
                }
                break;

            case 3:
                printf("\nItalian Foods Menu:\n");
                printf("1. Alfredo Pasta - ₱157.99\n");
                printf("2. Spaghetti - ₱258.49\n");
                printf("3. Pesto Pasta - ₱257.49\n");
                printf("4. Lasagna - ₱250.00\n");
                printf("5. Pizza Margherita - ₱357.69\n");
                printf("6. Gnocchi with Pesto Sauce - ₱310.00\n");
                printf("\nEnter the number of your choice: ");
                scanf("%d", &foodChoice);

                if (foodChoice == 1) {
                    strcpy(itemName, "Alfredo Pasta");
                    itemPrice = 157.99;
                } else if (foodChoice == 2) {
                    strcpy(itemName, "Spaghetti");
                    itemPrice = 2.49;
                } else if (foodChoice == 3) {
                    strcpy(itemName, "Pesto Pasta");
                    itemPrice = 257.49;
                } else if (foodChoice == 4) {
                    strcpy(itemName, "Lasagna");
                    itemPrice = 250.00;
                } else if (foodChoice == 5) {
                    strcpy(itemName, "Pizza Margherita");
                    itemPrice = 357.59;
                } else if (foodChoice == 6) {
                    strcpy(itemName, "Gnocchi with Pesto Sauce");
                    itemPrice = 310.00;
                } else {
                    printf("Invalid choice.\n");
                    continue;
                }
                break;

            case 4:
                printf("\nKorean Foods Menu:\n");
                printf("1. Kimchi - ₱80.00\n");
                printf("2. Bulgogi - ₱250.00\n");
                printf("3. Tteokbokki - ₱170.00\n");
                printf("4. Bibimbap - ₱180.00\n");
                printf("5. Kimchi Jjigae (Kimchi Stew) - ₱258.70\n");
                printf("6. Japchae (Stir-Fried Glass Noodles) - ₱320.00\n");
                printf("\nEnter the number of your choice: ");
                scanf("%d", &foodChoice);

                if (foodChoice == 1) {
                    strcpy(itemName, "Kimchi");
                    itemPrice = 80.00;
                } else if (foodChoice == 2) {
                    strcpy(itemName, "Bulgogi");
                    itemPrice = 250.00;
                } else if (foodChoice == 3) {
                    strcpy(itemName, "Tteokbokki");
                    itemPrice = 170.00;
                } else if (foodChoice == 4) {
                    strcpy(itemName, "Bibimbap");
                    itemPrice = 180.00;
                } else if (foodChoice == 5) {
                    strcpy(itemName, "Kimchi Jjigae (Kimchi Stew)");
                    itemPrice = 258.70;
                } else if (foodChoice == 6) {
                    strcpy(itemName, "Japchae (Stir-Fried Glass Noodles");
                    itemPrice = 320.00;
                } else {
                    printf("Invalid choice.\n");
                    continue;
                }
                break;

            case 5:
                printf("\nDessert Menu:\n");
                printf("1. Ice Cream - ₱83.49\n");
                printf("2. Cake - ₱124.99\n");
                printf("3. Brownie - ₱49.99\n");
                printf("4. Halo-Halo - ₱123.59\n");
                printf("5. Leche Flan - ₱180.00\n");
                printf("6. Ube Cheesecake - ₱173.99\n");
                printf("\nEnter the number of your choice: ");
                scanf("%d", &foodChoice);

                if (foodChoice == 1) {
                    strcpy(itemName, "Ice Cream");
                    itemPrice = 83.49;
                } else if (foodChoice == 2) {
                    strcpy(itemName, "Cake");
                    itemPrice = 124.99;
                } else if (foodChoice == 3) {
                    strcpy(itemName, "Brownie");
                    itemPrice = 49.99;
                } else if (foodChoice == 4) {
                    strcpy(itemName, "Halo-Halo");
                    itemPrice = 123.59;
                } else if (foodChoice == 5) {
                    strcpy(itemName, "Leche Flan");
                    itemPrice = 180.00;
                } else if (foodChoice == 6) {
                    strcpy(itemName, "Ube Cheesecake");
                    itemPrice = 173.99;
                } else {
                    printf("Invalid choice.\n");
                    continue;
                }
                break;

            case 6:
                printf("\nDrinks Menu:\n");
                printf("1. Soda - ₱30.99\n");
                printf("2. Cooconut Juice - ₱142.49\n");
                printf("3. Calamansi Juice - ₱110.99\n");
                printf("4. Gulaman - ₱120.49\n");
                printf("5. Iced Coffee - ₱210.60\n");
                printf("6. Water - ₱10.99\n");
                printf("\nEnter the number of your choice: ");
                scanf("%d", &foodChoice);

                if (foodChoice == 1) {
                    strcpy(itemName, "Soda");
                    itemPrice = 30.99;
                } else if (foodChoice == 2) {
                    strcpy(itemName, "Coconut Juice");
                    itemPrice = 142.49;
                } else if (foodChoice == 3) {
                    strcpy(itemName, "Calamansi Juice");
                    itemPrice = 110.99;
                } else if (foodChoice == 4) {
                    strcpy(itemName, "Gulaman");
                    itemPrice = 120.49;
                } else if (foodChoice == 5) {
                    strcpy(itemName, "Iced Coffee");
                    itemPrice = 210.60;
                } else if (foodChoice == 6) {
                    strcpy(itemName, "Water");
                    itemPrice = 10.99;
                } else {
                    printf("Invalid choice.\n");
                    continue;
                }
                break;

            default:
                printf("Invalid category choice.\n");
                continue;
        }

        // Ask for quantity
        printf("\nEnter quantity: ");
        if (scanf("%d", &quantity) != 1 || quantity <= 0) {
            printf("Invalid quantity. Try again.\n");
            continue;
        }

        // Add to cart
        int found = 0;
        for (int i = 0; i < cartSize; i++) {
            if (strcmp(items[i], itemName) == 0) {
                quantities[i] += quantity;
                found = 1;
                break;
            }
        }
        if (!found) {
            strcpy(items[cartSize], itemName);
            quantities[cartSize] = quantity;
            prices[cartSize] = itemPrice;
            cartSize++;
        }

        total += itemPrice * quantity;

        // Ask for Dine-In or Take-Out
        printf("\nDine-In or Take-Out?\n");
        printf("1. Dine-In\n");
        printf("2. Take-Out\n");
        printf("\nEnter the number of your choice: ");
        scanf("%d", &dineChoice);

        if (dineChoice == 1) {
            printf("\nOrder noted for Dine-In.\n");
        } else if (dineChoice == 2) {
            printf("\nOrder noted for Take-Out.\n");
        } else {
            printf("\nInvalid choice. Defaulting to Take-Out.\n");
        }
    }

    // Checkout
    printf("\n----- Receipt -----\n");
    if (total > 0) {
        for (int i = 0; i < cartSize; i++) {
            printf("%s (x%d) - ₱%.2f\n", items[i], quantities[i], prices[i] * quantities[i]);
        }
        
        // Apply 12% VAT and service charge
        float vat = total * 0.12;
        float serviceCharge = total * 0.10;
        float finalTotal = total + vat + serviceCharge;

        printf("\nSubtotal: ₱%.2f\n", total);
        printf("\nVAT (12%%): ₱%.2f\n", vat);
        printf("\nService Charge (10%%): ₱%.2f\n", serviceCharge);
        printf("\nTotal Amount: ₱%.2f\n", finalTotal);

        // Generate and display priority number
        int priorityNumber = rand() % 100 + 1; // Random number between 1 and 100
        printf("\nYour priority number: %d\n", priorityNumber);
        printf("Please wait for the cashier to call your number.\n");
    } else {
        printf("You did not purchase anything.\n");
    }

    printf("\n\n\nThank you for ordering!! Enjoy!!\n");

    return 0;
}
