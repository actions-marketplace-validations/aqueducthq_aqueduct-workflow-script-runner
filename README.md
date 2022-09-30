# Aqueduct workflow script runner docker action

This action installs the `aqueduct-sdk` package and runs an Aqueduct workflow script.

## Inputs

## `server_address`

**Required** IP address of the Aqueduct server.

## `port`

**Optional** Port on which the server is listening.

## `api_key`

**Required** Api key to gain access to the server. This should be passed in as a GitHub secret.

## `path`

**Required** Path to the workflow script.

## Example usage
```
uses: aqueducthq/aqueduct-workflow-script-runner@v1
with:
  server_address: 1.2.3.4
  port: 8080 # Optional
  api_key: ${{ secrets.AQUEDUCT_API_KEY }}
  path: workflow/churn_prediction.py
```