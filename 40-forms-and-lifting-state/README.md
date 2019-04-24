Controlled Forms and Lifting State
======================

## SWBATs

- [ ] Debug the `event` object we get in our event handler callbacks
- [ ] Write fully controlled forms

- [ ] Manipulate the DOM by changing values in `state` instead of using vanilla JS

- [ ] Pass data up and down the component hierarchy with our callbacks
- [ ] Draw a component hierarchy and describe the Flow of Information

## Lecture Notes

How do we capture form data in JS?

Add event listener to form (submit)
Capture values of the inputs from
  - Find the input field
  - Grab its value
Do whatever you need to do with the user input


 For Next Lecture:

 Delete a turtle
 Update a turtle
 Front-end form validations
 What happens when you get to the end of the turtles??
 Ninjify???
 Back to the pond????


### Lifting State

[Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)

> Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor.

If two sibling components need access to the same `state`, you will want to place the shared `state` in a parent container. Then you can pass down that `state` as well as any functions that need to modify the state as props to the two sibling components that need to display and/or change that data.

**Metaphor Time!**

**DISCLAIMER:** _This metaphor may confuse you more, so read only if you dare!!_

Think of your React app as a hydroelectric dam made of legos. Your legos are React components. `state` is like the energy / water that can be generated and used by the legos (aka: components). That energy comes in the form of `props`.

Anytime a component needs energy, it can either be from itself (poke a hole in that lego) === the component has `state`.

OR

If multiple components need that energy, you poke a hole in some higher up lego (a container component holding the other components) so it can spill out water (aka: `state`) and give it to its children via `props`.

## Extras

- [Reconciliation](https://reactjs.org/docs/reconciliation.html)