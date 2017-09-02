# RGL (responsive-grid-light)

This partial is intended as a super lightweight responsive grid mixin for easy adaptation. It has a very low entry cost and can be especially helpeful within projects that follow a specifc terminologies like the BEM methodology (http://getbem.com/).

I'm using the flexbox method for container building but you can easily change it to float elements or extend it to use either.

The goal with this was to keep something super simple and lightweight so that I can adapt it and reuse it on other projects as needed.


## Getting started
coming soon

### Defining your breakpoints

Using the variables below define your breakpoints. these breakpoints take into account a wide range of screensizes but you can change it and extend it as needed.

```

// Define your breakpoint sizes
$break--xs-min:   0;
$break--xs-max:   575px;

$break--sm-min:   ($break--xs-max+1);
$break--sm-max:   767px;

$break--md-min:   ($break--sm-max+1);
$break--md-max:   991px;

$break--lg-min:   ($break--md-max+1);
$break--lg-max:   1199px;

$break--xl-min:   ($break--lg-max+1);
$break--xl-max:   1439px;

$break--xxl-min:  ($break--xl-max+1);
$break--xxl-max:  100%;


```

### Setting your config values

You can define your project specific configs here.

```

// Define your config values
$grid-vars: (
  'prefix': 'grid', // class prefix
  'columns': 12, // number of columns
  'gutters': 15, // gutter width
  'container': 100%, // container fluid or sized
);

```

### rem function()

A small funtion to calculate px to rem is included. It asumes the 16px root font-size to use for the formula. You can change this to use your own root font-ssize if you need to.

```
rem(15) // uses 16px as root
```
or

```
rem(15, 'yourvalue') // to use your custom value
```




