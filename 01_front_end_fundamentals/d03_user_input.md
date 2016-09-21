## Homework: User Input

It is time for you to explore how to accept user input on your own. Web browsers have three default methods that accept user input. These can be sued inside of Chrome's Developer Tools in the Javascript Console. They are:

* `prompt(stringArgument);`
* `confirm(stringArgument);`
* `alert(stringArgument);`

#### Challenge

> *Methods* are the computer science term for an "action" or "verb" that an object can perform.

1. In classical programming languages, methods that are not **void** return values. Methods that are in fact void will return `null`.
2. Which of these three built-in browser methods are **void**?
3. Which are not?
4. What is the data type that these return?

*Hint*: You can assign user input to a variable and then call it later.

#### Research

When you continuously spam a user with these methods, most **evergreen** browsers will provide the ability to hide popups from a specific website forever. How would this affect your development?

Take a few moments to research the pitfalls of using these browser methods for user input. Have you found any suggestions or alternatives?

#### Practice Problems

Let's work on a few problems to get your developer chops up to par! Use your user input skills to solve the following problems:

* Create a conditional or control flow statement (either switch or if) that detects if a student is of the appropriate age to purchase alcohol. **Alert** them with either a success or failure message.

* You're at a large convention and are running a sign-up booth for a product. Developers that visit your booth need to be able to signup for your newsletter. Create an empty array of developers and another array for their email addresses. Research the `String.split()` and `String.join()` methods for splitting strings apart. You'll need to split the first and last names. Using `window.prompt()`, ask for their name and email address. Use `Array.push` to add to these arrays. Add each name to your developers array using the `lastname, firstname` format. `console.log()` both the name and email of the user. This will require you to research string manipulation and changing. You may find some random names (check out https://randomuser.me/) or populate data from your classmates. 
