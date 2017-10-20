## vue-form-generator

Simple project with form generator. It's simple.

There are some *form component*.
Just import to parent component and as *:creator* binding pass configuration object.

## configuration

Configuration is array contain other arrays which represents rows in your form.

On row-array you can pass some field objects with options:
* model - vue model for input,
* type - type of field (**IMPORTANT**: it must be same as field component name)
* placeholder
* label

in future there will be also: required, validation etc.

## fields

For now there is:
* text field
* date field

## view

generator split row for equals parts depends on how many fields you have in row.

