# json-to-md
Convert Json Schema to MarkDown

using

Clone into folder module

Use it like this:

var parse = require('json-to-md')
var schema = // An object that is a valid JSON Schema
var markdown = parse(schema)
There are plenty of examples in the test folder, but a very simple example would be as follows:

For a JSON file like this:

{
    "$schema": "http://example.com#",
    "title": "Example",
    "description": "Testing Script.",
    "type": "object",
    "properties": {
        "price": {
            "description": "Testing.....",
            "type": "number"
        }
    }
}
The output would be:

# Example Schema

Testing Script.

The schema defines the following properties:

## `price` (number)

Testing.....
