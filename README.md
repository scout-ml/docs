# Scout.ml: Dead simple CI/CD for ML teams.

Scout.ml is a tool to track, version, and deploy machine learning experiments from within your Git workflow.

There are 3 components:
1. CLI tool: `sct`
2. Web app: https://app.scout.ml:16043
3. GitHub app: [Link here]

## 1. CLI Tool

Every time an experiment is run, Scout automatically tracks/versions: 1) models, 2) dataset, 3) code. Scout provides a custom Git command `git push-sct origin master`.

#### Template

```yaml
# .scout/user_config.yaml:

version: 1

scout:
  job_id_ref: "EVAL_JOB_ID"
  root_dir: "/Users/gilfoyle/chatbot"
  remote:
    platform: "gcloud" # gcloud, aws
    url: "gs://piedpiper"
    executable_path: "/Users/gilfoyle/google-cloud-sdk/bin/gcloud"

  bucket_id: "gs://piedpiper"

app:
  username: "gilfoyle"
  password: "gilfoyle123"
```
