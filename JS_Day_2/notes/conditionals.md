# Conditionals
Conditionals let'd you make decisions on what code to evoke based on a specified condition.

**if else**
if/else statements read very similar to english. The syntax is; if (conditional) do one thing, else if (other conditional) do this thing instead, else to this.

e.g.
```
if (my_var === 'a') {
    console.log('we love a!');
}
else if (my_var === 'b') {
    console.log('we love b!');
}
else {
    console.log('we love c!');
}
```

**switch**
The switch statement evaluates an expression. The value of that expression is then compared to all the 'cases'. If there's a match the code for that case will run.

Instead of using `else` as the catch all you may use the keyword `default` which will run if there's not match.

`break` is also a frequently used keyword in switches. The keyword `break` will stop execution of more execution of code and/or case testing inside the block.

```
switch (my_var) {
    case 'a':
        console.log('we love a!');
    break;
    case 'b':
        console.log('we love b!');
    break;
    default:
        console.log('we love c!');
    break;
}
```
