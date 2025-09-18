<!-- markdownlint-disable MD030 -->

# AI Agent Builder Server

<h3>Build AI Agents, Visually</h3>

## ⚡Quick Start

1. Install the application
    ```bash
    npm install -g flowise
    ```
2. Start the application

    ```bash
    npx flowise start
    ```

3. Open [http://localhost:3000](http://localhost:3000)

## 🌱 Env Variables

The application supports different environment variables to configure your instance. You can specify the following variables in the `.env` file inside `packages/server` folder.

You can also specify the env variables when using `npx`. For example:

```
npx flowise start --PORT=3000 --DEBUG=true
```

| Variable                           | Description                                                                      | Type                                             | Default                             |
| ---------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------ | ----------------------------------- |
| PORT                               | The HTTP port the application runs on                                            | Number                                           | 3000                                |
| CORS_ORIGINS                       | The allowed origins for all cross-origin HTTP calls                              | String                                           |                                     |
| IFRAME_ORIGINS                     | The allowed origins for iframe src embedding                                     | String                                           |                                     |
| FLOWISE_FILE_SIZE_LIMIT            | Upload File Size Limit                                                           | String                                           | 50mb                                |
| DEBUG                              | Print logs from components                                                       | Boolean                                          |                                     |
| LOG_PATH                           | Location where log files are stored                                              | String                                           | `your-path/Flowise/logs`            |
| LOG_LEVEL                          | Different levels of logs                                                         | Enum String: `error`, `info`, `verbose`, `debug` | `info`                              |
| LOG_JSON_SPACES                    | Spaces to beautify JSON logs                                                     |                                                  | 2                                   |
| TOOL_FUNCTION_BUILTIN_DEP          | NodeJS built-in modules to be used for Tool Function                             | String                                           |                                     |
| TOOL_FUNCTION_EXTERNAL_DEP         | External modules to be used for Tool Function                                    | String                                           |                                     |
| DATABASE_TYPE                      | Type of database to store the application data                                   | Enum String: `sqlite`, `mysql`, `postgres`       | `sqlite`                            |
| DATABASE_PATH                      | Location where database is saved (When DATABASE_TYPE is sqlite)                  | String                                           | `your-home-dir/.flowise`            |
| DATABASE_HOST                      | Host URL or IP address (When DATABASE_TYPE is not sqlite)                        | String                                           |                                     |
| DATABASE_PORT                      | Database port (When DATABASE_TYPE is not sqlite)                                 | String                                           |                                     |
| DATABASE_USER                      | Database username (When DATABASE_TYPE is not sqlite)                             | String                                           |                                     |
| DATABASE_PASSWORD                  | Database password (When DATABASE_TYPE is not sqlite)                             | String                                           |                                     |
| DATABASE_NAME                      | Database name (When DATABASE_TYPE is not sqlite)                                 | String                                           |                                     |
| DATABASE_SSL_KEY_BASE64            | Database SSL client cert in base64 (takes priority over DATABASE_SSL)            | Boolean                                          | false                               |
| DATABASE_SSL                       | Database connection overssl (When DATABASE_TYPE is postgre)                      | Boolean                                          | false                               |
| SECRETKEY_PATH                     | Location where encryption key (used to encrypt/decrypt credentials) is saved     | String                                           | `your-path/Flowise/packages/server` |
| FLOWISE_SECRETKEY_OVERWRITE        | Encryption key to be used instead of the key stored in SECRETKEY_PATH            | String                                           |                                     |
| MODEL_LIST_CONFIG_JSON             | File path to load list of models from your local config file                     | String                                           | `/your_model_list_config_file_path` |
| STORAGE_TYPE                       | Type of storage for uploaded files. default is `local`                           | Enum String: `s3`, `local`, `gcs`                | `local`                             |
| BLOB_STORAGE_PATH                  | Local folder path where uploaded files are stored when `STORAGE_TYPE` is `local` | String                                           | `your-home-dir/.flowise/storage`    |
| S3_STORAGE_BUCKET_NAME             | Bucket name to hold the uploaded files when `STORAGE_TYPE` is `s3`               | String                                           |                                     |
| S3_STORAGE_ACCESS_KEY_ID           | AWS Access Key                                                                   | String                                           |                                     |
| S3_STORAGE_SECRET_ACCESS_KEY       | AWS Secret Key                                                                   | String                                           |                                     |
| S3_STORAGE_REGION                  | Region for S3 bucket                                                             | String                                           |                                     |
| S3_ENDPOINT_URL                    | Custom Endpoint for S3                                                           | String                                           |                                     |
| S3_FORCE_PATH_STYLE                | Set this to true to force the request to use path-style addressing               | Boolean                                          | false                               |
| GOOGLE_CLOUD_STORAGE_PROJ_ID       | The GCP project id for cloud storage & logging when `STORAGE_TYPE` is `gcs`      | String                                           |                                     |
| GOOGLE_CLOUD_STORAGE_CREDENTIAL    | The credential key file path when `STORAGE_TYPE` is `gcs`                        | String                                           |                                     |
| GOOGLE_CLOUD_STORAGE_BUCKET_NAME   | Bucket name to hold the uploaded files when `STORAGE_TYPE` is `gcs`              | String                                           |                                     |
| GOOGLE_CLOUD_UNIFORM_BUCKET_ACCESS | Enable uniform bucket level access when `STORAGE_TYPE` is `gcs`                  | Boolean                                          | true                                |
| SHOW_COMMUNITY_NODES               | Show nodes created by community                                                  | Boolean                                          |                                     |
| DISABLED_NODES                     | Hide nodes from UI (comma separated list of node names)                          | String                                           |                                     |

## 📄 License

Source code in this repository is made available under the [Apache License Version 2.0](LICENSE.md).