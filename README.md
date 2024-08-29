# Solving reCaptcha v2 Invisible Challenges: Identification and Parameters

![](https://assets.capsolver.com/prod/posts/solving-recaptcha-invisible/juHsE3uGZigy-3ffee69da3cb7568e82778b9714b3306.png)

## Overview

reCaptcha v2 Invisible is a type of CAPTCHA designed to provide security without disrupting the user experience. Unlike traditional CAPTCHAs, reCaptcha v2 Invisible does not require user interaction unless a suspicious activity is detected. This guide will walk you through the process of identifying and solving reCaptcha v2 Invisible challenges using [CapSolver](https://www.capsolver.com/?utm_source=official&utm_medium=blog&utm_campaign=recaptchaparameter) API.

## What is reCaptcha v2 Invisible?

reCaptcha v2 Invisible is a security challenge provided by Google that helps protect websites from bots and automated abuse while minimizing disruption to legitimate users. Here's a breakdown of its key features:

- **Invisible by Default**: The CAPTCHA challenge does not appear unless the system detects unusual behavior. For most users, the CAPTCHA is seamlessly integrated and unobtrusive.
- **Trigger Mechanism**: It activates based on user interactions that might indicate suspicious activity, such as an unusual browsing pattern or behavior that deviates from normal usage.
- **Token-Based Verification**: Once triggered, the CAPTCHA generates a token that must be verified by the website to confirm that the user is a human.

For a detailed explanation, you can visit the [official reCaptcha v2 Invisible page](https://www.google.com/recaptcha/about/invisible/).

## Bonus Code

> Claim Your   <u>**Bonus Code**</u> for top captcha solutions; [CapSolver](https://www.capsolver.com/?utm_source=official&utm_medium=blog&utm_campaign=recaptchainvisible): **WEBS**. After redeeming it, you will get an extra 5% bonus after each recharge, Unlimited
> 
> ![](https://assets.capsolver.com/prod/images/post/2024-03-29/fbc29472-886c-45b2-9eb2-2b307f6d9700.png)

## Identifying the Correct reCaptcha Version and Parameters

Before solving reCaptcha v2 Invisible, it’s essential to identify the correct version and parameters. This ensures that you are using the appropriate solving method.

### Step 1: Use the CapSolver Browser Extension

The [CapSolver Browser Extension](https://www.capsolver.com/blog/Extension/identify-any-captcha-and-parameters) is a user-friendly tool designed to accurately detect the version and parameters of reCaptcha challenges. It guarantees 100% accuracy in identifying CAPTCHA details.

#### Installation and Activation

1. **Download the Extension**: Obtain it from the [CapSolver website](https://www.capsolver.com/?utm_source=official&utm_medium=blog&utm_campaign=recaptchaparameter).
2. **Install the Extension**: Follow your browser's installation instructions to add the extension.
3. **Activate and Identify**: Navigate to the page with the reCaptcha challenge. The extension will automatically identify the reCaptcha version and display its parameters.

![CapSolver Extension Identification](https://assets.capsolver.com/prod/images/post/2023-11-06/ddf61de6-a736-421a-b186-482b3940afc7.png)

For detailed instructions, refer to the [Instruction Manual for reCaptcha Identification Extension](https://www.capsolver.com/blog/Extension/identify-any-captcha-and-parameters).

### Step 2: Retrieve the CapSolver JSON Data

Once you confirm that reCaptcha v2 Invisible is present and you’ve collected the necessary parameters, prepare a JSON request to send to CapSolver.

Here is an example of the JSON structure you should use:

![Capsolver JSON](https://assets.capsolver.com/prod/images/post/2023-11-06/9e3c36d0-123e-4568-a985-030ad6581401.png)

## Solving reCaptcha v2 Invisible

With the JSON data ready, you can now use CapSolver's API to solve the reCaptcha challenge.

### Step 3: Create a Task

Use the following JSON format to create a task with CapSolver:

```json
POST https://api.capsolver.com/createTask
Host: api.capsolver.com
Content-Type: application/json
{
    "clientKey": "YOUR_API_KEY",
    "task": {
        "type": "ReCaptchaV2TaskProxyLess",
        "websiteURL": "https://example.com",
        "websiteKey": "6LcR_okUAAAAAPYrPe-HK_0RULO1aZM15ENyM-Mf",
        "anchor": "value",
        "reload": "value",
        "isInvisible": true
    }
}
```

**Key Parameters**:
- `clientKey`: Your CapSolver API key.
- `websiteURL`: The URL where the reCaptcha challenge is located.
- `websiteKey`: The site key of the reCaptcha challenge (obtained from the page source).
- `isInvisible`: Set this to `true` to specify that the reCaptcha is invisible.

### Step 4: Retrieve the Result

After creating the task, you need to retrieve the result using the following request:

```json
POST https://api.capsolver.com/getTaskResult
Host: api.capsolver.com
Content-Type: application/json
{
    "clientKey": "YOUR_API_KEY",
    "taskId": "TASK_ID" // ID returned by the createTask request
}
```

**Important Notes**:
- Replace `TASK_ID` with the ID obtained from the `createTask` request.
- Monitor the task status and handle errors accordingly.

### Troubleshooting and Support

If you encounter issues where the CAPTCHA token is not functioning or if you need further assistance, please contact our [customer support team](https://www.capsolver.com/?utm_source=official&utm_medium=blog&utm_campaign=recaptchaparameter). Our team is available to provide solutions and support for any challenges you may face.

## Conclusion

By following these instructions, you can efficiently solve reCaptcha v2 Invisible challenges using CapSolver. For additional details and advanced configurations, refer to the [CapSolver Documentation](https://docs.capsolver.com/en/guide/getting-started/?utm_source=official&utm_medium=blog&utm_campaign=recaptchaparameter).

## Note on Compliance

> **Important:** When engaging in web scraping, it's crucial to adhere to legal and ethical guidelines. Always ensure that you have permission to scrape the target website, and respect the site's `robots.txt` file and terms of service. **CapSolver firmly opposes the misuse of our services for any non-compliant activities**. Misuse of automated tools to bypass CAPTCHAs without proper authorization can lead to legal consequences. Make sure your scraping activities are compliant with all applicable laws and regulations to avoid potential issues.
