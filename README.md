# Songs-Recommendation-Engine
A Simple Songs Recommendation Engine Using ELK Stack, GCP and C#

<img src="https://static-www.elastic.co/v3/assets/bltefdd0b53724fa2ce/blt52c29462320a5d1e/5ea8c7efea2a04243200ce24/brand-elastic-horizontal-220x130.svg">

<img src="https://img.shields.io/badge/Deployment-Healthy-brightgreen"> <img src="https://img.shields.io/badge/Active%20Clusters-3-brightgreen">

# Elastic Stack Configuration
- ```Cloud Provider``` : ```GCP``` <br>
- ```Region``` : ```IN Mumbai (asia-south-1)``` <br>
- ```Harware Profile``` : ```I/O Optimized``` <br>
- ```Version``` : ```7.13.1```
- ```Deployment Name``` : ```Songs-Recommendation-Engine```
<br>
<img src="https://raw.githubusercontent.com/tushar821999/Songs-Recommendation-Engine/ELK-Stack-Deployment/Architecture.PNG">

# Default End Points

```Get : https://songs-recommendation-engine.es.asia-south1.gcp.elastic-cloud.com:9243/```
```
{
  "name" : "instance-0000000001",
  "cluster_name" : "6c3c430ff53a464d89a857721103e479",
  "cluster_uuid" : "omrlndeKR9-jTus0taUNiA",
  "version" : {
    "number" : "7.13.1",
    "build_flavor" : "default",
    "build_type" : "docker",
    "build_hash" : "9a7758028e4ea59bcab41c12004603c5a7dd84a9",
    "build_date" : "2021-05-28T17:40:59.346932922Z",
    "build_snapshot" : false,
    "lucene_version" : "8.8.2",
    "minimum_wire_compatibility_version" : "6.8.0",
    "minimum_index_compatibility_version" : "6.0.0-beta1"
  },
  "tagline" : "You Know, for Search"
}
```
```Get : https://songs-recommendation-engine.es.asia-south1.gcp.elastic-cloud.com:9243/_cat/indices```
```
green open .kibana_task_manager_7.13.1_001           7bTFAX1FTNybnZaOSKSPcA 1 1   11 479 449.8kb 287.2kb
green open apm-7.13.1-span-000001                    0F718AoLSSiWFQ2qA4Dorg 1 1    0   0    416b    208b
green open apm-7.13.1-onboarding-2021.06.06          B0t_35fQQtajt3FjQ9JrMg 1 1    1   0  14.9kb   7.4kb
green open .transform-internal-007                   bUuNv8I0ToWNdNr1qpzj0w 1 1    3   0  51.6kb  25.8kb
green open .fleet-agents-7                           0gb2EIWOTyq7XQS03Fw1Gg 1 1    1  50 678.7kb   409kb
green open .fleet-enrollment-api-keys-7              u3enK5ykR8KVgWmu2poKsQ 1 1    2   0  23.3kb  11.6kb
green open apm-7.13.1-transaction-000001             P4ZaGBEYRf6fTqfSNfPQuA 1 1    0   0    416b    208b
green open .apm-agent-configuration                  crgyZawPRSGiPPTopvBwMw 1 1    0   0    416b    208b
green open .kibana-event-log-7.13.1-000001           l_7t4q9eQteioCFDq4F2Xg 1 1    1   0  11.2kb   5.6kb
green open .fleet-servers-7                          tw_mTsImRkuE-kbWRTqU3g 1 1    1  75 119.6kb  48.6kb
green open .fleet-policies-leader-7                  PCmjllx3QPKfUOMLKE5CNQ 1 1    2 138 111.8kb  68.1kb
green open metrics-endpoint.metadata_current_default MO8Bek0ASqKqttVNgoN8FA 1 1    0   0    416b    208b
green open apm-7.13.1-metric-000001                  _ufuCOYRSNO29Yj9FRjKfw 1 1    0   0    416b    208b
green open .security-tokens-7                        M6PwU9feTJS_1Gtxx1pCuA 1 1    3   0  79.3kb  39.6kb
green open .security-7                               QPcgaCrOR96JGFuFBmRiKQ 1 1   64   1 378.7kb 189.5kb
green open apm-7.13.1-profile-000001                 weLymdWCT3OiuvHnf1WvxQ 1 1    0   0    416b    208b
green open .apm-custom-link                          brvZ583EQbmec0QLVhPl-w 1 1    0   0    416b    208b
green open apm-7.13.1-error-000001                   UFbIBHgJSA-VDATawjf0cg 1 1    0   0    416b    208b
green open .kibana_7.13.1_001                        K1HqOvu2TY2M1VchxY02ng 1 1 1413   3   8.9mb   4.4mb
green open .fleet-policies-7                         vObLtbdRSNOe_AIHV83hkg 1 1    5   0  54.2kb  27.1kb
```
