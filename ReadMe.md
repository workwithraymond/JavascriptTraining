Objects can be created two ways:
Object constructor 
Object literal

let user = new Object(); //object constructor
let user = {}; //object literal

------------------------

<h1>Literal and Properties</h1>

let user = {  //an object
    name: "Raymond" //key is the name and value is John
    age: 20  

};

//Its important to note that objects can be removed, added, and read:

<p>As we noted above USER is the object which has keys and values. </p>
<p>The way to access properties and values is by using the dot notation for instance:</p>

console.log(user.name); //Raymond
console.log(user.age); //20

<h2>To remove a property</h2>

delete user.age;

<p>Another important note properties names can be multi-word using a quote</p>

let user = {
    name: "Raymond"
    age: 20,
    "likes dogs": true //As you see multi-word quoted
};

<h2>Property value Shorthand</h2>

function newUser(name, age){
    return{
        name: name,
        age: age,

    };
}

let user = newUser("Raymond", 20);
console.log(user.name);

<h3>Alternative property value example</h3>

function newUser(name, age) {
    return {
        name,
        age,
    };
}

///

let user = {name: "Raymond", age: 20};

console.log("age" in user);
console.log("name" in user);

<h1>Introducing the for in loop</h1>
<p>This kind of loop is different than the other loops</p>

for (key in object) {
    //executes the body for each key among object properties
}

<h2>For Example</h2>

let user = {
  name: "John",
  age: 30,
  isAdmin: true
};

for (let key in user) {
  // keys
  console.log( key );  // name, age, isAdmin
  // values for the keys
  console.log( user[key] ); // John, 30, true
}

<h2>Ordered like an object</h2>
<p>In this example it whenever a property has quotation mark even though
its a number it takes it in order</p>

let codes = {
  "49": "Germany",
  "41": "Switzerland",
  "44": "Great Britain",
  // ..,
  "1": "USA"
};

for (let code in codes) {
  alert(code); // 1, 41, 44, 49
}

<h2>The way around this is by adding plus sign in front of number</h2>

let codes = {
  "+49": "Germany",
  "+41": "Switzerland",
  "+44": "Great Britain",
  // ..,
  "+1": "USA"
};

for (let code in codes) {
  alert( +code ); // 49, 41, 44, 1
}
