# ES2015ObjectEnhacements
In this exercise ES5 code is refactored into ES2015 code, object enhancements.  

The code shown below is refactored into the function, createInstructorES2015.
function createInstructor(firstName, lastName){
  return {
    firstName: firstName,
    lastName: lastName
  }
}

**Function createInstructorES2015:**
const createInstructorES2015 = (firstName, lastName) => ({firstName, lastName});

**Function computedPropNamesES2015:**
const favoriteNumber = 42;

const instructor = {
  firstName: "Colt",
  [favoriteNumber]: "That is my favorite!"
}

const computedPropNamesES2015 = () => instructor;

**Function objectMethodsES2015:**
const objectMethodsES2015 = {
  firstName: "Colt",
  sayHi() {
    return "Hi!";
  },
  sayBye() {
    return `${this.firstName} says bye!`;
  }
}

**Function createAnimal:**
function createAnimal(species, verb, noise) {
  return {
    species,
    [verb]() {
      return noise;
    }
  };
}

const d = createAnimal("dog", "bark", "Woooof!");
// {species: "dog", bark: ƒ}
d.bark(); // "Woooof!"

const s = createAnimal("sheep", "bleet", "BAAAAaaaa");
// {species: "sheep", bleet: ƒ}
s.bleet(); // "BAAAAaaaa"



