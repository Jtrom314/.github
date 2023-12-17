# Startup JavaScript

Now that you have learned how to make an application interactive, it is time to add some JavaScript to your startup application. The main thing you should focus on in this deliverable is making your application minimally viable. The application doesn't have to do everything it will do once you are done, but it should be completely usable to some extent at this point.

To make your application usable you may need to use JavaScript to generate mock data that represents data that you will eventually get from the server, or from another user. For example, if you are building a chat app then you might need to have JavaScript that periodically generates a hard coded message that gets inserted into your application display. One way to do this is to use the `setInterval` function.

```js
let chat = 'Carpe diem';
setInterval(() => {
  chat = `${chat} lorum ipsum`;
  document.querySelector('#chat-response').textContent = chat;
}, 5000);
```

You must use the same startup GitHub repository that you created with your earlier startup deliverables. Update the notes.md file with things that you learn as you work on your startup. As you make changes to your HTML, CSS, and JavaScript commit those changes and push them to GitHub. You will need at least four commits to get full credit, but in reality you should have many more than that.

Leverage what Simon teaches in order to learn how to read login information, represent database data, and save and display data in `localstorage` between pages and browser sessions.

Remember to use the `VS Code Live Server` extension to see what your code looks like in the browser. Also use the browser's debugger window to debug your CSS and JavaScript. This will save you a lot of time if you learn how to leverage these tools.

Once you have developed your application to where you want it, you need to release it to your production environment. Use the deployment `deployFiles.sh` script from the [Simon JavaScript repository](https://github.com/webprogramming260/simon-javascript/blob/main/deployFiles.sh) to deploy your application. Make sure you specify `startup` for the service parameter (`-s`).

```sh
./deployFiles.sh -k <yourpemkey> -h <yourdomain> -s startup
```

For example,

```sh
./deployFiles.sh -k ~/keys/production.pem -h yourdomain.click -s startup
```

Doing this will make this deliverable of your startup available from `https://startup.yourdomainname`.

## ☑ Assignment

1. Review and deploy Simon JavaScript
   1. Clone the Simon JavaScript repository to your development environment.
   1. Open the project in VS Code and examine the application's use of JavaScript.
   1. Execute in your development environment using the VS Code Live Server extension.
   1. Debug using the browser's dev tools to step through the JavaScript using the Source tab.
   1. Deploy to your production environment using the deployment script so that it is available with your domain's `simon` subdomain.
1. Represent each of the required technologies with JavaScript either as a complete implementation or with mocked implementation that will be replaced later.
   1. Have JavaScript that takes user input and adds it to the mocked database data. This should be something simple like an array or object in your JavaScript that will eventually be replaced by service endpoint database calls.
   1. Have JavaScript that reads the login input and displays the user name.
   1. Have JavaScript that mocks your database data and injects it into the DOM.
   1. Use the `localstorage` API to keep data between pages and browser sessions.
   1. Have JavaScript that mocks out the realtime data you expect to get from the server using WebSocket and inject it into the DOM.
1. Make sure your name is displayed in the application and that there is a link to your GitHub repository.
1. Periodically commit and push your code to GitHub.
1. Periodically update your startup repository's notes.md file to reflect what you have learned and want to remember.
1. Push your final version of your project to GitHub.
1. Deploy your startup application to your production environment (your server).
1. Make sure your application is available from your production environment.
1. Upload the URL to your startup application to the Canvas assignment.

## Grading Rubric
The following are required for your startup to be considered on time to be graded (Note: if one of these requirements are missing, you will be required to resubmit your assignment)

- (Required) Simon HTML deployed successfuly to your production environment
-    // Can we move the grading of this to be something the TAs grade instead of a self grade? We've had a few students that would say that they deployed Simon but didn't and the TAs often wouldn't check
- (Required) Startup deployed successfuly to your production environment
-    // I feel that this is needed since there were quite a few students that submitteded their project to be considered 'on time' that didn't have their startup deployed. I feel that when the students submit, they are telling us that they have checked that everything is ready to go.
- (Required) All required technologies from previous startup assignments are present
- (Required) A link to your GitHub startup repository prominently displayed on your application's main page. Your Github must be accessable by every grading TA at the time of submission
- (Required) Notes in your startup Git repository README.md file documenting what you modified and added with this deliverable. The TAs will only grade things that have been clearly described as being completed. Review the [voter app](https://github.com/webprogramming260/startup-example) as an example.
-    // Can we enforce this requirement more foreefully this time around or if we aren't going to, can we remove this from what we are expecting the students to do? I find it odd that we say that it is required when we are told to not really care about it when we grade these assignments

After you have completed the above requirements, your startup will be graded on the following critera
- Significant use of JavaScript to create a viable working application
  - 20% JavaScript support for future login.
    - Refer to [Assigment 2.ii and 2.iv](##Assignment) for help
  - 20% JavaScript support for future database data.
    - Refer to [Assigment 2.i and 2.iii](##Assignment) for help
  - 20% JavaScript support for future WebSocket.
    - Refer to [Assigment 2.v](##Assignment) for help
  - 30% JavaScript support for your application's interaction logic.
    - All of your frontend Javascript should work as intended without errors in the console
- 10% - Multiple Git commits with meaningful comments.

## Go celebrate

You did it! This is a significant milestone. Time to grab some friends, show them what you did, and celebrate with cupcakes 🧁.
