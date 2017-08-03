# Loops
  Loops offer a quick and easy way to do something repeatedly.

When contemplating of loops think of it in just plain english.

If you wanted something to happen for a set number of times you would say something like "for every apple in the basket, do one jumping jack". That is essentially what you do in JavaScript.

e.g.
```
var apples
for (apples = 0; apples < 5; apples ++) {
  console.log('Hello world!')
}
```

There are many different kinds of loops, but they all essentially do the same thing: they repeat an action some number of times (and it's actually possible that number could be zero).

**for loop**
A for loop repeats itself until a specified value evaluates as false.

Syntax:
```
for ([initialExpression]; [condition]; [incrementExpression]){
  statement
}
```

**for in loop**
When using for loops you can also iterate through something such as a list.

So let's say you have a list of strings such as `var cats = ['Eddie', 'Cider', 'Bucky']` and you want to go through it and log out every single one, you can do that like so:

```
var cats = ['Eddie', 'Cider', 'Bucky']

for (catName in cats) {
  console.log(catName);
}
```

**while loop**
A while loop will repeat until the specified condition becomes false.

Syntax:
```
while (condition){
  statement
}
```

**break statement**
break will break out of the current loop.

Syntax:
```
for (var i = 0; i < 10; i++){
  if (x == 1){
    console.log(x);
  }
  if (x == 5){
    break
  }
}
```
