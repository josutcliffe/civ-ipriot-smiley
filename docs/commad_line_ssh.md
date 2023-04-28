# Command line instructions

##### To upload code to a Raspberry Pi via SSH on PowerShell, follow these steps

1. Verify the Raspberry Pi's IP address: 
Ensure your Raspberry Pi is connected to the same network as your computer. Find the hostname, which should be in the format `pi-XX.local`, where `XX` is the 2-digit number on the sticker on the Raspberry Pi.

2. Test the SSH connection: 
In PowerShell, enter the following command, replacing `XX` with the 2-digit number from the sticker:

```bash
ssh pi@pi-XX.local
```

3. Enter the password when prompted. In this case, the password is `Pi3.14`.

4. If the connection is successful, you will see the Raspberry Pi terminal. You can now navigate the Raspberry Pi's file system using Linux commands.


##### To upload a file to the Raspberry Pi

1. Navigate to the directory containing the file you want to upload using the `cd` command:

```bash
cd path\to\your\file
```

2. Use the SCP (Secure Copy) command to transfer the file to the Raspberry Pi. Replace `your_file.extension` with the actual filename and extension, and `XX` with the 2-digit number from the sticker:

```bash
scp .\your_file.extension pi@pi-XX.local:/path/on/pi
```
**Tip**: add the `-r` switch to copy a directory.

3. Enter the password (`Pi3.14`) when prompted.

The file will be uploaded to the specified directory on the Raspberry Pi. You can use the SSH connection from step 4 to navigate to the destination directory and verify the file is present.

When you have finished uploading files and managing the Raspberry Pi, type `exit` in the SSH terminal to close the connection.

That's it! 

You have successfully uploaded code to a Raspberry Pi via SSH using PowerShell.