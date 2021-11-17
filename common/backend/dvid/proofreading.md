NeuTu/Neu3 will try to create the following data instances while loading a dataset to be proofread:

| Data Instance | Type | Description | Can Rename |
| ------------- | ---- | ----------- | ------------- |
| bookmark_annotations | annotation | User-scope bookmarks | N |
| \<BODY\>_todo | annotation | Todo bookmarks shared among users | Y |
| \<BODY\>_skeletons | keyvalue | Body skeletons | N |
| \<BODY\>_thumbnails | keyvalue | (OBSOLETE) | N |
| bookmarks | keyvalue | Additional bookmark information (mainly used to record if a bookmark is checked) | N |
| \<BODY\>_annotations | keyvalue | User-scope annotations | N |
| \<BODY\>_annotations | keyvalue | Body annotations | N |
| \<BODY\>_splits | keyvalue | Split labels | N |

