
> W3.JS is a JavaScript library designed to simplify web development projects


## tl;dr

If you want to display a large json object, you can use the `w3-repeat` attribute
in combination with `displayObject()`

```
<table id="id01">
  <tr w3-repeat="customers">
    <td>{{CustomerName}}</td>
    <td>{{City}}</td>
    <td>{{Country}}</td>
  </tr>
</table>

<script>
  w3.displayObject("id01", {
      "customers":[
        {"CustomerName" : "Alfreds Futterkiste","City" : "Berlin","Country" : "Germany"},
        {"CustomerName" : "Berglunds snabbköp","City" : "Luleå","Country" : "Sweden"},
        {"CustomerName" : "Centro comercial Moctezuma","City" : "México D.F.","Country" : "Mexico"}
      ]});
</script>
```

But it only works for flat objects. You cant use something like `{{Customer.Address.Zip}}`.
That is the reason for this fork.

## JSONPath

XPath is a language for addressing parts of an XML document. It has a [specification at w3c](https://www.w3.org/TR/xpath/all/).

JSONPath is the same for json, but it doesn't have a real specification. Most of the references goes to a 
[Stefan Goessner article](https://goessner.net/articles/JsonPath/).

He points to this implementation: [jsonpath - code.google.com](https://code.google.com/archive/p/jsonpath/)
If you go to its [download](https://code.google.com/archive/p/jsonpath/downloads) page you can find the **0.8.0** version: [jsonpath-0.8.0.js](https://storage.googleapis.com/google-code-archive-downloads/v2/code.google.com/jsonpath/jsonpath-0.8.0.js.txt)

However I found a more recent version in [GH - MikeRalphson/jsonpath](https://github.com/MikeRalphson/jsonpath): 0.8.5 verion: [jsonpath.js](https://raw.githubusercontent.com/MikeRalphson/jsonpath/master/src/js/jsonpath.js)


## References

- [JSONPath Online Evaluator](https://jsonpath.com/)

