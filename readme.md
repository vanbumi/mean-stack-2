# MEAN Stack Developer

** MongoDB, ExpressJS, AngularJS and NodeJS

## The Steps

Create new folder in your workspace folder

	mkdir myproject

Create new file named package.json under myproject folder, fill with this code:

	{
		"name": "mean-demo",
		"version": "0.0.1"
	}

Create new file named server.js and type bellow for test purpose:

	console.log("Hello form Node!");

Open your Terminal	navigate to folder myproject:

	$ cd myproject
	myproject$ node server

Hello form Node! will show up!

After that delete that and modified with real code bellow:

	var express = require("express");
	app	    = express();

	app.get("/", function(req, res) {
		res.sendfile(__dirname + '/client/views/index.html');
	});

	app.listen(3000, function() {
		console.log('I\'m Listening to.. ');
	});		 	

Install express

	npm install express --save	

* the reason --save is node will auto insert into file package.json, see below the change:

	{
		"name": "mean-demo",
	  	"version": "0.0.1",
	  	"dependencies": {
	    "express": "^4.13.4"
	  	}
	}

* and this command will install new folder named node_modules autmatically for us.

Create new folder client/views and new file index.html inside of views folder, and types simple html bellow:

	<html>
	<head>
		<meta charset="UTF-8">
		<title>Document</title>
	</head>
	<body>
		<h1>Hello Dyo!</h1>
	</body>
	</html>




