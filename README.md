# MaxwellAI Accessibility Recommendations API README

This project aims to provide accessibility recommendations based on an input assessment of various technologies. The core functionality lies within the JavaScript code, particularly the `getAccessibilityAnalysis` function, which analyzes the input assessment and generates recommendations using a version of appliedAIstudio's PhysarAI technology.

## How to Use

1. **Clone the Repository**: Start by cloning this repository to your local machine.

2. **Project Structure**: The project consists of HTML and JavaScript files, along with JSON files containing input examples and schemas.

3. **Understanding the JavaScript Code**:
   - `getAccessibilityAnalysis`: This function performs the accessibility analysis based on the provided input data and returns recommendations. It uses PhysarAI to understand the goal, analyze options and generate recommendations.
   - Other utility functions handle JSON validation, fetching data, and key extraction.

4. **HTML Usage**:
   - The HTML file (`index.html`) provides a simple interface to trigger the accessibility analysis.
   - Clicking the "Get Accessibility Information" button initiates the process.

5. **Providing Input Data**:
   - Modify the `inputData` object in the HTML file to reflect the accessibility assessment of your technologies.
   - Ensure the structure matches the provided example, including product names, assessment questions, and final scores.

6. **Executing the Analysis**:
   - Upon clicking the button, the JavaScript code calls `getAccessibilityAnalysis` with a license key (if required) and the input data.
   - The license key, if needed, should be provided as a string within the `licenseKey` variable in the HTML file.

7. **Viewing Recommendations**:
   - Once the analysis is complete, the HTML page displays a table summarizing recommendations.
   - Recommendations include technology, diagnosis, recommendation, impact estimate, and recommended sites.

## Notes:

- **Processing Time**: The `getAccessibilityAnalysis` function takes approximately 60 seconds to complete its execution. Therefore, when designing the user interface, it's crucial to account for this delay to provide a seamless experience for the end user.

- **Non-Deterministic Results**: The results produced by the function are non-deterministic. Even with the same input data, the function may generate different variations of the output. It's essential to set proper user expectations and inform them about this variability beforehand.

- **Intermittent Failures**: The function may experience intermittent failures. If this occurs, it's worth retrying the function, as sometimes it works after retrying. However, be aware that retrying may potentially increase the wait time to 2 minutes or more.

### Schema and Examples:

- **Schema and Examples**: Examples of input, output recommendations, and schemas can be found in the `assets/json` folder.

- **Potential Mistakes**: This functionality is based on technology that can make mistakes. While the information provided can be valuable, there is a possibility of errors. It's advised to use the generated recommendations as a reference and verify them thoroughly before implementation. Users should be cautioned about the possibility of inaccuracies and encouraged to double-check the recommendations.

### Creating a Satisfying User Experience:

Given the potential delays in processing and intermittent failures, here are some suggestions for creating a satisfying user experience:
- **Offline Report Sending**: Offer users the option to receive the report offline later via email or download link.
- **Estimated Countdown**: Provide an estimated countdown or progress bar to indicate the remaining processing time.
- **Interactive Loading Screen**: Design an interactive loading screen with engaging visuals or messages to keep users informed and entertained during the processing period.
- **Progressive Disclosure**: Display partial results or interim progress updates to keep users informed about the ongoing analysis.
- **Error Handling**: Implement robust error handling mechanisms to gracefully handle intermittent failures and provide clear instructions to users on how to retry or proceed.



## Keep in Mind:

- **Processing Time**: The `getAccessibilityAnalysis` function takes approximately 60 seconds to complete its execution. Therefore, when designing the user interface, it's crucial to account for this delay to provide a seamless experience for the end user.

- **Non-Deterministic Results**: The results produced by the function are non-deterministic. Even with the same input data, the function may generate different variations of the output. It's essential to set proper user expectations and inform them about this variability beforehand.

- **Potential Mistakes**: This functionality is based on technology that can make mistakes. While the information provided can be valuable, there is a possibility of errors. It's advised to use the generated recommendations as a reference and verify them thoroughly before implementation. Users should be cautioned about the possibility of inaccuracies and encouraged to double-check the recommendations.


## Conclusion:

This README serves as a guide to using the provided JavaScript code for generating accessibility recommendations based on input assessments. For further customization or integration into your project, refer to the code comments and modify as needed. If you encounter any issues or have questions, don't hesitate to reach out for assistance.
