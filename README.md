# Introduction

This is a hackathon boilerplate for a messaging app using the Snap Kit Bitmoji SDK created by Major League Hacking. It is for hackers looking to get started quickly on a new hackathon project using Snap Kit.

# Prerequisites

This project requires the following tools:

* [Firebase](https://firebase.google.com/) - A mobile and web application development platform. Firebase’s Cloud Firestore will store and sync messages between users of your app.
* [Node.js](https://nodejs.org/en/download/) - An open-source, cross-platform JavaScript run-time environment that executes JavaScript code outside of a browser.
* [Snap Kit SDK](https://kit.snapchat.com/) - Lets hackers like you integrate some of Snapchat's best features across your hacks.

To get started, create a [Firebase](https://console.firebase.google.com/) and [Snap kit](https://kit.snapchat.com/) account if you haven't already, you can use your Snapchat credentials if you have one to log into Snap Kit. 

# Getting Started

**Step 1: Configure Firebase in Your App**

Open `script.js`, and fill in the Firebase config from earlier. This will give your web app access to the Cloud Firestore.

```
firebase.initializeApp({
  /* Fill in the following values based on your config. */
  apiKey: "",
  authDomain: "",
  databaseURL: "",
  projectId: "",
  storageBucket: "",
  messagingSenderId: ""
});
```

**Step 2: Set Up a Web Server**

You’ll need to host your web app with a server in order to leverage the Skap Kit SDK. Open your terminal, and run the following command. Do keep in mind that [Node.js](https://nodejs.org/en/download/) is required to run the `http-server` command. 

```
$ npm install http-server -g
```

Once installed navigate to the folder that holds the sample project files and use the following command to start your server.

```
$ http-server
```

`http-server` will output a link to our server which in this case `http://127.0.0.1:8080`. The server address is equivalent to `localhost` so moving forward we will utilize the latter. Enter the following URL into your browser (be sure to replace the port number with the number provided by `http-server`)

Open http://localhost:8080 to view it in your browser.


**Step 3: Configuring the Snap Kit SDK**

Before working with the Snap Kit Development Kit, you'll need to get your Snap Kit credentials. Navigate to the [Snap Kit Development Portal](https://tinyurl.com/y738hmag) and Create an account. Alternatively, you can login using your Snapchat account.

1. Add a new Snap application by hitting ht `+` symbol
2. Enable the Bitmoji Kit under `Kits` 
3. Add a redirect URL which is your localhost URL `http://localhost:8081/`
4. Configure your development environment by toggling the `web` client on.

**Step 4: Adding Bitmoji Kit to your app**


Now that we have configured all the starting steps to our application, we can now add the Bitmoji Kit to our application. We will be adding the Bitmoji Icon to our messaging bar. 

Open `index.html`, and add a placeholder `<div>` where our sticker picker would go

```
<div class="controls">
  <input id="messageInput" type="text" placeholder="Type a message..."/>
  <i id="namePicker" class="material-icons">account_box</i>
  <div class="bitmojiStickerPicker"></div>
</div>
```

# What's Included?

# Code of Conduct

We enforce a Code of Conduct for all maintainers and contributors of this Guide. Read more in [CONDUCT.md](https://github.com/MLH/mlh-hackathon-flask-starter/blob/master/docs/CONDUCT.md).

# License

The Hackathon Starter Kit is open source software [licensed as MIT](https://github.com/MLH/github-hackathon-starter/blob/master/LICENSE.md).
