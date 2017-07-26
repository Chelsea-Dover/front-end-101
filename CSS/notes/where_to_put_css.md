# Where to put CSS
---

There are three places to add css to your webpage.
- inline
- embedded
- external

## Inline
Inline css is the least desirable out of the three because it can be quite hard for maintain. In the CSS hierarchy it is one of the most unique, therefor it will override almost all other CSS.

The way to add inline style to your HTML is by using the `style` attribute. Here's an example:
`<p style="background:red;">hello!</p>`

## Embedded
Embedded css is the second least desirable out of the three. It's better than inline when it comes to maintenance but it's still not the best. In the CSS hierarchy it will act the same way as an external stylesheet, so how unique the style is will depend on the selectors you use.

The way to add inline style to your HTML is by using the `<style>` tag in your html head. Here's an example:
```
<style>
  p {
    background:red;
  }
</style>
```

## External
External css is the most desirable out of the three. You can use the same stylesheet for multiple HTML files making maintenance easier and helps section out your file for a more clear file. In the CSS hierarchy it will act the same way as an embedded stylesheet, so how unique the style is will depend on the selectors you use.

The way to add an external stylesheet to your HTML is by using a `<link/>` tag in your html head with the path to your css file. Here's an example:
`<link rel="stylesheet" type="text/css" href="style.css">`
