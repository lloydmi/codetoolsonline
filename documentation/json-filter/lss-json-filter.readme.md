## Json Filtering
The filtering component will allow you to filter the JSON down to a specific object within the tree. When loading
the component it will calculate all of the possible elements that you can filter down to within the tree. 

### Usage

The functionality is available anywhere you see the filter icon. If the icon is present, it will be disabled
until there is data that can be filtered.

Once in the filter modal, you can either select the value from the dropdown or you can start to type in
key words to filter down the results using the dot notation. 

Using the below example, since you a can filter down to specific objects you would be able to enter either 
*Envelope*, *Envelope.Body* or *Envelope.Body.GetQuotation*. 

<img alt="JSON Filter" src="../images/json_filter.jpg?raw=true" /> 

```json
{
  "Envelope": {
    "Body": {
      "GetQuotation": {
        "QuotationsName": "Microsoft"
      }
    }
  }
}
``` 
 Choosing the option *Envelope.Body* the ending result will be:
 
 ```json
{
  "GetQuotation": {
    "QuotationsName": "Microsoft"
  }
}
```

*Tip*: You can also type in values and the system will filter the available options to the elements that
contain the input value. 

Using the same example, if you type in __Bo__ the selections will be filtered down to *Envelope.Body* and
*Envelope.Body.GetQuotation*.

<img alt="JSON Filter with Search" src="../images/json_filter_with_search.jpg?raw=true" />
