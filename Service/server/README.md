## Similar Properties API
<hr />

### Get similar properties info
  * GET `/properties/:id/similarHomes`

**Path Parameters:**
  * `id` property id

**Success Status Code:** `200`

**Returns:** JSON

```json
    "[
      {
        "id": "Number",
        "location": "String",
        "rating": "Number",
        "property_type": "String",
        "bed_num": "Number",
        "description": "String",
        "price_per_night": "Number",
        "img_src": "[ "String" ]"
      },
      ...
    ]"
```
<hr />

### Add property
  * POST `/properties/createProperty`

**Success Status Code:** `201`

**Request Body**: Expects JSON with the following keys.

```json
    {
      "location": "String",
      "rating": "Number",
      "property_type": "String",
      "bed_num": "Number",
      "description": "String",
      "price_per_night": "Number",
      "img_src": [ "String" ]
    }
```
**Success Status Code:** `201`
<hr />

### Update property info
  * PATCH `/properties/:id`

**Path Parameters:**
  * `id` property id

**Success Status Code:** `204`

**Request Body**: Expects JSON with any of the following keys (includes only keys to be updated)

```json
    {
      "rating": "Number",
      "description": "String",
      "price_per_night": "Number",
      "img_src": [ "String" ]
    }
```
<hr />

### Delete property
  * DELETE `/properties/:id`

**Path Parameters:**
  * `id` property id

**Success Status Code:** `204`
<hr />
