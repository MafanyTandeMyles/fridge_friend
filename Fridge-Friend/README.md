# Pervasive Fridge Friend Final Project Report


## Project goal: describes the purpose of this project 
My app's purpose is to help users organize and easily visualize their groceries, by using a UPC supplied database. Users will be able to barcode scan their groceries as they unpack them, adding them to their current list with a single button press. Tags such as expiration date and food type are automatically added, so users can easily sort their grocery list by what to eat (or throw away) next.

## Project features: abstract from the user stories 
* Scan barcodes from camera
* Fetch barcode UPC info using COmputer Vision API
* Store UPC Items in a database
* Sort UPC Items by food category or expiration date



## File structure: what does each file do and who wrote that file
* UI Files: 
 * Activity_Main: homepage with photo button
 * Activity_Results: Results screen after barcode scan; shows product name and info, with Add button
 * content_main: 
 * drawer_list_item: 
 * list_item: individual xml for each list item
 
* Java Files:
 * DBHelper:  Creates the SQLite Database for storing food items by UPC type including expiry date, type of food, name, etc.
 * ItemType:  associates common words in UPC item name with appropriate food category, defines item typing
 * MainActivity: Displays the homepage with current items in database, along with button to add new via photo
 * NetworkUtilis:  Handles network operations of looking up barcodes
 * Results_Activity:  Looks up barcode scan and retrieves UPC Item with description & photo, adds to the database
 * UpcItem:  Defines a UPC Item including name, item type, and shelf life, to be added to database
 * UpcItemLoader: Asyncronously loads UPCItem in background
 
