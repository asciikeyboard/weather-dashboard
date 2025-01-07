# Weather Dashboard Application

This application fetches weather app data from the OpenWeather API and saves it to AWS S3 Bucket.

## Prerequisites

- AWS account with access keys
- OpenWeather API key
- Python, VS Code, GitHub

## Setup

1. Clone this repository:
    ```sh
    git clone https://github.com/asciikeyboard/weather-dashboard.git
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

3. Run the python script:

    ```sh
    python3 src/weather_dashboard.py
    ```

4. Verify data in S3 bucket

## Usage 

The application will parse weather data from the cities. The weather data will be saved to the specified AWS S3 bucket.

## AWS Configuration

The application uses the AWS CLI to interact with the S3. Ensure your AWS credentials are correctly set in the **.env** file. Also check the aws config file via "cat ~/.aws/config" command.

## Resources

- [OpenWeather API Documentation](https://openweathermap.org/api): Learn more about the OpenWeather API.
- [AWS S3 Documentation](https://docs.aws.amazon.com/s3/index.html): Comprehensive guide to using AWS S3.
- [AWS CLI Configuration](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html): Guide to configuring the AWS CLI.
