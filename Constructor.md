<h1>Constructor, Operator "new"</h1>

<p>If you need to create multiple similar objects, its recommendable to use the "new" operator
in a constructor function.</p>

<h2>Constructor function</h2>
<ul>
<li>They are named with capital letter first</li>
<li>They should be executed only with "new" operator</li>
</ul>

<h3>For Example:</h3>

function User(name, lastName) {
  this.name = name;
  this.lastName = lastName;
  this.isAdmin = false;
}

let user = new User("Jack", "Raymond");

alert(user.name);
alert(user.lastName); // Jack
alert(user.isAdmin); // false

<h2>Important note:</h2>

<p>When a function is executed with "new", the following happens:</p>
<p>A new empty object is created and assigned to "this".</p>
<p>The function body executes. Usually it modifies "this", adds new properties to it.</p>
<p>The value of "this" is returned.</p>


function User(name) {
  // this = {};  (implicitly)

  // add properties to this
  this.name = name;
  this.isAdmin = false;

  // return this;  (implicitly)
}

<h2>Example:</h2>


function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

const car1 = new Car('Eagle', 'Talon TSi', 1993);

console.log(car1.make);
// Expected output: "Eagle"

<h1>Return from constructors</h1>
<ul>Rule for return statement in a constructor</ul>
<li>return is called with an object then the object is returned instead of "this"</li>
<li>if return is called with a primitive,its ignored</li>
<li>Return overides "this" by returning an object</li>

<h2>Example:</h2>

function BigUser() {

  this.name = "John";

  return { name: "Godzilla" };  // <-- returns this object
}

alert( new BigUser().name );  // Godzilla, got that object

<h2>If return is empty this is the result:</h2>

function SmallUser() {

  this.name = "John";

  return; // <-- returns this
}

alert( new SmallUser().name );  // John

<h3>Another note:</h3>
<p>Omitting parentheses</p>

let user = new User; // <-- no parentheses
// same as
let user = new User();


<h3>Methods in constructor</h3>

function User(name) {
  this.name = name;

  this.sayHi = function() {
    alert( "My name is: " + this.name );
  };
}

let john = new User("John");

john.sayHi(); // My name is: John

--------

Example:

function User(name, lastName) {
    this.name = name;
    this.lastName = lastName;

    this.sayHi = function() {
        alert("My full name is:" + this.name + " " + this.lastName);
    };
}

let fullName = new User("Raymond", "Del Rosario");

fullName.sayHi(); //My name is: Raymond Del Rosario