Publisher: Splunk\
App Version: 3.2.0\
Product Vendor: Google\
Product Name: Google Sheets\
Product Version Supported (regex): ".*"\
This app allows various file manipulation actions to be performed on Google Sheets

This app requires a pre-configured service account to operate. Please follow the procedure outlined below.

Step 1: Create a project
------------------------

1. Go to [Google Cloud](https://console.developers.google.com) and sign in as a super administrator. If it's your first time signing in to the console, agree to the Terms of Service.
2. Click **IAM &amp; Admin** &gt; **Manage Resources**. You might have to click Menu first.
3. At the top, click **Create Project** and enter a project name.
4. (Optional) To add the project to a folder, for **Location**, click **Browse**, navigate to the folder, and click **Select**.
5. Click **Create**.
6. By default, only the creator of the project has rights to manage the project. To ensure the project can be maintained if the creator leaves the organization, you should assign at least one other person the role of Project Owner. For details, go to [Manage access to projects, folders, and organizations](https://cloud.google.com/iam/docs/granting-changing-revoking-access).

Step 2: Turn on the APIs for the service account
------------------------------------------------

1. Go to [Google Cloud Console](https://console.cloud.google.com/) and select the project you created above in Step:1 from the dropdown list on the top.
2. Click **APIs &amp; Services** &gt; **Library**. You might have to click Menu first.
3. For each API you require (below), click the API name and then Enable: 
    1. Google Sheets API
    2. Identity and Access Management (IAM) API
    3. Google Drive API
       
 **Tip:** If you can't find the API, specify the API name in the search box.


Step 3: Create the service account
----------------------------------

1. Click **APIs &amp; Services** &gt; **Credentials**. You might have to click Menu first.
2. Click **Create Credentials** &gt; **Service account**.
3. For **Service account name**, enter a name for the service account.
4. (Optional) For **Service account description**, enter a description of the service account.
5. Click **Create and Continue**.
6. Click **Done** &gt; **Save**.
7. Select the service account you just created and note down the email ID.  **You'll need it later while creating an asset for the connector (service\_account\_email).**
8. At the top, click **Keys** &gt; **Add Key** &gt; **Create new key**.
9. Make sure the key type is set to **JSON** and click **Create**.  You'll get a message that the service account's private key JSON file was downloaded to your computer. Make a note of the file name and where your browser saves it. **You'll need it later while creating an asset for the connector (service\_account\_credentials).**
10. Click **Close**.
11. At the top, click **Permissions**.
12. Click Grant Access
13. In **Add Principals** field, enter the service account email ID.
14. In **Assign roles** select Service Account Admin
15. If the google sheet you are trying to modify is not created from the same service account then open the sheet &gt; Share &gt; Enter the service account email ID &gt; give editor access and click on done before using this app.
