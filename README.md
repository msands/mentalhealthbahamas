# Mental Health Bahamas

This is the first version of the static website for [mentalhealthbahamas](https://mental-health-bahamas.firebaseapp.com) built using [Middleman](https://middlemanapp.com) static site generator.

## System Requirements
- Ruby
- Middlemanapp
- Firebase CLI tool

## Installation
- Clone the repo

```
    git clone git@github.com:msands/mentalhealthbahams.git
```

- Change into the repo's directory and install dependencies

```
cd mentalhealthbahamas
bundle update
```

- Make make code changes to files under the `source/` directory
- **Bonus step:** Commit your changes to git for version control
- When you are ready to push your code changes to production, first you use middleman to build the static site

```
bundle exec middleman build
```

- This will create the `build` directory, which contains everything that can be read by any platform which can serve a static website
- The platform that is in use here is Google's Firebase.  It allows for free static website hosting.  Since `firebase.json` is already configured, all you need to do is run `firebase deploy` and like magic, the site will be availabe at whatever the domain is set to in the [project_name](https://console.firebase.google.com/u/0/project/mental-health-bahamas/settings/general/) location, in this case [mental-health-bahamas.firebaseapp.com](https://mental-health-bahamas.firebaseapp.com).
	- Custom domains can be set [here](https://console.firebase.google.com/u/0/project/mental-health-bahamas/hosting/main)

## Work In Progress
- Contact form, using [formspree.io](https://formspree.io), doesn't appear to be working
- Create `rake` task to move the build and deploy process into one command
- Move entire dev environment to docker, which would make the only system requirement [Docker](https://docker.com