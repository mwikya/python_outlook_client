# Simple Python(Django) Outlook Client
A simple Python web app that retrieves messages in Office 365 or Outlook.com.This app uses [Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)  to access Outlook mail, calendar, and contacts.

## Prerequisites

### Register the app

-  Open a browser and navigate to the Azure [ Azure Active Directory admin center](https://aad.portal.azure.com/) . Login using a personal account (aka: Microsoft Account) or Work or School Account.

- Select **Azure Active Directory** in the left-hand navigation, then select **App registrations (Preview) ** under **Manage.**

- Select New registration. On the Register an application page, set the values as follows.

	1. Set **Name** to Python Outlook Tutorial.
	2. Set **Supported account types** to** Accounts in any organizational directory and personal Microsoft accounts**.
	3.     Under **Redirect URI**, set the first drop-down to **Web** and set the value to http://localhost:8000/tutorial/gettoken/.

>- Choose **Register**. On the **Python Outlook Tutorial** page, copy the value of the **Application (client) ID** and assign it to ***OUTLOOK_CLIENT_ID*** in python_tutorial/settings.py.

- Select **Authentication** under **Manage**. Locate the **Implicit grant** section and enable **ID tokens**. Choose **Save**.

- Select **Certificates & secrets** under **Manage**. Select the **New client secret** button. Enter a value in **Description** and select one of the options for **Expires** and choose **Add**.

>- Copy the client secret value before you leave this page, and assign it to ***OUTLOOK_CLIENT_SECRET*** in python_tutorial/settings.py
>
>>	==Important==
>
>	This client secret is never shown again, so make sure you copy it now.
	
## Getting Started

