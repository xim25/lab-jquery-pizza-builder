![](https://i.imgur.com/1QgrNNw.png)

# JS | Pizza Builder

## Introduction

![](http://i.giphy.com/e2AKpOvx2MREY.gif)

We've got the munchies for a nice, fresh pie of pizza. Of course, we want to order online. After all, talking to a person will only delay the consumption of pizza.

There's only one problem: our local pizzeria's pizza builder **isn't working**. This time, the local pizzeria is in luck because their customer today is a Web developer. We always hear about how developers should give back to their community. I can't think of a more meaningful contribution than helping the community get pizza more easily.

## Requirements

- [Fork this repo](https://guides.github.com/activities/forking/)
- Clone this repo into your `~/code/labs`
- Follow the instructions above to complete the exercise

## Submission

- Upon completion, run the following commands
	```
	git add .
	git commit -m "done"
	git push origin master
	```
- Navigate to your repo and [create a Pull Request](https://help.github.com/articles/creating-a-pull-request/)

## Instructions

Taking a look at the pizza builder you can see that we will work with the `pizza.js` file, that right now it's empty. Let's help the pizzeria out by writing the pizza builder's JavaScript.

### Iteration 1: Add and remove toppings

There are five buttons on the left of the pizza builder. Three of those have to add or remove toppings from the pizza. Write the JavaScript necessary for those three buttons to **add and remove pepperonni, mushrooms and green peppers** from the pizza. **Don't worry about updating the price**. We will do it later.

Each individual topping has its own HTML element:

```htmlmixed=56
<section class="green-pepper one"></section>
<section class="green-pepper two"></section>
```

```htmlmixed=78
<section class="mushroom one">
  <div class="cap">1</div>
  <div class="stem"></div>
</section>
```

```htmlmixed=238
<section class="pep one">1</section>
<section class="pep two">2</section>
```

**Create the code to display those elements when the buttons are clicked.**

### Iteration 2: Sauce and crust options

Wait a minute... this pizza comes with white sauce and gluten-free crust by default! Since that is a ridiculous default setting, we need to fix this as fast as possible. The last two buttons on the left are supposed to handle special options for the sauce and crust of your pizza. Make it so **regular sauce** and **crust** are selected **by default**. Also write the JavaScript code that will let users **select white sauce** and **gluten free crust** if they want to choose them. Again, **don't worry about updating the price**.

Both the crust and the sauce have their own HTML elements:

```htmlmixed=271
<section class="crust crust-gluten-free">
  <section class="cheese"></section>
  <section class="sauce sauce-white"></section>
</section>
```

**As you can see, the sections have two classes `.crust-gluten-free` and `sauce-white` that may not be the best choice.**

### Iteration 3: Change the buttons' state

Currently our pizza builder's buttons look the same, no matter if the option is activateed or not. If you notice, all the buttons have an `active` class.

```htmlmixed=20
<button class="btn btn-pepperonni active">Pepperonni</button>
```

**Write some JavaScript that will remove and add the buttons' `active` class appropriately**. This is, if the ingredient is turned on, its button should have `active`. If the ingredient is off, remove the `active` class from the button.

**Also make sure that the buttons' initial state matches that of their ingredient**. If when you first load the pizza builder there is no pepperonni, the pepperonni button should not be active.

### Iteration 4: Update price

On the right side of the pizza builder there is a price section. It should show the current price of your pizza, but it's always stuck on **$21**, which is the price if all the ingredients were on:

```htmlmixed=39
<aside class="panel price">
```

```htmlmixed=50
<strong>$21</strong>
```

**Write the JavaScript that update the current price of the pizza as a user clicks the ingredient buttons to turn ingredients on and off. How can you keep track of the current price? When an ingredient changes, how will you know how much to add or substract?**

Don't worry about the individual price items in above the total. First update the total price and worry about those later.

### Iteration 5: Update ingredient itemization

Now that the price is updating we should also update the itemization of the ingredients that make up the total price. It's always showing all of the ingredients, as if they were all turned on.

```htmlmixed=43
<ul>
  <li>$1 pepperonni</li>
  <li>$1 mushrooms</li>
  <li>$1 green peppers</li>
  <li>$3 white sauce</li>
  <li>$5 gluten-free crust</li>
</ul>
```

**Use JavaScript to hide and show the price items as they are turned on and off. When an ingredient is on, the user should see the price of the item. When an ingredient is off, the price item should be hidden.**

For example, if the user has selected only **white sauce** and **green peppers**, they should see:

```
$10 cheese pizza
  + $1 green peppers
  + $3 white sauce
$14
```

When an ingredient changes, how will you know which element to hide?
