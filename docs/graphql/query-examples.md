### Basics
Query:
```graphql
{books}
```
Responce:
```graphql
{
  "errors": [
    {
      "message": "`books` is an object, interface or union type field. Leaf selections on objects, interfaces, and unions without subfields are disallowed.",
      "locations": [
        {
          "line": 1,
          "column": 2
        }
      ],
      "extensions": {
        "declaringType": "Query",
        "field": "books",
        "type": "[Book!]!",
        "responseName": "books",
        "specifiedBy": "http://spec.graphql.org/October2021/#sec-Field-Selections-on-Objects-Interfaces-and-Unions-Types"
      }
    }
  ]
}
```
Does not query ab object.
