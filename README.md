# Commvault-Prometheus-Reports-Exporter

This project includes a metric service that presents the status information of Backup and Restore operations performed on the Commvault platform in Prometheus format. Metrics are collected every 60 seconds, and the results are made available on port 9279. The script retrieves the statuses of operations that have been completed, failed, canceled, or completed with errors within the last 24 hours each time it runs.

## Supported Statuses:
  - Completed: The operation was successfully completed.
  - Failed: The operation failed.
  - Kill: The operation was canceled by the user.
  - Completed w/ one or more errors: The operation was completed with one or more errors.
  - Completed w/ one or more warnings: The operation was completed with one or more warnings.

## Metrics Label
### `commvault_job_status`

This metric represents the status of operations running on the Commvault platform.

- `jobId`: Operation identifier.
- `status`: Operation status (Completed, Failed, Kill, Completed w/ one or more errors, Completed w/ one or more warnings).
- `jobType`: Type of operation.
- `localizedOperationName`: Localized operation name.
- `ClientName`: Name of the client initiating the operation.
- `ClientDisplayName`: Display name of the client initiating the operation.
- `jobStartTime`: Start time of the operation.
- `jobEndTime`: End time of the operation.
- `clientId`: Client identifier.
- `appType`:appType: Application type.

Metric Values

- `1`:  Operation completed successfully.
- `2`:  Operation completed with one or more warnings.
- `3`: Operation completed with one or more errors.
- `4`: Operation failed.
- `5`: Operation canceled by the user.

# Configuration and Installation
