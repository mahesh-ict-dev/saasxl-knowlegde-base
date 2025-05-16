---
sidebar_position: 1
---

# DataGOL User Guide

## Creating User Accounts

The first user to create an account with a new domain becomes the account admin by default.

1. Go to the DataGOL Sign in page and click the **Create an Account** option.  
   <img src="/img/att_128_for_220692503.png" alt="Create Account Option" />

2. In the **Welcome** dialog box, enter a valid email ID and click **Continue**. Providing a valid email ID is mandatory.  
   <img src="/img/att_129_for_220692503.png" alt="Welcome Dialog" />

3. In the **Create your account** dialog box, specify the following details:  
   <img src="/img/att_103_for_220692503.png" alt="Create Account Fields" />  
   - **First name**  
   - **Last name**  
   - **Password**  
   - **Confirm Password** 
   Click - **Submit** Button

4. Verify the email account. A verification email is sent from DataGOL `<no-reply@datagol.ai>`.

5. Once the user’s email address is verified, the user can log in using the email address and password configured.  
   <img src="/img/att_130_for_220692503.png" alt="Login Screen" />  
   <img src="/img/att_11_for_220692503.png" alt="Login Fields" />

The new user created as above will have a default role **User**. New Roles can be assigned by account admins. Users can update their general information and reset their password from the **User** section under **Accounts**.  
<img src="/img/image-20250505-063830.png" alt="User Settings" />  
<img src="/img/image-20250505-063744.png" alt="Accounts Section" />

Alternatively, you can **Login with Google** using your company email address if available. However, DataGOL recommends not using Gmail addresses as this functionality will not be available in the future.  
<img src="/img/att_131_for_220692503.png" alt="Login with Google" />

---

## Inviting Team Members

You can invite team members to DataGOL to quickly expand your team and ensure that new members have the appropriate access. Only users with roles **Account Admin** and **User Admin** are allowed to invite team members. External members cannot be invited to the team.

### Steps to Invite Team Members:

1. On the DataGOL home page, from the right side, click the **Go to Team** button. This will take you to the Team page.  
   <img src="/img/image-20250506-125208.png" alt="Team Page" />

2. From the upper right side, click the **Invite** button. The **Invite a member** box is displayed.  
   <img src="/img/image-20250506-125413.png" alt="Invite Member" />

3. Specify an email address of the member you want to invite and select the appropriate role for the member from the available options. Roles determine the level of access and permissions of the new member.  
   - Only members with the company’s domain can invite others. External members cannot be invited to the team.

4. Click the **Invite** button. The invitation is sent to the specified member. After the invitation is sent, the newly invited member is shown at the top of the team list.

5. The invited team member needs to accept the invite using the **Accept Invitation** link received in the email from DataGOL `<no-reply@datagol.ai>`, which then redirects to the Login page. The invited user needs to create an account using the **Create Account** option as described above.

---

## Understanding Roles and Permissions in DataGOL

Roles are essential in managing access to various functionalities and data in DataGOL. Each role comes with specific permissions tailored to manage different functionalities, ensuring proper access control and security.

### Roles and Permissions:

| **Role**            | **Description**                                                                                     |
|----------------------|-----------------------------------------------------------------------------------------------------|
| **Account Admin**    | Comprehensive control over the platform, including company settings, user management, and more.     |
| **Lakehouse Admin**  | Manages lake houses and associated components, excluding company-wide settings and user management. |
| **Lakehouse Member** | Read-only access to lake houses and their components.                                               |
| **Copilot Admin**    | Manages copilots within the platform.                                                              |
| **Copilot Member**   | Read-only access to copilots.                                                                      |
| **Connectors Admin** | Manages connectors within the platform.                                                            |
| **Connectors Member**| Read-only access to connectors.                                                                    |
| **User Admin**       | Focuses on user administration, including creating, editing, and assigning roles.                  |
| **User**             | Can create, edit, and view workspaces, workbooks, and dashboards.                                  |

---

## Editing a Team Member's Role

To modify roles for team members:

1. Navigate to **Teams** from the left side of the Home page.  
2. On the Team page, click the corresponding member’s options and select **Edit**.  
3. In the **Assign roles** dialog, edit the roles as required and click **Update**.  
   <img src="/img/att_202_for_220692503.png" alt="Edit Roles" />  
   <img src="/img/att_237_for_220692503.png" alt="Assign Roles" />

## Special considerations for Account Admin Role

If you want to add roles to a member who is an Account Admin, the roles won’t be visible on the teams page initially. However, when you click the more options icon, all available roles will be displayed.
If you delete the Account Admin role and add another role, the new role will appear on the teams page.
For members who are not listed as Account Admins, click , and add different roles, and the changes are immediately reflected on the Teams page.


---

## Configuring REST API Access to DataGOL

DataGOL offers REST APIs to access workbook data. To configure REST API access:

1. On the Home page, select **Teams** from the left navigation panel.  
2. Click the **Service Accounts** tab and then click **+ Service Account**.  
   <img src="/img/att_159_for_220692503.png" alt="Service Account" />

3. Specify a name and description for the service account. Optionally, select the **Keep token active without expiration** checkbox.  
4. Click **Create**.  
5. Use the generated token in the `x-auth-token` header for API requests.  
   <img src="/img/att_160_for_220692503.png" alt="API Token" />

---

## Using Your Own AWS Storage with DataGOL

DataGOL integrates with AWS and Azure cloud storage. To configure your own AWS storage:

1. From the Home page, select **Company** from the left navigation panel.  
2. Select the **Keys** tab and click **Edit** to add your AWS Access Keys, Secret Key, Region, and Root Directory.  
   <img src="/img/image-20250506-164725.png" alt="AWS Keys" />

3. Click **Save Directory**. Ensure the root directory (AWS S3 Bucket) exists and has full access.

To configure Azure storage, follow similar steps by providing the Azure Account Name, Account Key, and Root Directory.


# Using your own AWS storage with DataGOL

DataGOL seamlessly integrates with both AWS and Azure cloud storage, offering you flexibility in choosing your primary data location. By default, DataGOL utilizes its own managed AWS and Azure resources for storage, ensuring immediate and hassle-free operation.

While the platform's default configuration with its own AWS access keys is recommended for most users, you have the option to designate a specific AWS account for all your organization's DataGOL storage needs. Similarly, while DataGOL provides its own managed Azure storage for smooth operation, you can also choose to use your own Azure account by providing the necessary access key credentials. This allows companies requiring specific account separation or integration with existing cloud infrastructure to tailor their DataGOL storage setup.

## To update AWS access keys

1. From the left side of the Home page, select **Company**.
2.  
   ![Company Settings](/img/image-20250506-135902.png)
3. Select the **Keys** tab.
4.  
   ![AWS Keys Tab](/img/image-20250506-164725.png)
5. Click **Edit** to add your:
   - AWS Access Key  
   - AWS Secret Key  
   - Region  
   - Root Directory
6. Click **Save Directory**.

> ⚠️ **Note:** If changing the AWS access keys, ensure that the root directory (AWS S3 Bucket) exists and the AWS account used has full access to that bucket.

---

## To update Azure access keys

1. From the left side of the Home page, select **Company**.
2. Select the **Keys** tab.
3.  
   ![Azure Keys Tab](/img/image-20250506-170104.png)
4. In the Azure settings box, click **Edit** to add your:
   - Azure Account Name  
   - Azure Account Key  
   - Root Directory
5. Click **Save Directory**.