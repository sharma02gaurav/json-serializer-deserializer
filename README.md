# JSON Serializer Deserialize

<i>JSON serializer deserialize</i> makes the Read/Write operations on the JSON files easily. The applications employing the config files in JSON could utilize this plugin by simply importing the module and avoiding interating with the `fs` module. Focus only on reading, updating and saving the JSON. 

> Now support for typescript. prior updates to 1.0.2

## Installation
1. Run the following command to install<br/>`npm install json-serialize-deserialize`.


## Usage and snippets
    var jsonSerializer = require('json-serialize-deserialize');
	jsonSerializer.readFile ('path.to.config.json')
		.then ((fileData) => {
			// do something with the filedata

			fileData.revenue = 9809;

			jsonSerializer.writeFile ('path.to.config.json')
				.then ((val) => {
					console.log ('write success')
				}).catch ((err) => {
					console.error (err);
				})
		}).catch ((err) => {
			console.error (err);
		});