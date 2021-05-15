# Exercises

## 0 Setup

1. Fork the github [https://github.com/beaumoaj/components_and_props.git](https://github.com/beaumoaj/components_and_props.git) and clone YOUR COPY to your Ubuntu system.
2. Open an Ubuntu terminal window and `cd` into `components_and_props`
3.  Run the following commands in the terminal window:
    ```
    npm install
    npm start
    ```
    Wait for each command to finish.  After the second command, your browser window should open and you will see a page that says:
    ```
    Read the instructions to create components
    ```

You are now ready to start

## 1. Creating components.

1. Inside the `src` folder, create a new component called `Greeting`.  Inside the component, declare a variable called name and assign it your name as a string value.
    ```javascript
    const name = "Tony";
    ```
    This component should output the following header:
    ```html
    <h1>My name is {name} and I created this greeting</h1>
    ```
2. Inside `App.js`, find the line of code which says:
    ```html
    <p>Read the instructions to create components</p>
    ```
    and replace it with a call to your new `<Greeting/>` component.  Check that when you view the app, you see the greeting message.  Open the developer tools and check for errors in the console.
4.  Modify your `Greeting` component so that instead of using a local variable inside the component, you pass the name into the `props` for the component.  Modify the component first.  Make sure you add a `props` argument and then modify the variable declaration:
    ```javascript
    const name = {props.name};
    ```
    Now edit `App.js` to ensure that you pass the name property.  This is how I would pass my name to the greeting component.
    ```
    <Greeting name="Tony"/>
    ```
