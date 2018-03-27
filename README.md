<a href="https://www.sparkpost.com"><img src="https://www.sparkpost.com/sites/default/files/attachments/SparkPost_Logo_2-Color_Gray-Orange_RGB.svg" width="200px"/></a>

[Sign up](https://app.sparkpost.com/join?src=Dev-Website&sfdcid=70160000000pqBb) for a SparkPost account and visit our [Developer Hub](https://developers.sparkpost.com) for even more content.

This sample app demonstrates how to send email with Python and [python-sparkpost](https://github.com/SparkPost/python-sparkpost) on the Google App Engine flexible environment.

### Prerequisites

 - a [Google Cloud Platform](https://cloud.google.com/) account
 - the [Google Cloud SDK](https://cloud.google.com/sdk/) installed and configured

### Setup

1. Sign up for a SparkPost account [here](https://app.sparkpost.com/join).

1. Create an API key with *Transmissions: read/write* privilege [here](https://app.sparkpost.com/account/credentials).

1. Add your API key to `app.yaml`.

1. Optional: prepare an isolated Python virtual environment:
    ```sh
    virtualenv env
    source env/bin/activate
    ```

1. Install the app's dependencies:
    ```sh
    pip install -r requirements 
    ```

### Running Locally

1. Start the app:
    ```sh
    SPARKPOST_API_KEY=your-api-key python main.py
    ```

1. Visit the app in your browser: [http://localhost:8080/](http://localhost:8080/)

### Deploying To Google App Engine 

1. Deploy the app and dependencies to your Google Cloud project:
    ```sh
    gcloud app deploy
    ```

1. Visit the app in your browser: 
    ```sh
    gcloud app browse
    ```

### Running The Tests

```sh
pip install pytest responses flaky
pytest main_test.py
```

