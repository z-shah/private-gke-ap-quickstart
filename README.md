### Deploy a sample app to private gke autopilot cluster

__Prequisites__

1. Enable necessary APIs [refer](https://cloud.google.com/deploy/docs/integrating-ci#before_you_begin)

1. Define and register Cloud Deploy Delivery pipeline and targets

``` 
gcloud deploy apply --file=clouddeploy.yaml --region=australia-southeast1

gcloud deploy apply --file=target-test.yaml --region=australia-southeast1

gcloud deploy apply --file=target-staging.yaml --region=australia-southeast1

gcloud deploy apply --file=target-prod.yaml --region=australia-southeast1
```

