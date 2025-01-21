# README.md

## Project Title
Responsive Webpage Layout

## Description
This project is a simple responsive webpage layout that utilizes HTML, CSS, and JavaScript to create a flexible and adaptive user interface. The layout consists of a fixed navigation bar, a three-column structure with a left menu, main content area, and a right panel, along with a footer. The design is optimized for various screen sizes, ensuring a seamless user experience across devices.

## Installation Instructions
To set up this project on your local machine, follow these steps:

1. Clone the Repository:
   ```bash
   git clone https://github.com/yourusername/responsive-webpage.git
   cd responsive-webpage
   ```

2. Open the HTML File:
   - Open the `HTML.txt` file in your preferred web browser. You can also rename it to `index.html` for easier access.

3. Link CSS and JavaScript:
   - Ensure that the `styles.css` and `script.js` files are in the same directory as your HTML file. The HTML file already includes links to these files.

4. Run the Project:
   - Simply open the HTML file in a web browser to view the responsive layout in action.

## Usage Instructions
- The webpage is designed to be responsive. Resize your browser window to see how the layout adjusts according to different screen sizes.
- The navigation bar at the top remains fixed while scrolling through the content.
- The left menu, main content area, and right panel are designed to adapt their widths based on the available screen space.

## Features
- Responsive Design: The layout adjusts seamlessly across various screen sizes, from mobile devices to large desktop monitors.
- Fixed Navigation Bar: The navigation bar remains at the top of the page, providing easy access to navigation links.
- Three-Column Layout: The page is divided into three sections: a left menu, a main content area, and a right panel, allowing for organized content presentation.
- Dynamic Scaling: The JavaScript function adjusts the scale of the webpage based on the window size, enhancing readability and usability.
- Cross-Browser Compatibility: The design is compatible with modern web browsers, ensuring a consistent experience for all users.


## **Project Title**
Django Chat Application

## **Description**
This project is a Django-based chat application that allows users to communicate in real-time. It utilizes Django models for user authentication and message storage, along with Django Channels for handling WebSocket connections. The application features a user-friendly interface where users can send and receive messages instantly. The chat messages are stored in a database, and users can view their chat history. The application is designed to be secure, requiring user authentication to access the chat functionality.

## **Installation Instructions**
To set up this Django chat application on your local machine, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/django-chat-app.git
   cd django-chat-app
   ```

2. **Create a Virtual Environment:**
   - It is recommended to use a virtual environment to manage dependencies.
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies:**
   - Install the required packages using pip.
   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up the Database:**
   - Run the following commands to apply migrations and create the database.
   ```bash
   python manage.py migrate
   ```

5. **Create a Superuser (Optional):**
   - Create a superuser to access the Django admin panel.
   ```bash
   python manage.py createsuperuser
   ```

6. **Run the Development Server:**
   - Start the Django development server.
   ```bash
   python manage.py runserver
   ```

7. **Access the Application:**
   - Open your web browser and go to `http://127.0.0.1:8000/` to access the chat application.

## **Usage Instructions**
- **User  Registration and Login:**
  - Users must register and log in to access the chat functionality. Use the provided forms to create an account or log in.

- **Chat Interface:**
  - Once logged in, users can see a list of other users and initiate chats. The chat interface displays the chat history and allows users to send new messages.

- **Real-Time Messaging:**
  - Messages are sent and received in real-time using WebSockets. Users will see new messages appear instantly without needing to refresh the page.

- **Logout:**
  - Users can log out from the application using the logout option in the navigation bar.

## **Features**
- **User  Authentication:** Secure user registration and login system using Django's built-in authentication framework.
- **Real-Time Chat:** Instant messaging capabilities using Django Channels and WebSockets for real-time communication.
- **Chat History:** Users can view their chat history with other users, stored in the database.
- **Responsive Design:** The chat interface is designed to be user-friendly and responsive across different devices.
- **User  List:** Users can see a list of other registered users to initiate chats.
- **Admin Panel:** An admin interface to manage users and chat messages, accessible to superusers.

## **Project Title**
AWS Lambda Functions for Number Operations and S3 File Upload

## **Description**
This project consists of two AWS Lambda functions designed to perform specific tasks: one for adding two numbers and returning the result, and another for uploading files to an Amazon S3 bucket. The first function takes two numbers as input and returns their sum in a JSON format. The second function decodes a base64 encoded file content and uploads it to a specified S3 bucket. This project demonstrates the use of AWS Lambda for serverless computing and AWS S3 for file storage.

## **Installation Instructions**
To set up and deploy these AWS Lambda functions, follow these steps:

1. **Set Up AWS Account:**
   - Ensure you have an AWS account. If you don’t have one, sign up at [AWS](https://aws.amazon.com/).

2. **Install AWS CLI:**
   - Install the AWS Command Line Interface (CLI) on your local machine. Follow the instructions [here](https://aws.amazon.com/cli/).

3. **Configure AWS CLI:**
   - Configure the AWS CLI with your credentials.
   ```bash
   aws configure
   ```

4. **Create an S3 Bucket:**
   - Create an S3 bucket where files will be uploaded. You can do this via the AWS Management Console or using the AWS CLI.
   ```bash
   aws s3 mb s3://your-bucket-name
   ```

5. **Set Environment Variables:**
   - For the S3 upload function, set the environment variable `BUCKET_NAME` to your S3 bucket name.

6. **Deploy Lambda Functions:**
   - You can deploy the Lambda functions using the AWS Management Console or by using AWS SAM (Serverless Application Model) or AWS CloudFormation.

## **Usage Instructions**
- **Adding Two Numbers:**
  - To use the number addition function, invoke the Lambda function with a JSON payload containing `num1` and `num2`. For example:
  ```json
  {
      "num1": 5,
      "num2": 10
  }
  ```
  - The function will return a JSON response with the result:
  ```json
  {
      "statusCode": 200,
      "body": "{\"result\": 15}"
  }
  ```

- **Uploading Files to S3:**
  - To upload a file, invoke the S3 upload function with a JSON payload containing `file_name` and `file_content` (base64 encoded). For example:
  ```json
  {
      "file_name": "example.txt",
      "file_content": "SGVsbG8gd29ybGQh"  // Base64 for "Hello world!"
  }
  ```
  - The function will return a success message:
  ```json
  {
      "statusCode": 200,
      "body": "{\"message\": \"File example.txt uploaded successfully to your-bucket-name.\"}"
  }
  ```

## **Features**
- **Number Addition Functionality:** 
  - A simple Lambda function that takes two numbers as input and returns their sum in a JSON format.

- **File Upload to S3:**
  - A Lambda function that decodes base64 encoded file content and uploads it to an S3 bucket, providing a message upon successful upload.

- **Serverless Architecture:**
  - Both functions are designed to run in a serverless environment, allowing for easy scaling and reduced operational overhead.

- **JSON Responses:**
  - Both functions return responses in JSON format, making it easy to integrate with other applications or services.

- **Environment Variable Configuration:**
  - The S3 upload function uses environment variables for configuration, allowing for flexibility in deployment across different environments.



