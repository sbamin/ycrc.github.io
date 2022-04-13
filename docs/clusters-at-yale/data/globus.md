# Large Transfers with Globus

For large data transfers both within Yale and to external collaborators, we recommend using Globus. Globus is a file transfer service that is efficient and easy to use. It has several advantages:

* Robust and fast transfers of large files and/or large collections of files.
* Files can be transferred between your computer and the clusters.
* Files can be transferred between Yale and other sites.
* A web and command-line interface for starting and monitoring transfers.
* Access to specific files or directories granted to external collaborators in a secure way.

Globus transfers data between computers set up as "endpoints". The official YCRC endpoints are listed below. Transfers can be to and from these endpoints or those you have defined for yourself with [Globus Connect](#setup-an-endpoint-on-your-computer).

## Cluster Endpoints

We currently support endpoints for the following clusters.

| Cluster                                     | Globus Endpoint |
|---------------------------------------------|-----------------|
| [Farnam](/clusters-at-yale/clusters/farnam) | `yale#farnam`   |
| [Grace](/clusters-at-yale/clusters/grace)   | `yale#grace`    |
| [Ruddle](/clusters-at-yale/clusters/ruddle) | `yale#ruddle`   |

These endpoints provide access to all files you normally have access to, except sequencing data on Ruddle.

## Get Started with Globus

1. In a browser, go to [app.globus.org](https://app.globus.org/).
1. Use the pull-down menu to select Yale and click "Continue".
1. If you are not already logged into CAS, you will be prompted to log in.
    1. [First login only] Do not associate with another account yet unless you are familiar with doing this
    1. [First login only] Select "non-profit research or educational purposes"
    1. [First login only] Click on "Allow" for allowing Globus Web App
1. From the [file manager interface](https://app.globus.org/file-manager) enter the name of the endpoint you would like to browse in the collection field (e.g. yale#farnam)
1. Click on the right-hand side menu option "Transfer or Sync to..."
1. Enter the second endpoint name in the right search box (e.g. another cluster or your personal endpoint)
1. Select one or more files you would like to transfer and click the appropriate start button on the bottom.
2. To complete a partial transfer, you can click the "sync" checkbox in the Transfer Setting window on the Globus page, and hten Globus should resume the transfer where it left off.

### Manage Your Endpoints

To manage your endpoints, such as delete an endpoint, rename it, or share it with additional people (be aware, they will be able to access your storage), go to [Manage Endpoint](https://app.globus.org/endpoints) on the Globus website.

### Sharing Data Using Globus

1. From the [file manager interface](https://app.globus.org/file-manager) enter the name of the endpoint you would like to share from in the collection field (e.g. yale#grace)
1. Click the Share button on the right
1. Click on "Add a Shared Endpoint"
1. Next to Path, click "Browse" to find and select the directory you want to share
1. Add other details as desired and click on "Create Share"
1. Click on "Add Permissions -- Share With"
1. Under "Username or Email" enter the e-mail address of the person that you want to share the data with, then click on "Save", then click on "Add Permission"
1. Do not select "write" unless you want the person you are sharing the data with to be able to write to the share.

For more information, please see the [official Globus Documentation](https://docs.globus.org/how-to).

## Setup an Endpoint on Your Computer

You can set up your own endpoint for transferring data to and from your own computer with [Globus Connect Personal](https://www.globus.org/globus-connect). 

To transfer or share data between two personal endpoints, you will need to request access to the YCRC's Globus Plus subscription on [this page](https://app.globus.org/groups/8f3fced6-4318-11e3-9f63-12313809f035/join).


## Setup a Google Drive Endpoint

The Globus connector is configured to only allow data to be uploaded into EliApps (Yale's GSuite for Education) Google Drive accounts. If you don't have an EliApps account, request one as described above.

1. To set up your Globus Google Drive endpoint, click on the following link: [Setup Globus Google Drive Endpoint](https://app.globus.org/file-manager?origin_id=28ae8ae7-b2c6-47b4-badc-da9c1cab1e6e)
1. Log into Globus, if needed.
1. The first time you login to the Globus Google Drive endpoint, you will be presented with a permissions approval page. If you are ok with the Connector manipulating your files through Globus (which is required), click the Allow button.
1. You may see your Yale EliApps account expressed in an uncommon format, such as netid@yale.edu@accounts.google.com. This is normal, and expected.
1. After your approvals you will be directed to the Globus File Manager, with the default view of "/My Drive". To see "/Team Drives" and other Google Drive features use the "up one folder" arrow icon in the File Manager.
2. To transfer to or from your Google Drive, search in the Collection field for "YCRC Globus Google Drive Collection".

!!! note 
    There are "rate limits" to how much data and how many files you can transfer in any 24 hours period. If you have hit your rate limit, Globus should automatically resume the transfer during the next 24 hour period. You see a "Endpoint Busy" error during this time.

    Google has a 400,000 file limit per [Shared Drive](/data/google-drive), so if you are archiving data to Google Drive, it is better to compress folders that contain lots of small files (e.g. using [tar](/online-tutorials)) before transferring. 

In our testing, we have seen up to 10MB/s upload and 100MB/s download speeds.

## Setup a S3 Endpoint

We support creating Globus S3 endpoints. To request a Globus S3 Endpoint, please [contact YCRC](https://docs.ycrc.yale.edu/#web-and-email-support). Please include in your request:

- S3 bucket name
- The [Amazon Region](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-available-regions) for that bucket
- An initial list of Yale NetIDs who should be able to access the bucket

!!! warning
    Please DO NOT send us the Amazon login credentials through an insecure method such as email or our ticketing system.

After we have created your Globus S3 endpoint, you will be able to further self-serve you own access controls with the Globus portal.
