# Coffee Cart App - Automation Suite

This project is a Selenium-based automation test suite developed for conducting automated UI testing on the Coffee Cart web application. It features comprehensive test coverage using Maven, TestNG, and cross-browser testing capabilities for Chrome, Edge, and Firefox. The project is integrated with GitHub Actions for continuous integration, enabling automated test execution and reporting. The test suite validates various e-commerce scenarios including cart operations, checkout processes, and payment validations, ensuring robust functionality across different browsers.

Key Features:
- Automated cross-browser testing (Chrome and Edge)
- Continuous Integration with GitHub Actions
- Organized test structure with TestNG
- Maven-based project management
- Robust test scenarios covering cart and checkout functionality
- Automated test execution on push events

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Setup and Installation](#setup-and-installation)
- [Running Tests](#running-tests)
- [Allure Reports](#allure-reports)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The **Coffee Cart App Automation Practice** is designed to test the Coffee Cart web application. It covers multiple test cases to validate the cart functionality, including item addition, cart updating, and checkout processes. The test suite also implements cross-browser testing across Chrome, Edge, and Firefox.

## Technologies Used
- **Java**
- **Selenium WebDriver**
- **TestNG**
- **Maven**
- **Allure Reports**
- **Github Actions**
- **Browsers Supported**: Chrome, Firefox, Edge

## Project Structure
```plaintext
Coffee-Cart-App-AutomationPractice/
├── src/
│   ├── test/
│   │    ├── java/com/example/coffee_cart_app
│   │       ├── testClasses
│   │       ├── utilityMethods
│   ├── resources
├── pom.xml
└── README.md
```


- **utilityMethods**: Contains base classes like `BaseTest`, which handles test setup and teardown.
- **testClasses**: All Test classes.
- **resources**: Contains allure properties and testng.xml .

## Setup and Installation (For Local testing)

1. Clone the repository:
    ```bash
    git clone https://github.com/jafrnq/Coffee-Cart-App-AutomationPractice.git
    ```
   
2. Navigate into the project directory:
    ```bash
    cd Coffee-Cart-App-AutomationPractice
    ```

3. Install dependencies via Maven:
    ```bash
    mvn clean install
    ```

4. The Project uses Selenium 4 so browser drivers should be automatically installed.

### Running Tests

To run all tests using TestNG, use the following Maven command:

```bash
mvn test
```

To execute tests for specific browsers (Edge/Firefox), you can set the browser parameter in your TestNG suite XML or pass it through Maven as:

### Allure Reports

This project uses Allure for reporting test results. After running the tests, generate the Allure report using:

```bash
mvn allure:report
mvn allure:serve
```

This will automatically open the generated report in your default browser.

## GitHub Actions CI/CD
This project uses GitHub Actions for continuous integration and automated test execution. Every time you push changes to the repository, the workflow will automatically run your tests and generate Allure reports.

### Running Tests via GitHub Actions
1. Navigate to your repository on GitHub
2. Click on the "Actions" tab at the top of your repository
3. In the left sidebar, click on "Run Tests and Generate Allure Report"
4. Click the "Run workflow" button
   - Select the branch you want to run the tests on
   - Click "Run workflow" to start the execution
5. A new workflow run will be initiated, and you can click on it to see the progress
6. Once completed, you can view the test results and Allure report in the workflow artifacts

### Viewing Test Results
- The test results will be available in the Actions tab after each workflow run
- Allure reports are automatically generated and published to GitHub Pages
- You can access the latest Allure report by clicking on the GitHub Pages link in the latest "pages-build-deployment" build or in your repository settings.

## Contributing
If you would like to contribute, feel free to open an issue or submit a pull request. Please make sure to follow best practices for Java and Selenium projects.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
