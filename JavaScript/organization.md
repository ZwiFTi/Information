# Organization of code

## Model
- Where the data is stored (objects)
- from server and from user

## View
- All the stuff users sees
- Dom elements, input elements, buttons, images
- For giving and reading data


## Octopus
- Binds View and Model together

## Rules

1. Don't mess up the data in the model
2. Model and View NEVER talk to eachother

## Split up the views

You split up views if they are different functionally, not with regard to action, but to regard with what gets rendered.





## The stuff

octopus:

1. init method starts off the entire application

render functions: should redraw the respective area
