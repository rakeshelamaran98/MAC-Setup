# Requirements: UTM, Kali Linux, Metasploitable

Download Links:
- UTM: https://mac.getutm.app
- Kali: https://www.kali.org/get-kali/#kali-platforms
- Metasploitable: https://sourceforge.net/projects/metasploitable/ (or) From Onedrive
- Refer to this Blog For Setting Up Kali Linux on UTM, 
- https://medium.com/@cybersecfe/how-to-install-kali-linux-on-utm-on-m2-m1-macbook-bf04c6ce7031

---
# Steps to Set Up Metasploitable 2 on UTM:

- Download Metasploitable-2 Linux and Extract image
- Open UTM and create a new VM (button with symbol +) . Select Emulate.
- Select Other under Operating System and on the following screen select None.
- On the following screen under “Hardware”, you can optionally optimize Memory size. You can also leave it on a default setting, but 1024 MB is enough.
- Click through the next few screens until you get to the Summary screen. On the Summary screen, select Open VM Settings and click Save.
- Change the name of the VM.
- Select QEMU in the sidebar and uncheck UEFI Boot
- Go to Drives and delete the IDE Drive
- In the Drives section, click on New Drive, and then on Import.
- Go to your Metasploitable-2 folder and select the file ending in .vmdk
- Click Save and run your new Metasploitable-2
- Set Your System Like This,

<img width="801" alt="Screenshot 2025-05-01 at 3 57 49 PM" src="https://github.com/user-attachments/assets/7bf2c125-e39e-4100-a687-c0665ae90555" />

- Set your Network Like this,
<img width="801" alt="Screenshot 2025-05-01 at 3 58 43 PM" src="https://github.com/user-attachments/assets/c2ce35c8-4a4a-4373-becf-3e700f32e4f6" />

- After you clicked on Start your machine, several process will start running.
- At the end you will see a msg Login with msfadmin/msfadmin to get started.
- Use msfadmin as both the username and password.

# For PMA Machines:
- An .ova (Open Virtual Appliance) file is just a tar archive that bundles:
- *.ovf → XML-based config file (hardware layout)
- *.vmdk → Virtual hard disk(s)
- Optional *.mf → Manifest file (hash checksums)
- This is a format primarily used by VirtualBox and VMware
- UTM doesn’t support importing .ova directly.
- Instead, UTM lets you manually create a VM and attach a disk (like a .vmdk or .qcow2) to it.

# Extract the OVA:
- Go to Mac Terminal
- Use this command to extract

```
tar -xvf <your-pma-filename>.ova
```
- You’ll get .ovf and .vmdk files.
- Converting to .Qcow2 is also another option if .vmdk conversion not working or fails to boot try .qcow2

# Importing Vmdk:
- Repeat the Steps (Refer Metasploit Setup)
- Create a new VM manually
- Attach the .vmdk as a Disk Image (IDE or VirtIO interface)
- Boot the VM
