# LIB_GraphAPI

## Description
This library interacts with the O365 actions to perform Email & SharePoint actions.
Dependencies used:
"UiPath.MicrosoftOffice365.Activities": "2.4.3"
 "UiPath.System.Activities": "23.4.5"

## Features
- [Activity-1](#activity-1-create-folder)
- [Activity-2](#activity-2-download-file)
- [Activity-3](#activity-3-files-or-folders-exist)
- [Activity-4](#activity-4-get-files-or-folders)
- [Activity-5](#activity-5-get-list-item-field-value)
- [Activity-6](#activity-6-read-email)
- [Activity-7](#activity-7-send-email)
- [Activity-8](#activity-8-update-list-item)
- [Activity-9](#activity-9-upload-file)
- [Activity-10](#activity-10-delete-file)
- [Activity-11](#activity-11-get-list-items)



## Activity 1: Create Folder 
 
### Details:
  - This reusable activity uses the Microsoft Graph API to create a new folder in SharePoint.

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used). 
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strSharepointURL- This will hold the share point URL.
<br/>in_strSharepointNewFolderName - Name of the new folder being created.
<br/>in_strSharepointParentFolderPath - Folder path from root level.
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path.
<br/>out_boolFolderCreated - boolean to check if folder was created.

- Table Content : 

    | Command | Description |
    | --- | --- |
    | Input | in_strApplicationSecretAssetName : string; in_strApplicationIDAssetName: string; in_strTenantIDAssetName: string; in_strSharepointURL: string; in_strSharepointNewFolderName: string; in_strSharepointParentFolderPath: string ; in_strOrchestratorFolderPath : string |
    | Output | out_boolFolderCreated: bool |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |
 
- [Back to menu](#features)


## Activity 2: Download File

### Details:
  - This reusable activity uses the Microsoft Graph API to Download file from SharePoint.

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strParentDriveItemOptional- Drive item variable for upload file(optional).
<br/>in_strSpParentFolderPath - Folder path from root level.
<br/>in_strShareppointURL- This will holds the share point URL.
<br/>in_strLocalFilepath - This will holds the local full file path.
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path.
<br/>in_strDelay: Delay in "hh:mm:ss" format (example = "00:01:00").
<br/>out_boolFileDownloaded- This will result the status of download file.
<br/>out_strDownloadedFilepath- This will results the Downloaded file path.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strDelay : string; in_strOrchestratorFolderPath : string; in_strLocalFilepath : string; in_strShareppointURL : string; in_strSpParentFolderPath : string; in_ strParentDriveItemOptional : string; |
    | Output | out_strDownloadedFilepath : string ; out_boolFileDownloaded : bool ; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 3: Files or Folders Exist

### Details:
- This reusable activity uses the Microsoft Graph to retrieve the Files and Folders in a specified SharePoint site.

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strSharepointURL - URL for SharePoint site.
<br/>in_strSharepointSubfolder - sub folder path to search the file or folder.
<br/>in_strSharepointFileFolderToSearch - Name of the file or folder to search.
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path.
<br/>out_boolResultFileFolderFound - Boolean to denote if the file or folder was found.
<br/>out_intResultCount - The number of results found.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strSharepointSubfolder: string; in_strOrchestratorFolderPath : string; in_strSharepointFileFolderToSearch: string; in_strShareppointURL : string; |
    | Output | out_ intResultCount: int ; out_ boolResultFileFolderFound: bool ; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 4: Get Files¬ or Folders

### Details:
This activity uses the Microsoft Graph API to retrieve the Files and Folders in a specified SharePoint site.

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strSharepointURL - URL for SharePoint site.
<br/>in_strSharepointSubfolder - sub folder path to search the file or folder.
<br/>in_strSharepointFileFolderToSearch - Name of the file or folder to search.
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path.
<br/>out_boolResultFileFolderFound - Boolean to denote if the file or folder was found.
<br/>out_diResultDriveItems - List of Drive Items.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strSharepointSubfolder: string; in_strOrchestratorFolderPath : string; in_strSharepointFileFolderToSearch: string; in_strShareppointURL : string; |
    | Output | out_ diResultDriveItems: list ; out_ boolResultFileFolderFound: bool ; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 5: Get List Item Field Value

### Details:
-This activity Uses the Microsoft Graph API to get the list item field value from SharePoint site.


<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strSharepointURL- URL of the process SharePoint site.
<br/>in_FilterCondition-Filter condition to filter the list items and get the column value.
<br/>in_strSharepointListName- Name of the SharePoint list in the site.
<br/>in_ColumnDisplayName- Display name of the column to retrieve from the SharePoint list
<br/>in_strOrchestratorFolderPath: Orchestrator folder path to connect. 
<br/>out_FieldValue - Extracted value from the respective column.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_FilterCondition: string; in_strOrchestratorFolderPath : string; in_strSharepointListName: string; in_strShareppointURL : string; in_ColumnDisplayName  : string;|
    | Output | out_ FieldValue: string; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)



## Activity 6: Read Email

### Details:
- This workflow Uses the Microsoft Graph Get message and List messages APIs to retrieve the matching messages from a specified mailbox (in_MailAccount).

<br/>After performing the search, the activity returns an array of the matching Office365Message objects (Result_Email_List) that you can use as input variables in subsequent activities (e.g., Forward Mail and Move Mail).
<br/>The output will be a list of O365MailMessages.

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strEmailAccount - The email address, with which to interact.
<br/>in_strEmailFolder-  The mail folder, from which the messages are to be retrieved.
<br/>in_intEmailRetrievalCount- The maximum number of mails that are to be retrieved. It is mandatory to provide a mail count.
<br/>in_strEmailFilter- Query used for filtering the returned emails. If the query is not completed, all emails are returned. 
<br/>in_boolMarkEmailAsRead-  If True, the returned messages are marked as read.
<br/>out_listResultEmail - Returns all emails from the user's inbox. This field supports only Office365Message[] variables. 
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strEmailAccount : string; in_strOrchestratorFolderPath : string; in_strEmailFolder: string; in_intEmailRetrievalCount: int ; in_strEmailFilter  : string; in_boolMarkEmailAsRead  : bool;|
    | Output | out_ listResultEmail: list ; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 7: Send Email

### Details:
- This workflow uses the Microsoft Graph Create message and Send mail APIs to send a message (Body and Subject) to one or more recipients (To, CC, and BCC). This activity also gives you the option to include one or more attachments (Attachments) with your message.

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strMailBody - The body of the mail, that is to be sent. ( In HTML format)
<br/>in_strMailSubject - The mail subject of the mail that is to be sent.
<br/>in_strMailAccount- The mail account that is being used to send the mail. 
<br/>in_strMailRecipientCC - String array of the recipients to which the mail is to be CC'ed. ( A comma-separated list of email addresses that you want to be included as Cc recipients.)
<br/>in_strMailRecipientTo - String array of the recipients to which the mail has to be sent. ( A comma-separated list of email addresses that you want to send your mail to. )
<br/>in_strListOfAttachments - List of files that are to be attached with the mail.
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strMailBody: string; in_strOrchestratorFolderPath : string; in_strMailSubject: string; in_strMailRecipientTo: string  ; in_ListOfAttachments: list ; in_strMailRecipientCC: string ; in_strMailAccount : string ;|
    | Output | NA |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 8: Update List Item

### Details:
-This activity uses the Microsoft Graph API to update the list item in a specified SharePoint site.


<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strSharepointURL- URL of the process sharepoint site
<br/>in_FilterCondition-Filter condition to filter the list items and get the column value
<br/>in_strSharepointListName- Name of the sharepoint list in the site
<br/>in_ColumnDisplayName- Display name of the column to retrive from the sharepoint list
<br/> in_ValueToBeUpdated - New value to be updated against the defined column name
<br/>in_ strOrchestratorFolderPath – orchestrator folder path to connect

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_FilterCondition: string; in_strOrchestratorFolderPath : string; in_strSharepointURL : string; in_strSharepointListName: string; in_ColumnDisplayName: string; in_ValueToBeUpdated : string;|
    | Output | NA |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 9: Upload File

### Details:
-This activity uses the Microsoft Graph API to upload file in SharePoint

<br/>List of arguments used:
<br/>in_ApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_ApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_TenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strParentDriveItemOptional- Drive item variable for upload file(optional).
<br/>in_strSharepointParentFolderPath - Folder path from root level.
<br/>in_strSharepointUploadFilePath - directory path of the file to be uploaded.
<br/>in_strSharepointURL - URL of the sharepoint site.
<br/>out_boolFileUploaded - Boolean if the file has been uploaded.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strParentDriveItemOptional: string; in_strOrchestratorFolderPath : string; in_strSharepointURL : string; in_strSharepointParentFolderPath: string; in_strSharepointUploadFilePath: string;|
    | Output | out_ boolFileUploaded : bool; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)


## Activity 10: Delete File

### Details:
-This workflow uses the Microsoft Graph api to Delete file from sharepoint

<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strParentDriveItemOptional- Drive item variable for upload file(optional)
<br/>in_strSpParentFolderPath - Folder path from root level.
<br/>in_strShareppointURL- This will holds the share point URL.
<br/>in_strOrchestratorFolderPath - Name of the Orchestrator Folder Path.
<br/>out_boolFileDeleted : boolean result file deleted or not.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_strParentDriveItemOptional: string; in_strOrchestratorFolderPath : string; in_strSharepointURL : string; in_strSpParentFolderPath: string;|
    | Output | out_boolFileDeleted : bool; |
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)

## Activity 11: Get List Items

### Details:
-This workflow Uses the Microsoft Graph to get the list item field value from sharepoint site.
<br/>List of arguments used:
<br/>in_strApplicationSecretAssetName - Name of the asset containing the Application Secret ID - Secure String (Password of the credential is being used).
<br/>in_strApplicationIDAssetName- Name of the asset containing the Application ID.
<br/>in_strTenantIDAssetName- Name of the asset containing the Tenant ID.
<br/>in_strSharepointURL- URL of the process sharepoint site.
<br/>in_FilterCondition-Filter condition to filter the list items and get the column value.
<br/>in_strSharepointListName- Name of the sharepoint list in the site.
<br/>in_arrColumnNames-  columns list which we need to look in sharepoint.
<br/>in_strOrchestratorFolderPath - Orchestartor path.
<br/>out_dt_ListItems - datable contains list of items.
<br/>out_intListItemCount - no of list items as integer value.

- Table Content: 

    | Command | Description |
    | --- | --- |
    | Input | in_strTenantIDAssetName : string; in_strApplicationIDAssetName  : string;  in_strApplicationSecretAssetName : string; in_FilterCondition: string; in_strOrchestratorFolderPath : string; in_strSharepointURL : string; in_arrColumnNames: array; in_strSharepointListName :string;|
    | Output | out_dt_ListItems : datatable; out_intListItemCount :int;|
    | Input/Output | NA |
    | Requirements | NA |
    | App Version | NA |



- [Back to menu](#features)
