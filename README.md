# RGL (responsive-grid-light)

This partial is intended as a super lightweight responsive grid mixin for easy adaptation. It has a very low entry cost and can be especially helpeful within projects that follow a specifc terminologies like the BEM methodology (http://getbem.com/).

I'm using the flexbox method for container building but you can easily change it to float elements or extend it to use either.

The goal with this was to keep something super simple and lightweight so that I can adapt it and reuse it on other projects as needed.


## Getting started

1. Add RGL as a dependency:
```
npm install responsive-grid-light --save-dev
```

2. Import RGL your into your Sass files:
```
@import "~responsive-grid-light/grid";
```

3. Initilzie the the RGL mixin:
```
@include buildout-rgl(); 
```

### Setting your config values

You can define your project specific configs here.

```
//Defaults

$config: (
  'prefix': 'grid',  // class prefix
  'columns': 6, // number of columns
  'gutters': 15, // gutter width
  'container': 100%,
  'media-vars': ( // media variables for different screensizes
      'xs': 0,
      'sm': 576,
      'md': 768,
      'lg': 992,
      'xl': 1200,
      'xxl': 1440,
    )

);

@include buildout-rgl($config); 
```


| Options       | Description   |
| ------------- |:-------------:|
| prefix        | set custom class prefix here |
| columns      	| tnumber of columns to create |
| gutters 		| gutter widths    |
| container     | container width  / fixed or fluid|
| media-vars    | define all various brealpoints (using min-wdith)    |



### rem function()

A small funtion to calculate px to rem is included. It asumes the 16px root font-size to use for the formula. You can change this to use your own root font-ssize if you need to.

```
rem(15) // uses 16px as root
```
or

```
rem(15, 'yourvalue') // to use your custom value
```




