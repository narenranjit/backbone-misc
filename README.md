backbone-misc
=============

Miscellaneous Backbone Models with random utilities thrown in

# BaseComputedModel.js

This lets you have computed properties in Backbone.

```javascript
	var myModel = BaseComputedModel.extend({
		defaults: {
			firstName: "John",
			lastName: "Smith",

			fullName: function(){
					return this.get("John") + this.get("Smith");
			}
		}
	});

	console.log(myModel.get("fullName")); //Print John Smith
	myModel.set("firstName",  "Jane");
	console.log(myModel.get("fullName")); //Print Jane Smith
```

You can also bind on computed properties, and pretty much just treat it like you would any other property
```javascript
	myModel.on("change:fullName", function(){
		console.log("Full name changed");

	});
```

#TODO:

Add tests