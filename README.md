
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */

package com.mycompany.number1coffee;

/**
 *
 * @author Mc Donald
 */

public class Number1Coffee {

    public static void main(String[] args) {

        // Single Dimensional Arrays
        String[] cities = {"Cape Town", "Port Elizabeth", "Pretoria"};
        String[] drinks = {"Coffee", "Tea", "Boba Tea"};

        // Two Dimensional Array (City and Drink Sales)
        // Row 0 = Cape Town
        // Row 1 = Port Elizabeth
        // Row 2 = Pretoria

        int[][] sales = {
            {500, 300, 125}, // Cape Town
            {450, 250, 100}, // Port Elizabeth
            {480, 175, 120}  // Pretoria
        };

        // Report Header
        System.out.println("Number 1 Coffee Hut Application");
        System.out.println("---------------------------------------------------------------");

        // Display column headings
        System.out.printf("%-18s %-10s %-10s %-10s %-10s%n",
                "City", drinks[0], drinks[1], drinks[2], "Total");

        System.out.println("---------------------------------------------------------------");

        int grandTotal = 0;

        // Loop through cities
        for (int i = 0; i < cities.length; i++) {

            int cityTotal = 0;

            // Calculate total sales for each city
            for (int j = 0; j < sales[i].length; j++) {
                cityTotal += sales[i][j];
            }

            // Add city total to grand total
            grandTotal += cityTotal;

            // Display city sales and total
            System.out.printf("%-18s %-10d %-10d %-10d %-10d%n",
                    cities[i],
                    sales[i][0],
                    sales[i][1],
                    sales[i][2],
                    cityTotal);
        }

        System.out.println("---------------------------------------------------------------");

        // Display grand total
        System.out.printf("%-18s %-10s %-10s %-10s %-10d%n",
                "Grand Total", "", "", "", grandTotal);

        System.out.println("---------------------------------------------------------------");
    }
}
