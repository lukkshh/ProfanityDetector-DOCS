## Profanity Detector - v1

> Profanity Detector is a sophisticated tool designed to identify and flag Georgian swear words, regardless of whether they are written using Georgian script or transliterated into the Latin alphabet. it also can detect english swear words.

#### Base Url:
```http
GET https://profanity-detector.onrender.com
```

| Parameter | Type     | Description   |
| :-------- | :------- | :-------------|
| `text`    |`string`  | **Required**. |

#### Responses:

| Key       | Description   |
| :-------- | :-------------|
| `profanity_count` | `How Many Words Detected` |
| `profanity_list` | `List of found words` |
| `profanity_detected` | `Returns Boolean` |
| `text_length` | `Your Text Length` |
| `execution_time`    | `Detection time`  |

#### Endpoint:

```http
POST /api
```

#### Example Response Data:

```json
{
    "execution_time": 0, 
    "profanity_count": 0,
    "profanity_detected": false,
    "text_length": 1
}
```

#### Endpoint:

```http
POST /api/full-response
```

#### Example Response Data:

```json
{
    "execution_time": 0,
    "profanity_count": 0,
    "profanity_detected": false,
    "profanity_list": [],
    "text_length": 0
}
```

#### Example Javascript Code:

```javascript

const url = 'https://profanity-detector.onrender.com/api';

const postData = {
  text: 'Your text data here'
};

const options = {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json', 
  },
  body: JSON.stringify(postData), 
};

fetch(url, options)...

```
