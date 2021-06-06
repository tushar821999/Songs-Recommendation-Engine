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

- ```Get (Fetch All Indices) : https://songs-recommendation-engine.es.asia-south1.gcp.elastic-cloud.com:9243/_cat/indices```
```
green open .kibana_task_manager_7.13.1_001           7bTFAX1FTNybnZaOSKSPcA 1 1   11 422 757.6kb 307.7kb
green open apm-7.13.1-span-000001                    0F718AoLSSiWFQ2qA4Dorg 1 1    0   0    416b    208b
green open apm-7.13.1-onboarding-2021.06.06          B0t_35fQQtajt3FjQ9JrMg 1 1    1   0  14.9kb   7.4kb
green open .transform-internal-007                   bUuNv8I0ToWNdNr1qpzj0w 1 1    3   0  51.6kb  25.8kb
green open .fleet-enrollment-api-keys-7              u3enK5ykR8KVgWmu2poKsQ 1 1    2   0  23.3kb  11.6kb
green open .fleet-agents-7                           0gb2EIWOTyq7XQS03Fw1Gg 1 1    1  17 469.4kb 274.6kb
green open apm-7.13.1-transaction-000001             P4ZaGBEYRf6fTqfSNfPQuA 1 1    0   0    416b    208b
green open .apm-agent-configuration                  crgyZawPRSGiPPTopvBwMw 1 1    0   0    416b    208b
green open .kibana-event-log-7.13.1-000001           l_7t4q9eQteioCFDq4F2Xg 1 1    1   0  11.2kb   5.6kb
green open .fleet-servers-7                          tw_mTsImRkuE-kbWRTqU3g 1 1    1  82 117.2kb  37.1kb
green open .fleet-policies-leader-7                  PCmjllx3QPKfUOMLKE5CNQ 1 1    2 120 163.2kb    90kb
green open apm-7.13.1-metric-000001                  _ufuCOYRSNO29Yj9FRjKfw 1 1    0   0    416b    208b
green open .security-tokens-7                        M6PwU9feTJS_1Gtxx1pCuA 1 1    7   0   152kb  69.7kb
green open metrics-endpoint.metadata_current_default MO8Bek0ASqKqttVNgoN8FA 1 1    0   0    416b    208b
green open .security-7                               QPcgaCrOR96JGFuFBmRiKQ 1 1   64   1 378.7kb 189.5kb
green open apm-7.13.1-profile-000001                 weLymdWCT3OiuvHnf1WvxQ 1 1    0   0    416b    208b
green open .apm-custom-link                          brvZ583EQbmec0QLVhPl-w 1 1    0   0    416b    208b
green open apm-7.13.1-error-000001                   UFbIBHgJSA-VDATawjf0cg 1 1    0   0    416b    208b
green open songs                                     BsCsW9RzT0qh14Ufc9DP4A 1 1 2420   0 666.4kb 333.2kb
green open .kibana_7.13.1_001                        K1HqOvu2TY2M1VchxY02ng 1 1 1429  15   8.9mb   4.4mb
green open .async-search                             2yiXA0VPRQmeNIRXOCyGGA 1 1    0   1   6.6kb   3.3kb
green open .fleet-policies-7                         vObLtbdRSNOe_AIHV83hkg 1 1    5   0  54.2kb  27.1kb

```
- ```Get (Schema of songs index) : https://songs-recommendation-engine.es.asia-south1.gcp.elastic-cloud.com:9243/songs/```
```
{
    "songs": {
        "aliases": {},
        "mappings": {
            "_meta": {
                "created_by": "file-data-visualizer"
            },
            "properties": {
                "Artist-Name": {
                    "type": "text"
                },
                "Genere": {
                    "type": "keyword"
                },
                "Id": {
                    "type": "long"
                },
                "Movie-Name": {
                    "type": "text"
                },
                "Song-Name": {
                    "type": "text"
                },
                "User-Rating": {
                    "type": "keyword"
                }
            }
        },
        "settings": {
            "index": {
                "routing": {
                    "allocation": {
                        "include": {
                            "_tier_preference": "data_content"
                        }
                    }
                },
                "number_of_shards": "1",
                "provided_name": "songs",
                "creation_date": "1622957505480",
                "number_of_replicas": "1",
                "uuid": "BsCsW9RzT0qh14Ufc9DP4A",
                "version": {
                    "created": "7130199"
                }
            }
        }
    }
}
```
- ```Get (Fetch all songs) : https://songs-recommendation-engine.es.asia-south1.gcp.elastic-cloud.com:9243/songs/_search```
```
{
    "took": 2,
    "timed_out": false,
    "_shards": {
        "total": 1,
        "successful": 1,
        "skipped": 0,
        "failed": 0
    },
    "hits": {
        "total": {
            "value": 2420,
            "relation": "eq"
        },
        "max_score": 1.0,
        "hits": [
            {
                "_index": "songs",
                "_type": "_doc",
                "_id": "SpnO33kBmj9ei9SmPR7j",
                "_score": 1.0,
                "_source": {
                    "Artist-Name": "Kumar Sanu, Mika Singh, Neha Kakkar",
                    "Song-Name": "Aankh Marey",
                    "Genere": "BollywoodDance",
                    "User-Rating": "8.8/10",
                    "Id": 1,
                    "Movie-Name": "Simmba"
                }
            },
            {
                "_index": "songs",
                "_type": "_doc",
                "_id": "S5nO33kBmj9ei9SmPR7j",
                "_score": 1.0,
                "_source": {
                    "Artist-Name": "Neha Kakkar, Tony Kakkar",
                    "Song-Name": "Coca Cola",
                    "Genere": "BollywoodDanceRomantic",
                    "User-Rating": "9.0/10",
                    "Id": 2,
                    "Movie-Name": "Luka Chuppi"
                }
            },
            ..
            ..
            ..
```


