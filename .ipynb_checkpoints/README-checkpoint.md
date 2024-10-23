# Vertex AI Search Agent Builder

## Pre-requisite Setup

### Enable APIs and service account permissions
Enable the Vertex AI Search API:
```
gcloud services enable discoveryengine.googleapis.com
```
Enable the Enterprise Knowledge Graph API:
```
gcloud services enable enterpriseknowledgegraph.googleapis.com
```
Enable Cloud Run:
```
gcloud services enable run.googleapis.com
```
Give the Cloud Run service account required permissions:
```
gcloud projects add-iam-policy-binding [PROJECT_ID or PROJECT_NUMBER] --member='serviceAccount:[PROJECT_NUMBER]-compute@developer.gserviceaccount.com' --role='roles/discoveryengine.viewer'
```

1. Run the cells in **Install dependencies and set variables** section, this will also create a storage bucket for you.
2. Upload your Data in [storage bucket] ### to this BUCKET_URI and upload all of your documents. 

## Setting up Agent Builder
This section creates your datastore, imports your documents from the storage bucket and creates your search engine.

3. Run the cells in the **Setting up Agent Builder** section, this 

## Create Streamlit Search App
This section creates the files need to run the app.

4. Run the in **Create Streamlit Search App** to generate the front end

4a. omit **Run Streamlit app locally** cell if you are not testing or running locally.

## Deploy Streamlit Search App to Cloud Run
This section is for deploying the app made in the previous step to Cloud Run

5. In the **second cell** under **Replace the following below** replace the following in the **entrypoint** line with the values from the first cell: **PROJECT_ID** **DATASTORE_ID** **BUCKET_NAME**

6. Run all cells under the **Deploy Streamlit Search App to Cloud Run** section, this will take several minutes, but will also give you the link to your app below (The app link will also be accessible through selecting the [cloud run service](https://pantheon.corp.google.com/run?referrer=search&authuser=2&hl=en-GB&project=ai-sb-test))