# This is a sample project for bootstraping Django projects.

Sample Readme

## Setup

1. Setup a virtual environment (poetry and python >3.9)
   * You can use pycharm by using "Add new interpreter"
   * or You can do it manually by running `poetry install` and then `poetry shell`

2. Setup pycharm to work with django
   1. Go to `File -> Settings -> Frameworks & Languages -> Django`
   2. Enable Django Support
   3. Fill in the path to the project: "/some/absolute/path/strefa-partnera/backend"
   4. Fill in the path to the manage.py: "manage.py"
   5. Fill in the path to the settings: "backend/settings.py"
3. Download the service account key from google cloud console
   1. Go to `https://console.cloud.google.com/iam-admin/serviceaccounts?project=strefa-partnera-379912`
   2. Select the project
   3. Select the service account
   4. Select ... -> manage keys
   5. Click "add key" -> "create new key" -> "json
   6. Save the file in the root of the project
4. Add configuration
   1. Edit configurations -> "+" -> Django Server
   2. Add the following environment variables:
      * `GOOGLE_APPLICATION_CREDENTIALS=path/to/key.json`
      * `DJANGO_SETTINGS_MODULE=backend.settings`
5. Add .env file under backend/.env
    * Go to `secrets url`
    * Click ... -> "view secret value"
    * Copy the value and paste it into the .env file
