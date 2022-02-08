There are three places related to ROIs in DVID:

- native ROI data: each data instance of ROI type corresponds to one ROI
- keyvalue `rois`: keyvalues for indexing ROI data for 3D visualization in NeuTu. Each key will treated be as a ROI. The value has the following format
  ```
  {
    "->": {
      "type": "mesh" | "roi",
      "key": "roi key" # this should be the name of a ROI data instance if "type" is "roi"; otherwise, it should be a key in roi_data
    }
  }
  ```
- keyvalue `roi_data`: the place of storing precomputed ROI meshes. Each mesh is stored with a key, which might be accompanied with \<key\>_info to specify additional information such as mesh format. The default format is `obj`.

For example, a ROI named MB may have a ROI data instance named `MB`, and an `MB` key in the `rois` keyvalue data. Assuming the value is
`{"->": {"key": "d230e3669195ebd143d73b22011f8eec"}}`,
there should be a key `d230e3669195ebd143d73b22011f8eec` pointing to the actual mesh in the `roi_data` data instance.

