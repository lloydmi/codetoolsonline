# Xml to Json
Convert an XML string into a JSON object using desired configurations, sorting and filtering. 

![Xml to Json](../images/xml-to-json/xml_to_json.jpg?raw=true) 

### Convert JSON to Camel Case
When selected, it will convert the property name from the XML element into a Camel Cased JSON object property.
For example, when checked it will convert *SoapEnvelope* to *soapEnvelope*.

### Treat empty nodes as null
Currently the conversion does not validate the properties are the same across each object, so an empty XML
node will be treated as an empty string (assuming it doesn't have a *nil* attribute on it). To get around
this limitation, check the box and any empty node will be set to null. 

### Include Attributes
When selected, the system will place any attributes on the an XML node as a property on the JSON object. It
will be prefixed with the value entered in the *Attribute Prefix* input. An example of what that might look
like is:

```xml
<breakfast_menu>
     <food id="1">
          <name>Belgian Waffles</name>
          <price>$5.95</price>
          <description>Two of our famous Belgian Waffles with plenty of real maple syrup</description>
          <calories>650</calories>
     </food>
</breakfast_menu>
```
```json
{
  "breakfast_menu": {
    "food": {
      "@id": "1",
      "name": "Belgian Waffles",
      "price": "$5.95",
      "description": "Two of our famous Belgian Waffles with plenty of real maple syrup",
      "calories": "650"
    }
  }
}
```

### Attribute Prefix
The prefix that will be appended to any attribute found on the XML node. This is ignored unless the checkbox
above is selected.

*Tip*: If you need the attribute on your object, but without the prefix leave the field blank and it will use
an empty string as the prefix.

### Indentation Level
The number of spaces that you want to have for each level of indentation on the properties of the JSON object.

### Additional Documentation
See the additional documentation for the functionality details of shared components.

* [Sorting](../json-sort/lss-json-sort.readme.md)
* [Filtering](../json-filter/lss-json-filter.readme.md)
* [Copy to Clipboard](../copy-to-clipboard/lss-copy-to-clipboard.readme.md)
