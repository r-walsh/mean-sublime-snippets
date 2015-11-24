# mean-sublime-snippets

###A set of Sublime Snippets to avoid boilerplate MEAN Stack code.

##Usage
Download and unpack the zip or clone this repository into your sublime settings directory. On a Mac it will be something like `~/Library/Application Support/Sublime Text 3/Packages/User`. Now inside of every JS file you will have access to these snippets. To use them you simply need to type the shortcut and hit your tab key.

___

Shortcuts (Note that you can tab through the different `$num`'s to make the necessary changes):

- `ngApp`:
```javascript
angular.module('$1', [$2]);
```

- `ngAppRoute`:
```javascript
angular.module('$1', ['ui-router'$2])

.config(function( $stateProvider, $urlRouterProvider ) {

	$urlRouterProvider.otherwise('/');
	
	$stateProvider
	.state('$3', {
		url: '$4',
		templateUrl: '$5',
		controller: '$6'
	})

});
```

- `ngCtrl`:
```javascript
angular.module('$1')
.controller('$2', function( $scope ) {
	
	$3

});
```

- `ngSrvc`:
```javascript
angular.module('$1')
.service('$2', function() {

	$3

});
```

- `ngFac`:
```javascript
angular.module('$1')
.factory('$2', function() {
	return {

		$3

	}
});
```

- `ngDir`:
```javascript
angular.module('$1')
.directive('$2', function() {
	return {

		$3

	}
});
```

- `node`:
```javascript
var   express = require('express')
	, app = express()
	, bodyParser = require('body-parser')
	, cors = require('cors')
	, mongoose = require('mongoose')
	, port = $1
	, mongoUri = 'mongodb:localhost:27017/$2';

app.use(bodyParser.json());
app.use(cors());
app.use(express.static(__dirname + '/public'));

mongoose.connect(mongoUri);
mongoose.connection.once('open', function() {
	console.log('Connected to MongoDB at ' + mongoUri);
});


app.listen(port, function() {
	console.log('Listening on ' + port)
});
```

- `ifErr`:
```javascript
if (err) {
	return res.status(500).send(err);
}

$1
```

___

Hopefully you find these helpful! I encourage you to modify these or create your own for whatever suits your purposes best. Pull requests are always welcome if you see something that needs changing.
