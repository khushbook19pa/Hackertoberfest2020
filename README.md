## 📡 API Documentation

| **Method** | **API**                            | **Description**                                                                                                                |
| ---------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **GET**    | `/dashboard/v3/`                   | Root endpoint that returns a welcome message                                                                                   |
| **GET**    | `/dashboard/v3/ecotron?limit=1`    | Retrieves the latest Ecotron machine details. Use `limit` in the query (e.g., `limit=1`) to get the most recent record         |
| **GET**    | `/dashboard/v3/ecotron/{machineId}` | Retrieves the current measurement details of the specified Ecotron device. Replace `EZMC240300029` with the desired machine ID |
| **GET** | `/dashboard/v3/ecotron/profile/{machineId}` | Retrieves the profile information of the specified Ecotron device. Replace `{machineId}` with the actual machine ID |
| **GET** | `/dashboard/v3/ecotron/design-metrics/{machineId}` | Returns the design metrics of the specified Ecotron device. Replace `{machineId}` with the actual machine ID |
| **POST** | `/dashboard/v3/ecotron/download-xlsx/{machineId}` | Downloads an XLSX sheet for the specified Ecotron device and month. Requires a JSON body with `month` and `format` fields |
| **POST** | `/dashboard/v3/ecotron/graph/{machineId}` | Returns a list of measurements for the specified device between `from` and `to`. Use `paramList` to select which fields to include |
| **GET** | `/dashboard/v3/ecotron/status/{machineId}?minutes={minutes}` | Checks the status of the specified Ecotron device for the past given number of minutes. Replace `{machineId}` with the actual ID and `{minutes}` with the time window (e.g., `5` for last 5 minutes) |
| **POST** | `/dashboard/v3/ecotron/ai-graph/{machineId}` | Retrieves AI-processed measurement data for the specified device between `from` and `to`. Include `measurement` and `timeFlag` in the body to customize results |
| **GET** | `/dashboard/v3/ecotron/list/{mobile}` | Retrieves a list of all Ecotron systems linked to the specified user. Replace `{mobile}` with the user’s mobile number or ID |
| **GET** | `/dashboard/v3/ecotron/service/problem-solution` | Retrieves a list of parts with their corresponding problems and recommended solutions |
| **GET** | `/dashboard/v3/ecotron/device/{machineId}` | Retrieves detailed information about the specified Ecotron device. Replace `{machineId}` with the actual machine ID |
| **POST** | `/dashboard/v3/ecotron/deviceinfo/{machineId}` | Updates device information for the specified Ecotron machine. Provide `pump_sl` and `motorsl` values in the request body |
| **GET** | `/dashboard/v3/ecotron/service-tickets/{user_id}?getLatest={boolean}` | Retrieves all service tickets for the specified user. Set `getLatest=true` to fetch only the most recent service entry |
| **POST** | `/dashboard/v3/ecotron/service-tickets/{user_id}` | Creates one or more service ticket entries for the specified user. Provide an array of ticket objects with service details in the request body |
| **GET** | `/dashboard/v3/ecotron/service-ticket/form-id/{serviceid}` | Retrieves a list of all form IDs linked to the specified service ID |
| **POST** | `/dashboard/v3/ecotron/drive-update` | Updates drive responses in bulk. Provide an array of response objects containing `id`, `executed_at`, and `actual_response` |
| **POST** | `/dashboard/v3/ecotron/drive-param` | Sends a drive parameter update command for the specified machine. Provide machine ID, command details, and expected response in the request body |
| **DELETE** | `/dashboard/v3/ecotron/drive-param?command_id={command_id}` | Deletes a pending or queued drive parameter command by its `command_id`. Returns confirmation when successfully deleted |
| **POST** | `/dashboard/v3/ecotron/faults/{machineId}` | Retrieves a list of faults for the specified Ecotron device within the given date range. Provide `from` and `to` in the request body |
| **POST** | `/dashboard/v3/ecotron/performance-metrics/{machineId}` | Calculates and retrieves performance metrics for the specified Ecotron device within the given date range. Provide `from` and `to` in the request body |
| **GET** | `/dashboard/v3/ecotron/check/{machineId}` | Performs an electronic check for the specified Ecotron device and returns the current health/status information |
| **GET** | `/dashboard/v3/ecotron/fota?timestamp={timestamp}` | Retrieves a list of Ecotron devices whose FOTA (Firmware Over-The-Air) update process has started since the given `timestamp` |
| **POST** | `/dashboard/v3/ecotron/fota` | Initiates the FOTA (Firmware Over-The-Air) update process for a list of devices. Provide device IDs, controller type, and target FOTA version in the request body |
| **GET** | `/dashboard/v3/ecotron/fota/versions` | Retrieves all available FOTA (Firmware Over-The-Air) versions stored on the server |
| **POST** | `/dashboard/v3/ecotron/fota/versions` | Uploads a new FOTA (Firmware Over-The-Air) file to the server. Requires a `file` field in `multipart/form-data` format |
| **POST** | `/dashboard/v3/ecotron/drive-param-bulk` | Uploads a CSV file containing parameter updates for multiple Ecotron devices. Requires `file` in `multipart/form-data` format |
| **POST** | `/dashboard/v3/ecotron/mqtt/{machineId}` | Retrieves raw MQTT data for the specified Ecotron device from ClickHouse. Supports filtering by date range, pagination, and createdAt timestamp |
| **POST** | `/dashboard/v3/ecotron/upload-file` | Uploads one or more files related to an Ecotron device to the server. Accepts multiple files (`file1`, `file2`, `file3`, `file4`, `file5`) via `multipart/form-data` |
| **POST** | `/dashboard/v3/ecotron/upload-file-machine` | Uploads one or more files associated with a specific machine to the server. Accepts multiple files (`file1`, `file2`, `file3`, `file4`, `file5`) via `multipart/form-data` |
| **POST** | `/dashboard/v3/ecotron/download-current-projected_file` | Generates and downloads a CSV file containing the selected measurement parameters for Ecotron devices. Provide `paramList` in the request body |
| **GET** | `/dashboard/v3/ecotron/download-all-faults` | Downloads a CSV file containing the latest list of faults for all Ecotron devices (up to 10,000 rows) |
| **GET** | `/dashboard/v3/ecotron/download-current-file` | Downloads a CSV file containing the latest measurements of all Ecotron devices |
| **POST** | `/dashboard/v3/ecotron/fcm-id/{mobile}` | Stores or updates the FCM (Firebase Cloud Messaging) ID for the given user (mobile). Provide `fcm_id` in the request body |
