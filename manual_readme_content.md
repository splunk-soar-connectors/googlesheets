This app requires a pre-configured service account to operate. Please follow the procedure outlined below.

# Step 1: Create a project

1. Go to Google Cloud and sign in as a super administrator. If it's your first time signing in to the console, agree to the Terms of Service.
1. Click IAM & Admin > Manage Resources. You might have to click Menu first.
1. At the top, click Create Project and enter a project name.
1. (Optional) To add the project to a folder, for Location, click Browse, navigate to the folder, and click Select.
1. Click Create.
1. By default, only the creator of the project has rights to manage the project. To ensure the project can be maintained if the creator leaves the organization, you should assign at least one other person the role of Project Owner. For details, go to [Manage access to projects, folders, and organizations](https://cloud.google.com/iam/docs/granting-changing-revoking-access).

# Step 2: Turn on the APIs for the service account

1. Go to Google Cloud Console and select the project you created above in Step:1 from the dropdown list on the top.

1. Click APIs & Services > Library. You might have to click Menu first.

1. For each API you require (below), click the API name and then Enable:

   1. Google Sheets API
   1. Identity and Access Management (IAM) API
   1. Google Drive API

   **Tip**:If you can't find the API, specify the API name in the search box.

# Step 3: Create the service account

1. Click APIs & Services > Credentials. You might have to click Menu first.

1. Click Create Credentials > Service account.

1. For Service account name, enter a name for the service account.

1. (Optional) For Service account description, enter a description of the service account.

1. Click Create and Continue.

1. Click Done > Save.

1. Select the service account you just created and note down the email ID. You'll need it later while creating an asset for the connector (service_account_email).

1. At the top, click Keys > Add Key > Create new key.

1. Make sure the key type is set to JSON and click Create.

   You'll get a message that the service account's private key JSON file was downloaded to your computer. Make a note of the file name and where your browser saves it. **You'll need it later while creating an asset for the connector (service_account_credentials)**.

1. Click Close.

1. At the top, click Permissions.

1. Click Grant Access

1. In Add Principals field, enter the service account email ID.

1. In Assign roles select Service Account Admin

1. If the google sheet you are trying to modify is not created from the same service account then open the sheet > Share > Enter the service account email ID > give editor access and click on done before using this app.
