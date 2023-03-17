=== "Google Drive"
    
    The example below is a screen dump when setting up `rclone` on Farnam for Google Drive.
    
    ```bash
    [pl543@c03n06 ~]$ rclone config
    No remotes found - make a new one
    n) New remote
    s) Set configuration password
    q) Quit config
    n/s/q> n
    name> remote
    Type of storage to configure.
    Enter a string value. Press Enter for the default ("").
    Choose a number from below, or type in your own value
     1 / 1Fichier
       \ "fichier"
     2 / Alias for an existing remote
       \ "alias"
    [...]
    15 / Google Drive
       \ "drive"
    [...]
    42 / seafile
       \ "seafile"
    Storage> 15
    ** See help for drive backend at: https://rclone.org/drive/ **
    
    Google Application Client Id
    Setting your own is recommended.
    See https://rclone.org/drive/#making-your-own-client-id for how to create your own.
    If you leave this blank, it will use an internal key which is low performance.
    Enter a string value. Press Enter for the default ("").
    client_id> 
    OAuth Client Secret
    Leave blank normally.
    Enter a string value. Press Enter for the default ("").
    client_secret> 
    Scope that rclone should use when requesting access from drive.
    Enter a string value. Press Enter for the default ("").
    Choose a number from below, or type in your own value
     1 / Full access all files, excluding Application Data Folder.
       \ "drive"
     2 / Read-only access to file metadata and file contents.
       \ "drive.readonly"
       / Access to files created by rclone only.
     3 | These are visible in the drive website.
       | File authorization is revoked when the user deauthorizes the app.
       \ "drive.file"
       / Allows read and write access to the Application Data folder.
     4 | This is not visible in the drive website.
       \ "drive.appfolder"
       / Allows read-only access to file metadata but
     5 | does not allow any access to read or download file content.
       \ "drive.metadata.readonly"
    scope> 1
    ID of the root folder
    Leave blank normally.
    
    Fill in to access "Computers" folders (see docs), or for rclone to use
    a non root folder as its starting point.
    
    Enter a string value. Press Enter for the default ("").
    root_folder_id> 
    Service Account Credentials JSON file path 
    Leave blank normally.
    Needed only if you want use SA instead of interactive login.
    
    Leading `~` will be expanded in the file name as will environment variables such as `${RCLONE_CONFIG_DIR}`.
    
    Enter a string value. Press Enter for the default ("").
    service_account_file> 
    Edit advanced config? (y/n)
    y) Yes
    n) No (default)
    y/n> n
    Remote config
    Use auto config?
     * Say Y if not sure
     * Say N if you are working on a remote or headless machine
    y) Yes (default)
    n) No
    y/n> y
    If your browser doesn't open automatically go to the following link: http://127.0.0.1:53682/auth?state=6glRr_mpEORxHevlOaaYyw
    Log in and authorize rclone for access
    Waiting for code...
    Got code
    Configure this as a Shared Drive (Team Drive)?
    y) Yes
    n) No (default)
    y/n> n
    --------------------
    [remote]
    type = drive
    scope = drive
    token = {"access_token":"ya29.A0ArdaM-mBYFKBE2gieODvdANCZRV6Y8QHhQF-lY74E9fr1HTLOwwLRuoQQbO9P-Jdip62YYhqXfcuWT0KLKGdhUb9M8g2Z4XEQqoNLwZyA-FA2AAYYBqB","token_type":"Bearer","refresh_token":"1//0dDu3r6KVakgYIARAAGA0NwF-L9IrWIuG7_f44x-uLR2vvBocf4q-KnQVhlkm18TO2Fn0GjJp-cArWfj5kY84","expiry":"2021-02-25T17:28:18.629507046-05
    :00"}
    --------------------
    y) Yes this is OK (default)
    e) Edit this remote
    d) Delete this remote
    y/e/d> y
    Current remotes:
    
    Name                 Type
    ====                 ====
    remote               drive
    
    e) Edit existing remote
    n) New remote
    d) Delete remote
    r) Rename remote
    c) Copy remote
    s) Set configuration password
    q) Quit config
    e/n/d/r/c/s/q> q
    ```

    
    
=== "Box"
    
    The example below is a screen dump when setting up `rclone` on Farnam for Yale Box.

    ```bash
    [pl543@c14n07 ~]$ rclone config
    No remotes found - make a new one
    n) New remote
    s) Set configuration password
    q) Quit config
    n/s/q> n
    name> remote
    Type of storage to configure.
    Enter a string value. Press Enter for the default ("").
    Choose a number from below, or type in your own value
     1 / 1Fichier
       \ "fichier"
    [...]
     6 / Box
       \ "box"
    [...]
    Storage> box
    ** See help for box backend at: https://rclone.org/box/ **
    
    Box App Client Id.
    Leave blank normally.
    Enter a string value. Press Enter for the default ("").
    client_id> 
    Box App Client Secret
    Leave blank normally.
    Enter a string value. Press Enter for the default ("").
    client_secret> 
    Edit advanced config? (y/n)
    y) Yes
    n) No
    y/n> n
    Remote config
    Use auto config?
     * Say Y if not sure
     * Say N if you are working on a remote or headless machine
    y) Yes
    n) No
    y/n> y
    If your browser does not open automatically go to the following link: http://127.0.0.1:53682/auth
    Log in and authorize rclone for access
    Waiting for code...
    Got code
    --------------------
    [remote]
    type = box
    token = {"access_token":"PjIXHUZ34VQSmeUZ9r6bhc9ux44KMU0e","token_type":"bearer","refresh_token":"VumWPWP5Nd0M2C1GyfgfJL51zUeWPPVLc6VC6lBQduEPsQ9a6ibSor2dvHmyZ6B8","expiry":"2019-10-21T11:00:36.839586736-04:00"}
    --------------------
    y) Yes this is OK
    e) Edit this remote
    d) Delete this remote
    y/e/d> y
    Current remotes:
    
    Name                 Type
    ====                 ====
    remote               box
    
    e) Edit existing remote
    n) New remote
    d) Delete remote
    r) Rename remote
    c) Copy remote
    s) Set configuration password
    q) Quit config
    e/n/d/r/c/s/q> q
    ```
    