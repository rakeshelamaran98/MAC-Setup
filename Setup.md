# Requirements: UTM, Kali Linux, Metasploitable

Download Links:
- UTM: https://mac.getutm.app
- Kali: https://www.kali.org/get-kali/#kali-platforms
- Refer to this Blog For Setting Up Kali Linux on UTM, 
- https://medium.com/@cybersecfe/how-to-install-kali-linux-on-utm-on-m2-m1-macbook-bf04c6ce7031

---
# Steps to Setup Metasploitable 2 on UTM:

- Download Metasploitable-2 Linux and Extract image
- Open UTM and create a new VM (button with symbol +) . Select Emulate.
- Select Other under Operating System and on the following screen select None.
- On the following screen under “Hardware”, you can optionally optimize Memory size. You can also leave it on a default setting, but 1024 MB is enough.
- Click through the next few screens until you get to the Summary screen. On Summary screen, select Open VM Settings and click Save.
- Change the name of the VM.
- Select QEMU in the sidebar and uncheck UEFI Boot
- Go to Drives and delete IDE Drive
- In the Drives section, click on New Drive, and then on Import.
- Go to your Metasploitable-2 folder and select the file ending in .vmdk
- Click Save and run your new Metasploitable-2
- After you clicked on Start your machine, several process will start running.
- At the end you will see a msg Login with msfadmin/msfadmin to get started.
- Use msfadmin as both the username and password.
