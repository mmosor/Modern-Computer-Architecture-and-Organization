__Modern Computer Architecture and Organization__, by Jim Ledin. Published by Packt Publishing
# Chapter 12, Exercise 1

Download and install the current version of Virtual Box. Download, install, and bring up Ubuntu Linux as a virtual machine within Virtual Box. Connect the guest OS to the Internet using a bridged network adapter. Configure and enable clipboard sharing and file sharing between the Ubuntu guest and your host operating system.

# Answer
1. Download the VirtualBox installer from https://www.virtualbox.org/wiki/Downloads. Be sure to select the version appropriate for your host operating system.

1. Run the VirtualBox installer and accept the default prompts.

1. Download a VirtualBox image of 64-bit Ubuntu Linux. One source for such an image is https://www.osboxes.org/ubuntu/. If the image is in a compressed format, uncompress it. Use 7-zip (https://www.7-zip.org/) if the filename ends with *.7z*. The VirtualBox disk image filename ends in *.vdi*.

1. Move the *.vdi* file to the folder where you want to run it from. If you don't have a preference, use yout **Documents** folder for this.

1. Start VirtualBox and click the **New** icon. Give the new machine a name, such as *Ubuntu*, select *Linux* as the type, and select *Ubuntu (64-bit)* as the version. Click **Next**.

1. In the **Memory size** dialog, accept the default memory size (or increase it if you prefer).

1. In the **Hard disk** dialog, select **Use an existing virtual hard disk file**. Click the browse button (it looks like a folder), then click the **Add** button in the **Hard disk selector** dialog. Navigate to the *.vdi* file you downloaded and select **Open**. Click **Create** to finish creating the virtual machine.

1. Click the **Settings** icon in VirtualBox. In the **General** section, **Advanced** tab, select *Bidirectional* for **Shared Clipboard**. 

1. Click **Network**. In the **Adapter 1** tab, select **Bridged Adapter** next to **Attached to:**.

1. Create a folder on the Windows disk named **share** in your **Documents** folder. Click **Shared Folders**. Click the icon to add a shared folder (it looks like a folder with a plus on it). Select the **share** folder on the host computer and click **OK**.

1. Click **OK** in the **Settings** dialog to close it.

1. Click the **Start** icon to start the virtual machine. When the Ubuntu system finishes booting, login with username *osboxes* and password *osboxes.org*.

1. After login has finished, open a terminal window by pressing *CTRL+ALT+T*.

1. Create a directory named *share* with this command: **mkdir share**

1. Enter this command to mount the shared folder: *sudo mount -t vboxsf -o rw,uid=1000,gid=1000 share ~/share