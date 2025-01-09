# JS-Chapter8
JavaScript Chapter 8 Programming Assignment

In this project you will create objects to describe the contents of a pizza and the contents of a shopping cart. Each pizza is described by its size, crust, and list of toppings. An interface that allows customers to build their pizza by selecting items from a web form has been created for you. Your job will be to write the object code to work with this interface, storing data about the pizzas the customers build. A preview of the completed project is shown in Figure 8-36.

![image](https://github.com/user-attachments/assets/ecf56e05-93ba-458f-a8c8-7600123893ed)

Figure 8-36

Do the following:

Use your code editor to open the index.html and script.js files. Enter your name and the date in the comment section of each file and commit.

Go to the index.html file in your code editor and link the page to the script.js file, deferring the script until after the page loads. Take some time to study the contents and structure of the web from which customers will make their selections. Close the file, saving your changes.

Return to the script.js file in your code editor. Directly below the Object Code comment create an object literal named cart. The cart object has a single property named items containing an empty array and a single method named addItem(foodItem) Add the command this.items.push(foodItem) to this method.

Create a constructor function for the Pizza object class containing a size and crust property with no initial values and a toppings property containing an empty array.

Create a constructor function for the Topping object class containing the name and side property to store the name of the topping and whether covers the entire pizza or is limited to the pizza’s left or right side. Do not enter initial values for these properties.

Add the addToCart(cart) method to the Pizza prototype. Within the method run the command cart.items.push(this) to add the pizza to the items array of a shopping cart.

Add the summarize() method to the Pizza prototype to create a text string summarizing the content of the pizza. Within the function do the following:

Declare a variable named summary with the initial value “Pizza: “.

Add the value of this.size and this.crust to the value of summary. Separate the size and crust values with a blank space.

Create a for loop that iterates through the this.toppings array. For each item in the array add the text string name (side) to the summary variable, where name is the value of the this.toppings[i].name property and side is the value of the this.toppings[i].side property.

After the for loop, return the value of the summary variable.

Scroll down to the buildPizza() function. This function builds a pizza object based on selections made on the web form. Add the following code to the function.

Create an instance of a Pizza object storing it in myPizza.

Set the value of myPizza.size to pizzaSizeBox.value. Set the value of myPizza.crust to pizzaCrustBox.value.

Add the selected toppings to the pizza by creating a for loop that iterates through the contents of the checkedToppings node list. Within the loop,

create an instance of a Topping object named myTopping;

set myTopping.name equal to checkedToppings[i].name and myTopping.side equal to checkedToppings[i]value;

apply the addTopping(myTopping) method to myPizza.

After the for loop, return the value of myPizza.

Go to the updateCart() function, which adds the pizza to the shopping cart. Add the following commands to the function:

Run the buildPizza() function, storing the result in the myPizza variable.

Apply the addItem(myPizza) method to the cart object.

Run the console.log(cart) method to write the contents of the cart object to the debugger console.

Create a paragraph element containing the value of summarize(myPizza). Use the appendChild() method to append the paragraph to the cartBox element.

Reset the page for the next pizza by running the clearPizzaImage() function followed by the clearToppings() function.

Commit your changes to the file and then load index.html in your browser. Verify that you can build a pizza and add it to the shopping cart by clicking controls on the web form. Verify that the debugger console lists all of the pizzas added to the cart object.
