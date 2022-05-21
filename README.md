# Build a marketing data infrastructure with Google Cloud

## Disclaimer:
🚧 This is a work in progress.

👨🏻‍💻 I'm not a professional developer and sometimes my script code may not be as good as it should be. feel free to contact me to contribute to the project.

---

## Architecture

![GCP Warehouse](https://user-images.githubusercontent.com/29273232/169641582-d9947fe3-eb08-4d84-86f6-0fda91943dbe.svg)


---

## Get start:
### Google Cloud:
  - [Google Cloud overview](https://cloud.google.com/docs/overview)
  - [Google Cloud products](https://cloud.google.com/products)
  - [Google Cloud Developer cheat sheet](https://googlecloudcheatsheet.withgoogle.com/)
  - [Visualizing Google Cloud](https://twitter.com/pvergadia/status/1507039794592899078) by [Priyanka Vergadia](https://twitter.com/pvergadia)
  - [Google Cloud Architecture Diagramming Tool](https://googlecloudcheatsheet.withgoogle.com/architecture)

## How to:
### Google Tag Manager:
  - #### Client-side GTM:
    - [Create Google Tag Manager client side container](https://developers.google.com/tag-platform/tag-manager/web) 
    - [Google Consent Mode](https://support.google.com/analytics/answer/9976101) and [how it affects the way Google Analytics records data](https://adswerve.com/blog/how-consent-mode-affects-the-way-google-analytics-records-data/)
    - [Google Consent Mode for websites](https://developers.google.com/tag-platform/devguides/consent#tag-manager)
    - [Google Consent Mode for iOS apps](https://developers.google.com/tag-platform/devguides/app-consent?platform=ios)
    - [Google Consent Mode for Android apps](https://developers.google.com/tag-platform/devguides/app-consent?platform=android)

  - #### Server-side GTM:
    - [Intro to Server-side GTM](https://developers.google.com/tag-platform/tag-manager/server-side/intro)
    - [Create Google Tag Manager server side container](https://developers.google.com/tag-platform/tag-manager/server-side#create_a_tag_manager_server_container)
    - [Automatically deploy server-side GTM on App Engine](https://developers.google.com/tag-platform/tag-manager/server-side/script-user-guide)
    - [Manually deploy server-side GTM on App Engine](https://developers.google.com/tag-platform/tag-manager/server-side/script-user-guide)
    - [Manually deploy server-side GTM on App Engine](https://www.simoahava.com/analytics/provision-server-side-tagging-application-manually/) with [Simo Ahava](https://twitter.com/simoahava)
    - [Deploy server-side GTM on Cloud Run](https://code.markedmondson.me/gtm-serverside-cloudrun/) with [Mark Edmondson](https://twitter.com/holomarked)
    - [Import GTM custom template](https://developers.google.com/tag-platform/tag-manager/templates#export_and_import)

### Compute engine:
  - [Create and manage Compute Engine VM instances](https://cloud.google.com/compute/docs/instances/create-start-instance)
  - [Deploy and manage AirByte on Compute Engine](https://docs.airbyte.com/deploying-airbyte/on-gcp-compute-engine)
  - [Create and manage scheduled snapshots for Persistent Disks](https://cloud.google.com/compute/docs/disks/scheduled-snapshots)

### Cloud functions:
  - [Deploy Cloud Functions](https://cloud.google.com/functions/docs/deploying)

### AppScript:
  - [Deploy AppScript functions](https://www.benlcollins.com/apps-script/google-apps-script-beginner-guide/)
 
### Cloud Scheduler:
  - [Create and manage Cloud Scheduler cron job](https://cloud.google.com/scheduler/docs/creating)

### Cloud Logging:
  - [Query Cloud Logging logs with Logs Explorer](https://cloud.google.com/logging/docs/view/logs-explorer-interface) 
  - [Create and manage Cloud Logging sinks](https://cloud.google.com/logging/docs/export/configure_export_v2)

### Pub/sub:
  - [Create and manage Cloud Pub/Sub topic](https://cloud.google.com/pubsub/docs/admin)
  - [Create and manage Cloud Pub/Sub subscription](https://cloud.google.com/pubsub/docs/create-subscription)

### Storage:
  - [Create and manage Cloud Storage bucket](https://cloud.google.com/storage/docs/creating-buckets)
  - [Create and manage Cloud Firestore database](https://cloud.google.com/firestore/docs/data-model?hl=it)
  - [Create and manage Stream Collections to BigQuery](https://firebase.google.com/products/extensions/firebase-firestore-bigquery-export)

### BigQuery:
  - [Create and manage BigQuery datasets](https://cloud.google.com/bigquery/docs/datasets)
  - [Create and manage BigQuery tables](https://cloud.google.com/bigquery/docs/tables)
  - [Create and manage BigQuery external tables](https://cloud.google.com/bigquery/external-data-sources)
  - [Query Google Analytics 4 export data](https://www.ga4bigquery.com/tag/ga4-dimensions-metrics/)
  - [Query Google Analytics Universal export data](https://www.ga4bigquery.com/tag/ua-dimensions-metrics/)

---

## Scripts

### Google Tag Manager

- #### Client-side GTM Tags:
  - [HTTP POST/GET request sender](https://github.com/tommasomoretti/cs-http-tag): send HTTP POST and GET requests from client-side GTM to an endpoint
  - [Custom Facebook pixel tag](https://github.com/Adsmurai-Google-Tag-Manager-Templates/adsmurai-facebook-pixel-and-conversions-api): fire Facebook events through regular pixel and Conversions API.

- #### Server-side GTM Tags:
  -  [HTTP POST/GET client](https://github.com/tommasomoretti/ss-http-client-tag): collect HTTP POST and GET requests
  -  [HTTP POST/GET request sender](https://github.com/tommasomoretti/ss-http-tag): send HTTP POST and GET requests from server-side GTM to an endpoint
  -  [Google BigQuery data writer](https://github.com/tommasomoretti/ss-bq-tag): write data in realtime into Goole BigQuery
  -  [Google Cloud Firestore data writer](https://github.com/tommasomoretti/ss-fs-tag): write data in realtime into Google Cloud Firestore
  -  Google Cloud Storage data writer: write data in realtime into Google Cloud Storage
  -  [Custom Facebook client Tag](https://github.com/Adsmurai-Google-Tag-Manager-Templates/adsmurai-facebook-conversions-api-client): handle requests for Facebook Conversions API
  -  [Custom Facebook CAPI tag](https://github.com/Adsmurai-Google-Tag-Manager-Templates/adsmurai-facebook-conversions-api-tag): send requests using Facebook's Conversions API

### Cloud Functions
  - EL from GCS to BQ: extract and load data (CSV, JSON, Avro, Parquet, ORC) scheduled/in realtime from Google Cloud Storage (with versioning) to BigQuery tables
  - Alerts: scheduled/in realtime emails alert

### App Script
  - [EL from Google Sheets to BQ](https://techandeco.medium.com/apps-script-tutorial-upload-to-a-database-sheets-bigquery-2fee3724f3ca): extract and load data scheduled/on-demand from Google Sheets to BigQuery table.
  - EL from Google Sheets to Cloud Storage: extract and load data scheduled/on-demand from Google Sheets to Gloud Storage file.
