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



