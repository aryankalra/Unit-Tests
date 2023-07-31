## Tests

Proper dependencies were installed via _yarn_ instead of _npm_. All tests are also run as _yarn test_ instead of _npm test_ due to the overload of errors using _npm_. A stable solution was searched for, however it lead to an increased amount of errors and failures, whereas _yarn_ was a simple command to utilise and test.

Upon also trialing different commands and playing around with the dependencies, _npm test_ does work and does successfully pass the tests.

If the tests do not pass the test, the following commands should be run to install the necessary dependencies to be able to successfully run the tests:

```
yarn add --dev @testing-library/react-native

yarn add --dev react-test-renderer
```

All three tests pass perfectly.

## Test 1: /components/AppButton.test.js

In the first test case, it verifies that the component renders correctly by checking the presence of the provided title ('Test Button').

The second test case simulates pressing the button and checks if the provided onPress function is called.

The terminal output when the test is run should be:

AppButton
✓ renders correctly with the provided title
✓ calls the onPress function when the button is pressed

## Test 2: /navigation/TabNavigator.test.js

This test case verifies that the TabNavigator component can render without any errors. It uses the render function from @testing-library/react-native to render the TabNavigator component in a virtual environment.

By rendering the component, the test case checks if the component and its child components can be rendered successfully. If there are any errors or exceptions thrown during the rendering process, the test case will fail.

## Test 3: /components/AppIcon.test.js

In this test, it's rendering the AppIcon component and passing the required prop name. It's using the book icon name as an example, but it can be replaced it with any valid icon name from the MaterialCommunityIcons library.

The purpose of this unit test is to ensure that the AppIcon component renders without any errors.

## Unit Test Explanation

Each test in the provided code can be classified as a unit test because it focuses on testing a specific unit of code in isolation, rather than testing the interactions between multiple components or systems.

Unit tests are typically designed to test individual units of code, such as functions, components, or modules, in isolation from their dependencies. These tests aim to verify the correctness of the unit's behavior and catch any potential bugs or issues within that unit. By isolating the unit being tested, it becomes easier to identify the cause of failures and maintain the overall stability and reliability of the codebase.
