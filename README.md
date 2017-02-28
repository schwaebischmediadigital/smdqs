# smdQS
A minimalistic javascript wrapper for the jquery babied...

Changes:

some day 2015	- 1.0: 		Initial version
28.02.2017 	- 2.0-testing:	new structure and two new functions: requreJS and ready

Examples:

- ajax() call:
``` js
smdQS().ajax("/testscript.php", function( returnData ) {
	console.log(returnData);					
}
```

- ready() - Execute something on document ready:
``` js
smdQS().ready(function() {
	console.log("document is ready");					
}
```

- requireJS() - load an other js:
``` js
smdQS().requireJS("/js/somejsfile.js", function() {
	console.log("js file is loaded.");					
}
```

- working with classes and selectors:
``` js
var myNode = smdQS("#idOfMyNode");
if (myNode.hasClass("aNiceClass")) {
	myNode.removeClass("aNiceClass");
}
```

- working with lists of nodes:
``` js
var aListOfNodes = smdQS(".btn");
if (aListOfNodes.isDomObject && aListOfNodes.isList) {
	aListOfNodes.forEach(function(index, oneOfThisNodes) 
	{
		oneOfThisNodes.removeAttribute("onclick");
		oneOfThisNodes.addEventListener("click", function() 
		{
			console.log("You have clicked on the button with the index " + index);
		});
	});
} 
```


This version includes a forked version of docReady (https://github.com/jfriend00/docReady)

Matthias Weiß / Schwäbisch Media Digital
