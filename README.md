### Deploy a sample app to private gke autopilot cluster

__Prequisites__

1. Enable necessary APIs [refer](https://cloud.google.com/deploy/docs/integrating-ci#before_you_begin)

1. Delivery pipeline defined and registered.

``` 
gcloud deploy apply --file=clouddeploy.yaml --region=australia-southeast1
```


#### Setting upconnect gateway

1. Enable APIs [doco](hhttps://cloud.google.com/anthos/multicluster-management/gateway/setup#enable_apis)

1. Register your cluser with workload identity (recommended) [docs](https://cloud.google.com/anthos/fleet-management/docs/register/gke#register_your_cluster)


```
gcloud container fleet memberships register ap-private-cluster         \                                            
 --gke-cluster="australia-southeast1/ap-private-cluster"         \
 --enable-workload-identity
 ```

1. Grant IAM roles to users/SA [refer docs](https://cloud.google.com/anthos/multicluster-management/gateway/setup#grant_iam_roles_to_users)

