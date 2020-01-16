# Lighting-Test
### Testing Lighting setup

#### Setup: 
git clone git@github.com:WebPlatformForEmbedded/Lightning-SDK-blueprint.git {YOUR_APP_NAME}

cd {YOUR_APP_NAME}

git remote set-url origin {YOUR_REPOSITORY_URL}

Create a new empty git repo on the specified origin url

Set name and identifier in metadata.json.

git commit -anm "init app"
git push origin master
npm install
Now please check if you can run index.html (using a web server or your IDE). If it works you're set up and ready to start building your app!

If you don't have a web server installed you could run instant-server from the directory:

sudo npm install -g instant-server

instant -p 8081 ./ 

#### Developing apps
When developing an app on the Lightning SDK, instead of extending lng.Application, extends ux.Apps. This brings some additional features such as automated font loading and relative paths.

Notice that the SDK provides additional features such as a mediaplayer implementation, a generic video player UI, generic keyboard and some other components. For now please use the force and read the source.

#### Building app distribution
Use the following steps to create a distribution:

Create a self-contained web-based distribution (HTML5) in dist/web: npm run release-web

Create a Metrological platform package in dist/{appname}.mpkg.tgz: npm run release-mpkg
