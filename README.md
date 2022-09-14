# copy_entities_from_DataStore
set the project
```
gcloud config set project ari-dp-***
```
export entities (need to create a folder for each entity)
```
gcloud datastore export --kinds="test" gs://tempo_storage_bucket_for_ds_export/folder
```
```
gcloud datastore export --kinds="data_transcoding" gs://tempo-bucket-datastore-exported/data_transcoding
gcloud datastore export --kinds="extenda-edmsalesreceipt" gs://tempo-bucket-datastore-exported/extenda-edmsalesreceipt
gcloud datastore export --kinds="sales_transcoding" gs://tempo-bucket-datastore-exported/sales_transcoding
```

import entities
```
gcloud datastore import --kinds="test" gs://tempo-bucket-datastore-exported/test/test.overall_export_metadata --async
```
