---
layout: post
toc: true
breadcrumb: true
title: Variables and Classes Homework
description: Homework problems for variables and classes in JavaScript
permalink: /student/hacks/varclasses-hw
author: Yiming Yin
date: 2025-10-09
categories: [javascript, homework]
tags: [variables, classes, coding]
type: hacks
---

## **Variables and Classes**

### <u>Popcorn Hack 1 - Variables</u>

A short program about variables. Complete the TODO sections to finish the program.

```javascript
// Step 1: Make some variables
let name = "Yiming";
let age = 15;

// Step 2: Print a message
console.log("Hi, my name is", name);
console.log("I am", age, "years old.");

// Step 3: Unfinished part
// TODO: Make a new variable called "nextYearAge"
// that is the age plus 1
let nextYearAge = age + 1;

// TODO: Print out the result
// Example: "Next year I will be 11 years old."
console.log("Next year I will be", nextYearAge, "years old!");
```

### <u>Popcorn Hack 2 - Classes</u>

A short program about classes using an Animal zoo example.

```javascript
// Step 1: Define the Animal class
class Animal {
  // Initialize each animal with a name, sound, and type
  constructor(name, sound, kind) {
    this.name = name;
    this.sound = sound;
    this.kind = kind;
  }

  // Make the animal speak
  speak() {
    console.log(`${this.name} the ${this.kind} says ${this.sound}!`);
  }

  // Bonus method: describe the animal
  describe() {
    console.log(`${this.name} is a ${this.kind} and is not friendly to strangers.`);
  }
}

// Step 2: Create a list to hold all the animals in the zoo
let zoo = [];

// Step 3: Add animals to the zoo
// TODO: Create at least 3 animals and push them into the zoo array
// Example:
zoo.push(new Animal("Giraffe", "Hum", "Herbivore"));
zoo.push(new Animal("Mittens", "Meow", "Cat"));
zoo.push(new Animal("Eagle", "whistle sound", "Bird")); //these are mine, thanks for the example.
zoo.push(new Animal("Golden Lab", "Woof", "Dog"));
zoo.push(new Animal("Tiger", "Roar", "Big Cat"));

// Step 4: Loop through all animals and make them speak
// TODO: Use a for loop (or forEach) to call speak() on each animal
zoo.forEach(animal => {
  animal.speak();
  // Step 5: Optional bonus: Call describe() too
  animal.describe();
});

// Step 5 Bonus: Let the user add a new animal (works in browser)
// Uncomment if running in browser with prompt()
// let name = prompt("Enter the animal's name:");
// let sound = prompt("Enter the sound it makes:");
// let kind = prompt("Enter the kind of animal:");
// let newAnimal = new Animal(name, sound, kind);
// zoo.push(newAnimal);
// newAnimal.speak();
// newAnimal.describe();
```

### <u>Homework - Rock Paper Scissors Game</u>

Complete the rock, paper, scissors game implementation.

```javascript
// Step 1: Make a list of choices
const choices = ["rock", "paper", "scissors"];

// Step 2: Ask the user for their choice (VS Code version without prompt)
// Since prompt() doesn't work in VS Code notebooks, we'll simulate user choice
let userChoice = choices[Math.floor(Math.random() * choices.length)]; // Random user choice for demo
console.log("You chose:", userChoice);

// Step 3: Computer picks a random choice
const computerChoice = choices[Math.floor(Math.random() * choices.length)];
console.log("Computer chose:", computerChoice);

// Step 4: Compare userChoice and computerChoice
if (userChoice === computerChoice) {
  console.log("It's a tie!");
} else if (userChoice === "rock" && computerChoice === "scissors") {
  console.log("You win!");
} else if (userChoice === "scissors" && computerChoice === "paper") {
  console.log("You win!");
} else if (userChoice === "paper" && computerChoice === "rock") {
  console.log("You win!");
} else {
  console.log("You lose!");
}

// Bonus: Put the whole game in a loop
// Uncomment to play multiple rounds in browser
/*
while (true) {
  let userChoice = prompt("Choose rock, paper, or scissors (or 'quit' to stop):").toLowerCase();
  
  if (userChoice === 'quit') {
    console.log("Thanks for playing!");
    break;
  }
  
  const computerChoice = choices[Math.floor(Math.random() * choices.length)];
  console.log("Computer chose:", computerChoice);
  
  if (userChoice === computerChoice) {
    console.log("It's a tie!");
  } else if (userChoice === "rock" && computerChoice === "scissors") {
    console.log("You win!");
  } else if (userChoice === "scissors" && computerChoice === "paper") {
    console.log("You win!");
  } else if (userChoice === "paper" && computerChoice === "rock") {
    console.log("You win!");
  } else {
    console.log("You lose!");
  }
}
*/
```