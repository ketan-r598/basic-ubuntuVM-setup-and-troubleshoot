# Sharing Folders between Host OS and Guest OS in VirtualBox

Sharing folders between your Host OS and Guest OS in VirtualBox allows seamless file transfer. Here's a guide to achieve this:

## 1. Setting Up Shared Folder on Host OS

1. **Open VirtualBox:** Launch VirtualBox on your Host OS.
2. **Select Guest OS:** Right-click on the desired virtual machine (Guest OS) and choose "Settings" from the menu.
3. **Enable Shared Folders:** In the Settings window, navigate to the "Shared Folders" section.
4. **Add Shared Folder:** Click the "Add Shared Folder" button.
   - **Folder Path:** Specify the folder on your Host OS that you want to share. Use the dropdown menu and select "Other" to browse and select the desired folder.
   - **Folder Name:** Assign a name for the shared folder as it will appear on the Guest OS.
   - **Permissions:**
     - Read-only: Check this box if you only want the Guest OS to read files (not modify them).
     - Auto-mount: This option allows the shared folder to be automatically mounted on the Guest OS whenever it boots up.

## 2. Accessing Shared Folder on Guest OS

1. **Install Guest Additions (if not already):** Guest Additions are required for the Guest OS to recognize the shared folder. You can find the Guest Additions ISO in the VirtualBox menu or download it from the official VirtualBox website [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads). Install them following the Guest OS instructions.
2. **Guest OS Specific Access:** The way to access the shared folder depends on your Guest OS:
   - **Windows Guest OS:** Open File Explorer. You should see the shared folder listed under "Network" or "Oracle VM VirtualBox Shared Folders". You can right-click and "Map Network Drive" for easier access.
   - **Linux Guest OS:** Open a terminal window. Use the `mount` command to mount the shared folder. The specific command format might vary depending on your Linux distribution. Refer to the official documentation for details (consult your distribution's manual for specific instructions).

**Remember:**

- If you chose "Auto-mount" during setup, the shared folder will be accessible on Guest OS reboot.