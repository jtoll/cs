# Node.js

#### Global packages

List all global packages

    npm list -g --depth=0  

Find global packages that need to be updated

    npm outdated -g --depth=0  

Update a single global package

    [sudo] npm install -g <package>  

Update all global packages

    [sudo] npm update -g  

#### Local Packages

Updating local packages is essentially the same as updating global packages, except the `-g` flag is not used, nor `sudo`.  Packages are installed into the `node_modules` subdirectory of the current directory.

#### References
<https://nodejs.org>  
<https://www.npmjs.com/>  
<https://docs.npmjs.com/getting-started/updating-global-packages>  
<https://docs.npmjs.com/getting-started/updating-local-packages>  
<https://docs.npmjs.com/files/folders>  
