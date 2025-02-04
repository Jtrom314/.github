# Startup DB

Now that you have learned how to set up and use a database, it is time to add that functionality to your startup application. The main things you should focus on in this deliverable include connecting to the database, creating endpoints that accept and return data, storing and retrieving data from the database.

You must use the same startup GitHub repository that you created in the earlier instruction. Update the `notes.md` file with things that you learn as you work on your startup. As you make changes to your HTML, CSS, and JavaScript commit those changes and push them to GitHub. You will need at least four commits to get full credit, but in reality you should have many more than that.

Remember to use the browser's debugger window to debug your frontend HTML, CSS and JavaScript. You can also debug your backend service JavaScript running on Node.js using the built in VS Code Node.js debugger.

Once you have developed your application to where you want it, you need to release it to your production environment. Use the `deployService.sh` script from the [Simon DB repository](https://github.com/webprogramming260/simon-db/blob/main/deployService.sh) and use `startup` for the service parameter (`-s`).

```sh
./deployService.sh -k <yourpemkey> -h <yourdomain> -s startup
```

For example,

```sh
./deployService.sh -k ~/keys/production.pem -h yourdomain.click -s startup
```

Doing this will make this deliverable of your startup available from `https://startup.yourdomainname`.

## ☑ Assignment

1. Review and deploy Simon DB
   1. Clone the Simon DB repository to your development environment.
   1. Run `npm install` in root of the project.
   1. Open the project in VS Code and examine the application's use of JavaScript to support database interactions.
   1. Create and configure the `dbConfig.json` file with your MongoDB credentials.
   1. Execute in your development environment by debugging the application using VS Code's Node.js debugger (press F5 while viewing index.js). Set breakpoints in VS Code and step through the backend JavaScript related to database interactions.
   1. Open your browser to https://localhost:3000 and use the browser's dev tools to step through the frontend JavaScript using the Source tab.
   1. Deploy to your production environment using the deployment script so that it is available with your domain's `simon` subdomain.
1. Add code for connecting to the database
1. Provide endpoints for adding, updating, and deleting your application data in the database
1. Persist data in MongoDB.
1. Display the user data in the frontend by manipulating the DOM.
1. Make sure your name is displayed in the application and that there is a link to your GitHub repository.
1. Debug your application using VS Code's Node debugger and the browser's dev tools, in your development environment, to verify it is working correctly.
1. Periodically commit and push your code to GitHub.
1. Periodically update your startup repository's `notes.md` file to reflect what you have learned and want to remember.
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
-    // Can we enforce this requirement more forcefully this time around or if we aren't going to, can we remove this from what we are expecting the students to do? I find it odd that we say that it is required when we are told to not really care about it when we grade these assignments

After you have completed the above requirements, your startup will be graded on the following critera
- Application database support
  - 20% - MongoDB Atlas database created
  - 40% - Provides backend endpoints for manipulating application data
  - 30% - Stores application data in MongoDB
- 10% - Multiple Git commits with meaningful comments.

## Go celebrate

You did it! This is a significant milestone. Time to grab some friends, show them what you did, and celebrate by eating a salad 🥗.
