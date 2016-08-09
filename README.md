# json-to-md
Convert Json Schema to MarkDown

# using

Clone into folder modules

Use it like this:

```js
var parse = require('json-to-md')
var schema = // An object that is a valid JSON Schema
var markdown = parse(schema)
```
A JSON file:

```json
{
	"$schema": "http://example.com#",
	"title": "Example",
	"description": "This Json file.",
	"type": "object",
	"properties": {
		"price": {
			"description": "Testing.....",
			"type": "number"
		}
	}
}
```

The output would be:

```markdown
# Example Schema

This Json file.

The schema defines the following properties:

## `price` (number)

Testing.....
```
