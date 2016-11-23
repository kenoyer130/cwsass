# Sassy CW example

## INSTALL
* make sure you have the latest nodejs installed
* run `npm install`
* run `npm run build-css` to generate the new style sheet

## What is SASS?
Sass is an extended version of CSS that allows us to use advanced features while still shipping a raw CSS file.
[http://sass-lang.com/]

## What features of SASS are cool?
* variables
* multiple files that are merged into one
* [http://sass-lang.com/guide]

## Example explained
Look in the scss folder. This is the precompiled raw files that are edited.

### source files
*colors.scss*
```
$foreground-color: #333333;
$background-color: #ffffff;
$default-margin: 5;
```

*ConnectWise.scss*
```
@import "colors";
@import "ConnectWise_Widget.scss";

body {
  margin: $default-margin;     
  background-color: $background-color;
  color: $foreground-color;    
}
```

*ConnectWise_Widgets*
```
.widget {
  background-color: $background-color;
}
```

### Css Output
```
.widget {
  background-color: #ffffff; } 

body {
  margin: 5;
  background-color: #ffffff;   
  color: #333333; }
```
