# colephillips.info


Created using the [Ghost](http://ghost.org) framework


## Required packages

Go to https://nodejs.org/en/ and install the latest LTS package. 

Use `npm` to install the `ghost-cli`:

`npm install ghost-cli`

Install `wget` to scrape the static pages of ghost


## Install the ghost framework

Use the `ghost-cli` tool to create a local development site. In an empty folder run
`ghost-cli install local`. Head to the provided URL in your terminal -  http://localhost:2370/ghost/


## Pushing to github

You can only host HTML/CSS/JS files on github, so we will need to use `wget` to scrape the static pages. 

Create a docs folder inside the theme you are using. For this example, I am using the casper theme. Make sure you run the command below, in the casper folder:

`/current/content/themes/casper`

To verify the port number ghost is using, use `ghost ls`:

| Name  | Location  | Version  | Status  | URL  | Port  | Process Manager  |
|---|---|---|---|---|---|---|
| ghost-local-1  | ~/Documents/colephillips.info  | 3.35.5 | running (development) | http://localhost:2370/  | 2370  | local  |

`wget -r -nH -P docs -E -T 2 -np -k http://localhost:2370/`


After running the `wget` coommand, the docs folder will now have the static content for github. Copy the docs folder to your master branch


