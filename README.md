# Restful-Booker API Testing & CI/CD

## 1. Project Overview

This project demonstrates API test automation using Postman, CI/CD integration with GitHub Actions, and Shift-Right Testing for API monitoring.

**Target API:** https://restful-booker.herokuapp.com

## 2. Technologies Used

- Postman: API testing and test automation.
- Newman: Command-line tool for running Postman collections.
- GitHub: Source code repository.
- GitHub Actions: CI/CD automation.
- Postman CLI: Running the production monitoring collection.

## 3. Project Structure

```text
demo_API/
├── .github/
│   └── workflows/
│       ├── main.yml
│       └── monitor.yml
├── RestfulBooker.postman_collection.json
├── RestfulBooker.postman_environment.json
├── booking_data.csv
└── README.md
```

## 4. API Testing

The Postman collection contains positive and negative test cases:

- Authentication with valid credentials.
- Create a booking.
- Retrieve booking information.
- Delete a booking.
- Test invalid authorization.
- Test invalid authentication.
- Test invalid input data.

The project uses a CSV file for data-driven testing.

## 5. CI/CD Pipeline

The GitHub Actions workflow in `.github/workflows/main.yml` runs API tests automatically when code is pushed or a pull request is created.

The pipeline uses Node.js and Newman to execute the Postman collection.

## 6. Shift-Right Testing

The workflow in `.github/workflows/monitor.yml` monitors the target API using a Postman collection.

The scheduled workflow is configured to run every hour. Manual execution is also available through GitHub Actions.

A GitHub repository secret named `POSTMAN_API_KEY` is required for Postman CLI authentication.

## 7. How to Run

1. Open the GitHub repository.
2. Select the **Actions** tab.
3. Select the desired workflow.
4. Run the workflow manually if manual execution is enabled.
5. Review the execution logs and test results.

## 8. Expected Results

- API requests are executed automatically.
- Test results are displayed in the workflow logs.
- Failed tests can be investigated using GitHub Actions logs.
- The monitoring workflow checks API availability and response time.

## 9. Author

Student: [Your Name]

Course: Software Testing

University: Van Lang University
