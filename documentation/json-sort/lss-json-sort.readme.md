## Json Sorting
The sorting component allows you to filter the properties on the object and sort any arrays by a property that
exists on the an object within the array. If the array only contains primitive values, it will allow you to
sort the elements within the array as well. 

### Usage
 
The functionality is available anywhere you see the sorting icon. If the icon is present, it will be disabled
unless there is data that can be filtered.

Once within the Sort Modal, you will be provided with different sorting options based on the information
within the object sorting. 

#### Sort Direction
The direction in which the properties on each object will be sorted. The system will go through nested
objects and sort the properties on each based on this selection. 

#### Sort Primitive Arrays
The direction in which to sort arrays that only contain primitive values such as numbers or strings. The
direction selected in the __Sort Direction__ section will apply to the sorting of the primitive arrays
if this value is selected.

#### Array Object Sorting
For each array of objects found within the request, you can choose what property or properties on the 
object to sort by and select the direction for each attribute. 

An example object will create the sort options shown in the image below. 

```json
{
  "catalog": {
    "books": {
      "book": [
        {
          "author": "1",
          "title": "XML Developer's Guide",
          "genre": "Computer",
          "price": "44.95",
          "publish_date": "2000-10-01"
        },
        {
          "author": "2",
          "title": "Midnight Rain",
          "genre": "Fantasy",
          "price": "5.95",
          "publish_date": "2000-12-16"
        },
        {
          "author": "3",
          "title": "Maeve Ascendant",
          "genre": "Fantasy",
          "price": "5.95",
          "publish_date": "2000-11-17"
        }
      ]
    },
    "authors": {
      "author": [
        {
          "name": "Gambardella, Matthew",
          "id": "1"
        },
        {
          "name": "Ralls, Kim",
          "id": "2"
        },
        {
          "name": "Corets, Eva",
          "id": "3"
        }
      ]
    }
  }
}
```

<img alt="JSON Sort Modal" src="../images/json_complex_array_sort.jpg?raw=true" />
