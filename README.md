# Shopping-Cart
Used a Tree Map data structure to store information of individual orders. 

This project uses a Map interface that references a TreeMap instance in order to build a shopping cart program. Two files are given, an orders file that tells what items are in each person’s cart, and an items file that lists products being sold with its price. These two files are inputted through the command line when the program is running, and will be scanned through the Scanner class. The information is then stored into the TreeMap accordingly. The product names are the keys that maps to its price, and the shopper’s name is the key to an ArrayList that stores their carted products. The output displays all the activities that are given in the orders file, such as adding and deleting items from the cart, displaying all the items in their cart, and calculating the total cost of their purchases.

For this program, I had to use java’s ArrayList, TreeMap, Scanner, and Map interface. Furthermore, a constructor, ShoppingCart(String itemsFile, String orderFile), accepts the two files String arguments that are passed from the main method. The constructor instantiates the Scanner class and scans both files, and stores the information to the corresponding TreeMap. In the constructor, a switch statement is implemented to call methods according to the action words in the orders file: add, delete, cart, checkout. Depending on the word, the switch statement will call either the add() method, delete() method, cart() method, or checkout() method.

When the add()method is called, the shopper’s name and the item name is passed into the parameters. There are certain conditions that must be checked before the item can be successfully added into the cart. If the shopper doesn’t have a cart, then a new cart, in the form of an ArrayList, is instantiated and then the item is added to the cart. If the item already exists in the cart, then the item is not added. The method ends by storing the shopper’s name and it’s Arraylist back into the TreeMap.

When the delete() method is called, the shopper’s name is then passed into the argument in order to map to the appropriate ArrayList, in which the product information are stored. Conditions must also be met in order for the items to be deleted successfully. The first condition is that if the shopper does not have an existing cart, then an Exception will be caught and prints that the cart does not exist. Next, the item is checked if it exists in the cart. If it doesn’t exist, then a printed message says that the item does not exist. Otherwise, the item is then removed fro the ArrayList.
The cart() method accepts the shopper’s name as the key to locate the corresponding ArrayList. This method then uses an enhanced for loop to print out all the items stored in that ArrayList. The checkout() method does the same thing, except it also takes the item name as a key and maps it to the price. An enhanced for loop is used to print out the item name, price, and it calculates the total amount due.

I tested the program out by adding various actions to the orders file, such as delete an item that actually exists in the person’s cart, or to delete an item that a cart does not exists. Also, I kept adding an item to a person’s cart and have the cart list the items each time to ensure that the add method works. What I learned from this project was how to implement a TreeMap and understand how a TreeMap actually works. Also, this project trained me to use the Java API library more efficiently because acknowledge how well Java documented all their codes.
