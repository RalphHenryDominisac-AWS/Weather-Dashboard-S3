# Weather Dashboard App with AWS S3

This application retrieves weather data from the OpenWeather API and stores it in an AWS S3 bucket.

## Prerequisites

Before setting up the application, ensure the following:

-Python 3.x installed on your machine.
-An AWS account with appropriate access credentials.
-A valid OpenWeather API key.
-AWS CLI installed and configured (optional for manual configuration).

## Setup

1. Clone this repository:
    ```sh
    git clone https://github.com/RalphHenryDominisac-AWS/Weather-Dashboard-S3.git
    cd weather-dashboard    
    ```

2. Create a [.env](https://dotenvx.com/docs/env-file) file in the root directory with the following content:

    ```properties
      OPENWEATHER_API_KEY=your_openweather_api_key
      AWS_BUCKET_NAME=weather-dashboard-${RANDOM}
    
      # AWS CREDENTIALS
      AWS_ACCESS_KEY_ID=your_aws_secret_key_id
      AWS_SECRET_ACCESS_KEY=your_aws-secret_access_key
      AWS_DEFAULT_REGION=your_aws_default_region
    ```

    Replace the placeholders with your actual credentials and keys.


3. Install Dependencies: Create a virtual environment and install the required Python dependencies

    ```sh
    python -m venv venv
    source venv/bin/activate  # For Linux/Mac
    venv\Scripts\activate     # For Windows
    pip install -r requirements.txt
    ```

4. Run the Application: You can now run the application using Python

   ```sh
    python src/weather_dashboard.py
    ```


## Usage 

The application fetches weather data for the cities listed in the /data/cities.json file. This data is then saved to the specified AWS S3 bucket.

## AWS Configuration

The application interacts with AWS S3 via the AWS SDK (Boto3). Ensure that your AWS credentials are correctly configured in the **.env** file for successful integration.


## License 

This project is licensed under the MIT License.
