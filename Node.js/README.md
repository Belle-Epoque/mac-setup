# Node.js

Install [Node.js](http://nodejs.org/) with Homebrew:

    $ brew update
    $ brew install node

Node modules are installed locally in the `node_modules` folder of each project by default, but there are at least two that are worth installing globally. Those are [CoffeeScript](http://coffeescript.org/) and [Grunt](http://gruntjs.com/):

    $ npm install -g coffee-script
    $ npm install -g grunt-cli

### Npm usage

To install a package:

    $ npm install <package> # Install locally
    $ npm install -g <package> # Install globally

To install a package and save it in your project's `package.json` file:

    $ npm install <package> --save

To see what's installed:

    $ npm list # Local
    $ npm list -g # Global

To find outdated packages (locally or globally):

    $ npm outdated [-g]

To upgrade all or a particular package:

    $ npm update [<package>]

To uninstall a package:

    $ npm uninstall <package>
    

### Fix bug with node/npm install

    $ brew update
    $ brew doctor
    
Try to create symlink

    $ brew link --overwrite node

You have to fix permission access

    $ sudo chown -R $USER /usr/local/etc
    $ sudo chown -R $USER /usr/local/lib
    $ sudo chown -R $USER /usr/local/share
    $ sudo chown -R $USER /usr/local
    
Reinstall node

    $ export PATH="/usr/local/bin:$PATH"
    $ brew install node
    $ brew postinstall node
