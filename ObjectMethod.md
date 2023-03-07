<h1>Object methods, "this"</h1>

// these objects do the same

user = {
  sayHi: function() {
    alert("Hello");
  }
};

// method shorthand looks better, right?
user = {
  sayHi() { // same as "sayHi: function(){...}"
    alert("Hello");
  }
};

<p>As noted function can be omitted by just using sayHi() without a function</p>

let user = {
  name: "Raymond",
  age: 20,

  sayHi() {
    // "this" is the "current object"
    alert(this.name);
  }

};

user.sayHi(); // Raymond

-----

let user = { name: "John" };
let admin = { name: "Admin" };

function sayHi() {
  alert( this.name );
}
