Connection validation is a protocol for proofreading synapses. The protocol object consists of metadata and a list of points, for example

```
{
  "date": "2020-02-14 02:49:26.106817",
  "file type": "connection validation",
  "username": "flyem",
  "software": "NeuTu",
  "coordinate system": "neuprint",
  "file version": 1,
  "points": [
    [
      1117,
      982,
      1024
    ],
    [
      1117,
      974,
      1023
    ]
  ]
}
```

Each point is supposed to be coordinates of a synaptic element. In DVID, the protocol is stored in `<dvid_address>/api/node/<uuid>/NeuTu-Protocols/key/<user>-connection_validation-<protocol_identifier>[-complete]`.

