## How to Reset the Root Password on Ubuntu 22.04 LTS

If you've forgotten your root password on Ubuntu 22.04 LTS, you can reset it by following these steps:

## Step 1: Boot into Recovery Mode
1. Restart your computer.
2. Hold down the `Shift` key while the system is booting up to bring up the GRUB menu.
3. In the GRUB menu, select the `Advanced options for Ubuntu` option using the arrow keys, then press `Enter`.
4. Select the recovery mode option, which should look something like `Ubuntu, with Linux <version>-generic (recovery mode)`, then press `Enter`.

## Step 2: Access the Root Shell
1. After a few moments, you’ll see the Recovery Menu. Select the `root` option to drop into a root shell prompt.
2. You'll be asked to press `Enter` to continue. Do so.

## Step 3: Remount the Filesystem with Write Permissions
1. By default, the filesystem is mounted as read-only in recovery mode. Remount it with write permissions using the following command:
   ```bash
   mount -o remount,rw /
   ```

## Step 4: Reset the Root Password
1. Now, reset the password with the following command:
	```bash
	passwd root
	```
2. You'll be prompted to enter a new password. Type the new password and press `Enter`.
3. Retype the new password to confirm it and press `Enter`.

## Step 5: Reboot the System
1. Once the password is reset, you can reboot the system with the following command.
	```bash
	reboot
    ```

Your root password should now be reset, and you can log in with the new password.