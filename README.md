# Frequently-used-Commands

- `conda env list` or `conda info --envs`: List all conda envs
- `conda list -n <my_env>` : List all packages installed in the env my_env
- `pip list`: List all packeges in current env. Need to run this when the env is activated.

## Google Cloud
- Typical steps:
  - Start an instance: `gcloud compute instances start pytorch-event-detector-vm `
  - Connecting to the instance: `gcloud compute ssh muyang@pytorch-event-detector-vm` 
  - Stop instances `gcloud compute instances stop pytorch-event-detector-vm --zone us-west1-b`
- check instance status: `gcloud compute instances list`. Note that you have to make sure the status is TERMINATED. Otherwise Google will charge you.
