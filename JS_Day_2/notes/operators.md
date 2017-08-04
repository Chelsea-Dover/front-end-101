# JavaScript Operators
Javascript uses arithmetic operators to compute values.
e.g.
```
(1 + 2) * 3
```
When computing values you may contain variables

e.g.
```
var x = 1;

(x + 2) * 3
```

The values don't have to be numbers. They can be many various types such as strings

e.g.
```
'Hello' + ' '  + 'world!'
```

Because the equals sign ( = ) is used to assign values. When comparing two values to see if they match `==` will determine if they are equal (e.g. `1 == 2` will return false) and `===` will determine if both the value and the type match (e.g. `1 == '1'` will return false)

**All Comparison Operators Are:**
- ==: equal to    1 == 2 will be false
- ===: equal value and type    1 === '1' will be false
- !=: not equal    1 != 2 will be true
- !==: not equal value and type    1 !== '3' will be true
- >: greater than    1 > 2 will be false
- <: less than    1 < 2 will be true
- >=: greater than or equal to    1 >= 1 will be true
- <=: less than or equal to    1 <= 1 will be true

You can also combine operators by using logical operators

**All Logical Operators Are:**
- &&:	and    (1 >= 1 && 3 > 1) will be true
- ||:	or    (1 > 3 || 1 < 3) will be true
- !:	not    !(1 == 3) will be true
