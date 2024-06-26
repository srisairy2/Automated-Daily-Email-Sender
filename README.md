# Automated Daily Email Sender

This is a Node.js application that is meant to send a scheduled email at 10 AM EST daily with a simple message.

### My Approach and the Decisions Made

When approaching this project, the first thing I did was learn how to use the nodemailer and node-cron libraries. I decided to do so by reading the documentation for each library. Since the functionality/purpose of each library is fairly simple, this allowed me to learn how to do the project quickly. Once I had done that, I moved on to actually writing the code for the application, which is in `sender.js`.

One important decision I made during development was to print out a confirmation message every time an email was sent out, as that shows anyone who runs the application that it is functioning properly. I also chose to handle errors by sending emails by printing the error status, which helps users see if the application is doing what they want it to do.

## Install Necessary Packages/Files

### Node.js and NPM

Install [Node.js and NPM](https://nodejs.org/en/download) if they are not installed already

### Clone Github Repository

Navigate to the directory where you want the application to be cloned to in terminal/command prompt, then run the following command:

```sh
git clone https://github.com/srisairy2/Automated-Daily-Email-Sender.git
```

If the following command doesn't work, then just go to the main page for this repository, click the green button labeled "Code", then copy the HTTP URL given.

### Nodemailer and Node-cron Libraries

Inside the directory where this README.md file is located, run the following code to install the nodemailer and node-cron libraries:

```sh
npm install nodemailer node-cron
```

## Configure Gmail Account to Send Automated Emails

By default, this application is configured to use a Gmail account that I have created (ssairy.mailer@gmail.com) to send emails. If you do not wish to change this, then you can skip to the [next section](#application-set-up).

If you wish to configure a different account for sending emails, then do the following steps:

- Go to the [Google account page](https://myaccount.google.com/) of the email you want to use to send automated emails
- Switch to the account that you want to send automated emails from
- Go to the `Security` Tab
- Turn on `2-Step Verification`
- Within the `2-Step Verification` page, click on the option `App Passwords`
- You should be given a dropdown labeled `Select app`
- Click on the drop-down and choose the option `Other`
- Set the `App Name` field to Automated-Daily-Email-Sender
- Click `Generate`
- An automatically generated password will be given
- Copy the password to your clipboard

## Application Set Up

If you chose to use an email other than ssairy.mailer@gmail.com to send the automated messages, do the following steps:

- Open `sender.js` in a text editor of your choice
- Within the `transporter` variable, set `user` to the email address you're using to send emails
- Also within `transporter`, set `pass` to the auto-generated password you obtained in the previous section
- Within the `mailOptions` variables, set `from` to the email address you're using to send emails

Once that is done, you now need to configure the app to send the automated messages to a specific email. To do so, do the following steps:

- Open `sender.js`
- Within the `mailOptions` variable, set `to` to the email address you want to send automated emails to

## Start Sending Emails

Once all the above steps are completed, cd to this directory in terminal and run the following command to run the application:

```sh
npm start
```

If that does not work then run the following command instead:

```sh
node sender
```
