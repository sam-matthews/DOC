SublimeSFTPDoc.md

To use the Sublime Text 2 FTP package, actually it's an add-on package, but essentially to setup, you do the following:

1. Install the SFTP package
2. Import a directory structure into the sidebar. 
3. Right click on the folder structure you want to send over to a remote host.
4. Open the remote mapping and make the following changes:


{
    "host": "nas",
    "user": "sam",
    "password": "sam",
    "port": "22",

    "remote_path": "/FTP/"
}

There are a few other options to update, but essentially these are the options to get you going. I would recommend you setup a SSH key so password is not required.

Once this file is setup, right click on the folder and sync the folder. SFTP package will display the commands which will be run with an option to run. This is quite nice as most FTP tools would just go ahead and run without asking.

The bueaty of this package is it keeps everything in sync. It doesn't look atomatically, which is probably a good thing. I can see some nice uses for this tool, particulary when I have some files I want to send to a remote server somewhere.

There are quite a few other options available. I can send this file I'm working on to the mapping location I created earlier. I can diff the files, upload the file, download the file or create a new location of the file.

 