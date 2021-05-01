# Class 05 Summary:

### Thinking in React:

 * To break a mock into a component heirarchy : every Component draw around it a box, each box has the same name of the component . The component has its own functionality("only do one thing"). Then map the Json data model with User Interface .
*********************************************************

* single responsibility principle is a technique to make each component do only one function and then convert to small subComponent. Each component matches one section in the model of Data.

* arranging component into a hierachy. will appear the component as a child.

*********************************************************

* Static version application is aplication contain static component can reuse and pass data  between components but with no interactivity. You may typing a lot but no thinking.

*********************************************************

* You need to add : top-down or buttom-up to build components , these componenrts havr render function and pass the data using props not state , because we need to make it static with no interactivity.

*********************************************************
 
 * The three questions to determine if something is state:

 1. if the data passed from parent using props  , isn't state.

 2. if the data unchanged , is'nt state.

 3. if the data can computed by another state or component , isn't state.

 ********************************************************

 * Steps to figure the state:

 1. every component render anything based on that state must be identify.

 2. identify component contain all component related to the state.

 3. the common or another component should have the state.

*********************************************************

* To decide where  the live state should be, we must identify the minimal set of app state and which component has this state.

*********************************************************
