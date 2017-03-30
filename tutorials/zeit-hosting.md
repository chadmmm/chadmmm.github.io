---
layout: tutorial
type: tutorial
title: Zeit Hosting
date: 2017-03-27
published: true
labels:
---

## Zeit Hosting Using Now

#### Install now and meteor-now

Install `now` and the `meteor-now` packages.

```
$ npm install now meteor-now
```


#### Login to now
Login to `now`. You'll receive an email with a link to verify your login.

```
$ now --login
> Enter your email: <your email>
> By continuing, you declare that you agree with https://zeit.co/terms and https://zeit.co/privacy.
- Continue? [y|N]

> Please follow the link sent to <your email> to log in.
> Verify that the provided security code in the email matches Classical Elephant Seal.

✔ Confirmed email address!
```

#### Add project settings to secrets

Add your project's settings to `now secrets` called `meteor-settings`. These are the settings that are located in the `settings.development.json` file.

```
$ now secrets add meteor-settings {
  "cas": {
    "baseUrl": "https://cas-test.its.hawaii.edu/cas/",
    "autoClose": true
  },
  "public": {
    "cas": {
      "loginUrl": "https://cas-test.its.hawaii.edu/cas/login",
      "serviceParam": "service",
      "popupWidth": 810,
      "popupHeight": 610
    }
  },
  "allowed_users": [
    "johnson"
  ]
}
```

#### Setup mLab Mongo database

Setup an `mLab` MongoDB for your project. [review](http://galaxy-guide.meteor.com/deploy-guide.html#mongo-configure)

#### Deploy

Navigate to your meteor project's app directory and run the following command:

```
$ meteor-now -e METEOR_SETTINGS=@meteor-settings -e MONGO_URL=mongodb://<dbuser>:<dbpassword>@ds159988.mlab.com:59988/<dbname> -e ROOT_URL=https://<your choice>.now.sh
```

`-e` is used to set environment variables.

- `METEOR_SETTINGS` is where the project's settings are set.
- `MONGO_URL` is the MongoDB URI that was previously set up at `mLab`.
- `ROOT_URL` will be the URL that your app is going to be located at. More info: [Stack Overflow - Meteor - What is the purpose of “ROOT_URL” and to what should it be defined?](http://stackoverflow.com/questions/24046186/meteor-what-is-the-purpose-of-root-url-and-to-what-should-it-be-defined)


#### Configuring an alias

After your project is finished building and deploying, you'll be given the URL of where it is hosted. For example: `app-hptqoskalf.now.sh`. This does not match your `ROOT_URL` so you want to create an alias to it, which is the same as `your choice` from earlier. Make sure to replace `app-hptqoskalf.now.sh` with the actual URL that you get.

```
$ now alias app-hptqoskalf.now.sh <your choice>.now.sh
```

Your app should now be running at `<your choice>.now.sh`.


#### References

- [Super Simple and Free Meteor Deployments using ZEIT ▲now](https://medium.com/@purplecones/deploying-a-meteor-app-for-free-using-zeit-now-c183329057c9)
- [meteor-now](https://www.npmjs.com/package/meteor-now)