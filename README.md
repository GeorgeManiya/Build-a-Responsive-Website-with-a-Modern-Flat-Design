# Build-a-Responsive-Website-with-a-Modern-Flat-Design

1. Install Node.js(https://nodejs.org/en/download/ -> Current -> ...) if it is not already on your machine.
Verify that you are running node version 0.4 or higher;
node -v in a terminal/console window. Older versions can produce errors.

2. Create App_Build folder in Web project. It should contains:
*r.js - js file that contains requirejs optimizer tool (can be downloaded from http://requirejs.org/docs/download.html);
*build-config.js - config file for requirejs optimizer;

3. Optimization tool starts after running "Path/to/App_Build/directory node r.js -o build-config.js" command in a terminal/console window. By the way you could add post-build event in project settings: 'if $(ConfigurationName) == Release node "$(ProjectDir)App_Build\r.js" -o "$(ProjectDir)App_Build\build-config.js"', that will runs command every time you build a project in release mode.

4. After executing optimization command, new directory will be created (js-build as an example). It will contains minimized version of basic js files. According to configuration in build-config.js some of the files can be bundled in one file (app.js as an example).
