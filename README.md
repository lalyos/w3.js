> [W3.JS](https://www.w3schools.com/w3js/default.asp) is a JavaScript library designed to simplify web development projects

It has a nice [displayObject](https://www.w3schools.com/w3js/w3js_display.asp) function,
but it lacks proper JSONPath support. I've combined `w3.js` and `jsonpath.js` 
with a minimal glue function into a single file.

## Usage

Add inside the html `<head>`:
```
<script src="https://raw.githubusercontent.com/lalyos/w3.js/master/w3.js"></script>
```

Or if you run into `Cross-Origin Read Blocking (CORB)`, then use this:
```
<script src="https://yacdn.org/serve/https://raw.githubusercontent.com/lalyos/w3.js/master/w3.js"></script>
```

Now you can use `displayObject()` with an array of complex objects:
```
  <table class="w3-table-all" id="table1" >
    <tr w3-repeat="person in people">
      <td>{{person.name}}</td>
      <td>{{person.age}}</td>
      <td>{{person.address.city}}</td>
    </tr>
  </table>
  <script>    
      w3.displayObject("table1", {"people": [
        {"name": "Karl", "age": 32, "address": {"city":"London", "zip":"NX3AZ"} },
        {"name": "Katrin", "age": 28, "address": {"city":"Berlin", "zip":"9999"} },
        {"name": "Bob", "age": 77, "address": {"city":"Texas", "zip":"5555"} }
      ]});
  </script>
```

See live exampe above [gh-pages](https://lalyos.github.io/w3.js/)

## JSONPath

XPath is a language for addressing parts of an XML document. It has a [specification at w3c](https://www.w3.org/TR/xpath/all/).

JSONPath is the same for json, but it doesn't have a real specification. Most of the references goes to a 
[Stefan Goessner article](https://goessner.net/articles/JsonPath/).

He points to this implementation: [jsonpath - code.google.com](https://code.google.com/archive/p/jsonpath/)
If you go to its [download](https://code.google.com/archive/p/jsonpath/downloads) page you can find the **0.8.0** version: [jsonpath-0.8.0.js](https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/jsonpath/jsonpath-0.8.0.js.txt)

However I found a more recent version in [GH - MikeRalphson/jsonpath](https://github.com/MikeRalphson/jsonpath): 0.8.5 verion: [jsonpath.js](https://raw.githubusercontent.com/MikeRalphson/jsonpath/master/src/js/jsonpath.js)


## References

- [JSONPath Online Evaluator](https://jsonpath.com/)

