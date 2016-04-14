# [compliance.cloud.gov](https://compliance.cloud.gov/) Deployment

This repo contains the [Concourse](https://concourse.ci/) pipeline for deploying [compliance.cloud.gov](https://compliance.cloud.gov/) a gitbook system security plan (SSP) for [Cloud.Gov](https://cloud.gov/).

## Local testing

1. Run

    ```bash
    cp credentials.yml.example credentials.yml
    fly -t lite set-pipeline -n -c pipeline.yml -p compliance-documentation -l credentials.yml
    fly -t lite unpause-pipeline -p compliance-documentation
    ```

1. Go to [the pipeline page](http://192.168.100.4:8080/pipelines/compliance-documentation)

Note this won't actually complete the deployment to compliance.cloud.gov...you will need to modify `credentials.yml` and run `set-pipeline` again for that to work.
