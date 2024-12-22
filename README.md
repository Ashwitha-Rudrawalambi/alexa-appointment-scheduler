# Voice-Activated Appointment Scheduler with Alexa
Revolutionize appointment scheduling with voice technology and Alexa. Using AWS and Google Calendar API, this project aims to simplify booking appointments with doctors, offering a user-friendly and efficient system.

## Overview

This repository contains the code for an Alexa skill designed for XYZ Hospital. The skill is aimed at facilitating user registration, login, appointment scheduling, and related functionalities.

## Features

1. **Registration**: Users can register by providing their name, age, date of birth, gender, and email. If the email is not verified, a verification email is sent.

2. **Login**: Registered users can log in using their unique ID and email. Unsuccessful logins are handled gracefully.

3. **Forgot ID**: Users can retrieve their unique ID by providing their registered email and name.

4. **Appointment Scheduling**: Users can schedule appointments with doctors in different departments for a specified date and time.

5. **Availability Check**: The skill checks the availability of the selected doctor for the specified time. If the doctor is not available, it suggests the next available slot.

6. **Email Confirmation**: Upon successful appointment scheduling, a confirmation email is sent to the user.

7. **Help and Fallback**: The skill provides help messages and fallback responses for a seamless user experience.

## Skill Flow

1. **Launch**: The skill is launched with a welcome message asking the user if they want to login or register.

2. **Registration**: Users can register by providing their details. If the email is not verified, a verification email is sent.

3. **Login**: Registered users can log in using their unique ID and email.

4. **Forgot ID**: Users can retrieve their unique ID by providing their registered email and name.

5. **Appointment Scheduling**: Users can schedule appointments with doctors.

6. **Availability Check**: The skill checks the availability of the selected doctor and suggests the next available slot if needed.

7. **Email Confirmation**: A confirmation email is sent to the user upon successful appointment scheduling.

## Prerequisites

- **Google Calendar API Credentials**: The skill uses the Google Calendar API for appointment scheduling. The API credentials are stored in `creds.json`.

- **DynamoDB Table**: The user data is stored in DynamoDB. Ensure that the table 'patient_info' with the required schema is set up.

- **SMTP Server**: An SMTP server is required to send confirmation emails. The `send_email` function uses this to send emails.

## Setup

1. **Install Dependencies**: Install the required Python libraries.

2. **Configuration**: Update the `creds.json` file with your Google Calendar API credentials.

3. **DynamoDB**: Set up a DynamoDB table named 'patient_info' with the required schema.

4. **SMTP Server**: Configure an SMTP server and update the email sending parameters in the `send_email` function.

## Deployment

Deploy the code as an Alexa skill using the Alexa Skills Kit (ASK). Ensure that the skill is linked to the Lambda function containing this code.

## Usage

1. **Invocation**: "Alexa, open XYZ Hospital."

2. **Follow the prompts**: Alexa will guide you through registration, login, and appointment scheduling.

3. **Natural Language**: The skill understands natural language inputs for a conversational experience.

## Support

For any issues or queries, please open an issue in this repository.
