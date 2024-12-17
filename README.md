# Flask-Excel-to-AWS-S3-for-Power-BI-Integration
 uploading Excel files, storing them in an AWS S3 bucket, and connecting the data to Power BI.

 # Flask Excel to AWS S3 for Power BI Integration

This project is a Flask application that facilitates uploading Excel files to an AWS S3 bucket, enabling integration with Power BI dashboards. It ensures seamless data storage and refresh workflows for Power BI users.

## Features
- Upload `.xlsx`, `.xls`, or `.csv` files through a web interface.
- Automatically replaces existing files in the S3 bucket.
- Supports resetting data by copying a predefined `Rawdata` file to the `Clientdata` file in S3.
- Enables Power BI to connect to updated data stored in S3.

## Requirements
- Python 3.x
- AWS S3 credentials with appropriate permissions
- Flask
- Boto3 (AWS SDK for Python)
- Power BI for data visualization

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/your-repo-name.git
    ```
2. Navigate to the project directory:
    ```bash
    cd your-repo-name
    ```
3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Configuration

Update the following variables in `app.py` with your AWS details:
- `S3_BUCKET`: Name of your S3 bucket.
- `S3_KEY`: AWS Access Key.
- `S3_SECRET`: AWS Secret Key.
- `S3_REGION`: AWS region (e.g., `us-east-1`).

To secure sensitive credentials, use environment variables or a secure configuration tool.

## Usage

1. Start the Flask app:
    ```bash
    python app.py
    ```
2. Access the app in your browser at `http://127.0.0.1:5000/`.
3. Use the web interface to:
   - Upload Excel or CSV files.
   - Reset data using the `Reset` endpoint.

4. **Power BI Integration**:
   - Use the AWS S3 URL for the uploaded file as the data source in Power BI.
   - Set up automatic refresh in Power BI to keep your dashboard updated with the latest data from S3.

## Security Best Practices
- Do not hardcode AWS credentials in `app.py`.
- Use environment variables or a secret management tool.
- Apply strict access controls to your S3 bucket.

## Folder Structure

