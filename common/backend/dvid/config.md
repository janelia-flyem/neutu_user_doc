# User Status

The user status configuration is used to determine the status of a user, such as if the user has admin privilege. It is a json object stored in `<dvid_base_url>/api/node/<uuid>/neutu_config/key/user_status`, such as

```
{ "admin": [ "user1", "user2" ] }
```

# Body Status

The predefined options of the body status can be configured in  `<dvid_base_url>/api/node/<uuid>/neutu_config/key/body_status_v2`, which hosts a JSON object, such as

```
{
  "status": [
    {
      "protection": 8,
      "priority": 10,
      "name": "Traced",
      "expert": true,
      "final": false,
      "preserving_id": true,
      "admin_level": 1
    },
    {
      "protection": 8,
      "priority": 30,
      "name": "Roughly traced",
      "expert": true,
      "final": false,
      "preserving_id": true,
      "admin_level": 1
    },
    {
      "protection": 8,
      "priority": 35,
      "name": "RT Orphan",
      "expert": false,
      "final": false
    },
    {
      "protection": 0,
      "priority": 40,
      "name": "Prelim Roughly traced",
      "expert": false,
      "final": false
    }
  ],
  "conflict": [
    ["roughly traced", "prelim roughly traced"]
  ]
}
```

# Body Annotation Dialog

A body annotation dialog can be customized by configuration saved in DVID. NeuTu/Neu3 looks for the configuration at `<dvid_base_url>/api/node/<uuid>/<segmentation>_annotations/key/schema`. It is a JSON object that has the same format as used in Clio.

Here is a simple example of the configuration:

```
{
  "collection": {
    "status": {
      "title": "status",
      "rank": 80,
      "filterEnabled": true,
      "editElement": {
        "type": "select"
      }
    },
    "instance": {
      "rank": 5,
      "editElement": {
        "type": "input"
      },
      "title": "instance",
      "filterEnabled": true
    },
    "type": {
      "rank": 8,
      "editElement": {
        "type": "input"
      },
      "title": "type",
      "filterEnabled": true
    }
  },
  "shape": [
    "instance",
    "status",
    "type"
  ]
}
```

In this example, the `status` field is set to be an option box without a list of predefined options there. This is because `status` is a special field that is linked to the body status configuration, which provides the predefined options for the `status` field.