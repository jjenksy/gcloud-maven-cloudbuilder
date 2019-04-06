# Build
To build this cloud bulder image change the project in the cloudbuild.yaml to the gcloud project name
Then run 
```
gcloud builds submit . --config=cloudbuild.yaml
```
# Step to use the builder in google cloud build
steps:
- name: 'gcr.io/$PROJECT_ID/gcloud-maven'
  args: ['mvn', 'appengine:deploy']