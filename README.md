# Accessibility Recommendations Project README

This project aims to provide accessibility recommendations based on an input assessment of various technologies. The core functionality lies within the JavaScript code, particularly the `getAccessibilityAnalysis` function, which analyzes the input assessment and generates recommendations using a Language Model (LLM).

## How to Use

1. **Clone the Repository**: Start by cloning this repository to your local machine.

2. **Project Structure**: The project consists of HTML and JavaScript files, along with JSON files containing input examples and schemas.

3. **Understanding the JavaScript Code**:
   - `getAccessibilityAnalysis`: This function performs the accessibility analysis based on the provided input data and returns recommendations. It utilizes the `promptLLM` function to interact with a Language Model (LLM) for generating recommendations.
   - `promptLLM`: Responsible for sending prompts to the LLM endpoint and retrieving AI-generated responses.
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

- **License Key**: If your setup requires a license key for accessing the LLM endpoint, ensure you provide it within the `licenseKey` variable in the HTML file.
- **Modification**: Feel free to modify the HTML structure or JavaScript code to suit your project's requirements.
- **Error Handling**: The code includes error handling to gracefully manage exceptions during execution. Check the console for any error messages.

## Important Notes:

- **Processing Time**: The `getAccessibilityAnalysis` function takes approximately 60 seconds to complete its execution. Therefore, when designing the user interface, it's crucial to account for this delay to provide a seamless experience for the end user.

- **Non-Deterministic Results**: The results produced by the function are non-deterministic. Even with the same input data, the function may generate different variations of the output. It's essential to set proper user expectations and inform them about this variability beforehand.

- **Potential Mistakes**: This functionality is based on technology that can make mistakes. While the information provided can be valuable, there is a possibility of errors. It's advised to use the generated recommendations as a reference and verify them thoroughly before implementation. Users should be cautioned about the possibility of inaccuracies and encouraged to double-check the recommendations.


## Conclusion:

This README serves as a guide to using the provided JavaScript code for generating accessibility recommendations based on input assessments. For further customization or integration into your project, refer to the code comments and modify as needed. If you encounter any issues or have questions, don't hesitate to reach out for assistance.
