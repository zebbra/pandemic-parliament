![](public/assets/logo_pandemia_parliament.png)


# What's this about?

Democracy as we know it is heavily impacted by covid-19. Decisions can’t be taken, yet it’s more crucial than ever that politicians can do their job. Some parliaments forbid the general population to meet, but they themselves need to meet in person, as there is just no other way.

# What are we trying to achieve?

We want to give the parliament the possibility to meet and vote on their business online. Digitalisation on the fast track, from physical being under one roof to simply doing the same work in a safe virtual space. Politicians need to lead by example, staying at home is the first crucial step!

# Solution ShowCase

We take the parliamentary process from the real-world and transfer it online. As simple as this. Politicians enter the online-lobby, are admitted by people that know them and join the online debate. They can vote on their businesses, do break out sessions with their parliamentary groups and come to the best possible decisions that make our society a great place to live in.
The general public can join in from anywhere in the world and follow the process.
For this hackathon we build a simple ShowCase that gives an impression how an online parliament could look like. All build on Open Source technology, protecting our sovereignty and guaranteeing a high level of security and transparency.


Getting Started
---------------

The easiest way to get started is to clone the repository:

```bash
# Get the latest snapshot
git clone https://github.com/sahat/hackathon-starter.git myproject

# Change directory
cd myproject

# Install NPM dependencies
npm install

# Then simply start your app
node app.js
```

Features
--------



Deployment
----------

Once you are ready to deploy your app, you will need to create an account with a cloud platform to host it. These are not the only choices, but they are my top picks. From my experience, the easiest way to get started is with **Heroku**. It will automatically restart your Node.js process when it crashes, has zero-downtime deployments and supports custom domains on free accounts. Additionally, you can
create an account with **MongoDB Atlas** and then pick one of the *4* providers below.
Again, there are plenty of other choices, and you are not limited to just the ones
listed below.

### 1-Step Deployment with Heroku

<img src="https://upload.wikimedia.org/wikipedia/en/a/a9/Heroku_logo.png" width="200">

- Download and install [Heroku Toolbelt](https://toolbelt.heroku.com/)
- In a terminal, run `heroku login` and enter your Heroku credentials
- From *your app* directory run `heroku create`
- Run `heroku addons:create mongolab`.  This will set up the mLab add-on and configure the `MONGODB_URI` environment variable in your Heroku app for you.
- Lastly, do `git push heroku master`.  Done!

**Note:** To install Heroku add-ons your account must be verified.

---

### Hosted MongoDB Atlas

<img src="https://www.mongodb.com/assets/images/global/MongoDB_Logo_Dark.svg" width="200">

- Go to [https://www.mongodb.com/cloud/atlas](https://www.mongodb.com/cloud/atlas)
- Click the green **Get started free** button
- Fill in your information then hit **Get started free**
- You will be redirected to Create New Cluster page.
- Select a **Cloud Provider and Region** (such as AWS and a free tier region)
- Select cluster Tier to **Free Shared Clusters**
- Give Cluster a name (default: Cluster0)
- Click on green **:zap:Create Cluster button**
- Now, to access your database you need to create a DB user. To create a new MongoDB user, from the **Clusters view**, select the **Security tab**
- Under the **MongoDB Users** tab, click on **+Add New User**
- Fill in a username and password and give it either **Atlas Admin** User Privilege
- Next, you will need to create an IP address whitelist and obtain the connection URI.  In the Clusters view, under the cluster details (i.e. SANDBOX - Cluster0), click on the **CONNECT** button.
- Under section **(1) Check the IP Whitelist**, click on **ALLOW ACCESS FROM ANYWHERE**. The form will add a field with `0.0.0.0/0`.  Click **SAVE** to save the `0.0.0.0/0` whitelist.
- Under section **(2) Choose a connection method**, click on **Connect Your Application**
- In the new screen, select **Node.js** as Driver and version **2.2.12 or later**. _*WARNING*_: Do not pick 3.0 or later since connect-mongo can't handle mongodb+srv:// connection strings.
- Finally, copy the URI connection string and replace the URI in MONGODB_URI of `.env.example` with this URI string.  Make sure to replace the <PASSWORD> with the db User password that you created under the Security tab.
- Note that after some of the steps in the Atlas UI, you may see a banner stating `We are deploying your changes`.  You will need to wait for the deployment to finish before using the DB in your application.



---

