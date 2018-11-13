# Important
Here is a bug is happining in verdaccio, that means this project is not usable for now. That is here [404 not found](https://github.com/verdaccio/verdaccio/issues/1085)

## Verdaccio dockerized example

To start the server
- Rename env.config.yaml to config.yaml in the conf folder
- Change the uplinks -> mDefault -> url paramater for your server in config.yaml file.
- docker-compose up


3 user already added(sytax: username:password)
- admin:admin
- aliduru:aliduru
- velidurmaz:velidurmaz

In this solution you can add a new user only manually. There are some tools you can create a new user for htpasswd syntax, for example: 
- http://www.htaccesstools.com/htpasswd-generator/

Create a new user this the tool, open conf/htpasswd file, add a new line and paste that what the tool is created

>Note: 
You can add a new user while server is on, the server can detect that. But when you delete a user from htpasswd, the server cannot handle that(if the user is logged in once), I think it calls the user from cache, you have to restart the server.



## Verdaccio usage

- If you are not installing to your localhost, DO NOT `npm set registry http://localhost:4873/`
- To login `npm login --registry=http://localhost:4873/`
- To logout `npm logout --registry=http://localhost:4873/`
- To check whoami  `npm whoami --registry=http://localhost:4873/`
- To publish a libary `npm publish --registry=http://localhost:4873/`
- To add a library from verdaccio `npm install --registry=http://localhost:4873/`



## License & copyright

© Ahmet Feyzullah Yıldız

Licensed under the [MIT License](LICENSE)
