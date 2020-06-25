# - ![#1589F0](https://via.placeholder.com/15/1589F0/000000?text=+) `#1589F0`Url-Shortener 

### Url Shortener using Django and Graphql

## Quickstart

### For installing url shortener just create your virtual environment

``` pip insall virtualenv -p python3 ```

### Then active and install dependency from requirementx.txt

``` pip install -r requirements.txt ```

## Examples

### Then just run the app on localhost:8000/graphql and you can query like this

``` 
    query{
        urls {
            id
            fullUrl
            urlHash
            clicks
            createdAt
            }
        }

```
### if you want to create data

    mutation{
        createUrl(fullUrl:"your url"){
            url{
                id
                fullUrl
                urlHash
                clicks
                createdAt

            }
        }
    }

### your output will be like this

    {
        "data":{
            "createUrl": {
                "url":  {
                    "id": "id",
                    "fullUrl": "your URL",
                    "urlHash": "shorted url",
                    "clicks": "how many time its been clicked",
                    "createdAt":"create at time"
                }
            }
        }
    }
