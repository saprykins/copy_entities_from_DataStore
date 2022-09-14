# copy_entities_from_DataStore
set the project
```
gcloud config set project ari-dp-***
```
export entities
```
gcloud datastore import --kinds="test" gs://tempo-bucket-datastore-exported/test/test.overall_export_metadata --async
```
import entities
