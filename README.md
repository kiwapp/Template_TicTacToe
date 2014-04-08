# Template_TicTacToe

This application provides a form followed by a game : a scratchcard. Your data will be send to [Parse](https://parse.com/) or your own server. You to can customize :

- Probabilities
- Your parse credentials
- Your server url

## File organisation

```shell
.
├── app/ : Build app ready to run
├── config/ : An exemple of kiwapp's config. It allows you to run the application in the browser
├── README.md
├── app.zip
└── src // where you code
    ├── .bowerrc
    ├── .editorconfig
    ├── .gitignore
    ├── .jshintrc
    ├── GulpFile.js
    ├── bower.json
    ├── package.json
    ├── layout // Your app layout (header,footer...)
    ├── partials // HTML partials
    ├── styles // Your css
    ├── assets // static files such as images for this applications
        ├── images // Your app images
        └── type // Fonts for the app
    └── js // Your backbone app
```

### Use the source code

Inside `src/``it's our source code for this application. It's built on top of :

- Node
- Npm
- Bower
- Gulp
- Backbone
- jQuery
- Lodash
- KiwappLib

To install you have to run inside a terminal : `npm install && bower install` inside this directory.
Then launch `gulp` to edit the application.

## Customize images

Currently you have to change the images inside `app/assets/images` or if you edit the source, inside the `src/assets/images`. Then upload a new version inside the manager.

## Add some custom parameters to your app

You can edit these inside the manager. Got to [Kiwapp Manager](https://retail.kiwapp.com/site/login).

- When you're logged in select your shop
- Select your app-set
- Next to the version of your app there is nut, click
- You must see a page *Setup your app:*

### Setup parse

- Check the checkbox inside the field ActiveParse if you want to use Parse
- Write your credentials if any

That's it. Now parse is ready to run, you can sync your device.

### Setup your webservice

- Write your Webservice url if you want to use your own server

We will send you this JSON :

```json
{
    "name": "",
    "appName": "",
    "mobile": "",
    "email": "",
    "country": "",
    "company": "",
    "surname": "",
    "current_date": "2014-04-04T14:24:28.642Z",
}
```

### Setup your scratchcard configuration

- Fill the fields you want, if its value is 0, these option will never show up.
- Fill the field *Minimum completion percent* (> 85 to have a realistic effect)


Now, you can save these fields by clicking in **OK**. Now deploy your app !