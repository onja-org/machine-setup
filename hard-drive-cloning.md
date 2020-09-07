# Hard-drive cloning

## Host machine

The Windows 10 desktop PC has the [free version of Macrium Reflect 7 installed](https://www.macrium.com/reflectfree). This software is excellent at cloning hard-drives as long as they are identical.

## HDD images

At the moment the PC has 2 HDD images stored in the `C:\VMs\` folder, for the following drives:

- **500GB HGST** laptop spindle HDD. These have 'Dolly', or 'D2' through 'D8' labels. The image is called: `clean-and-configured-XXXX.mimg`
- **320GB Toshiba** laptop spindle HDD. These have 'Folly', or 'F2' through 'F8' labels. The image is called: `Folly-320GB-toshiba-clean-and-configured-XXXX.mimg`

## Cloning (and overwriting a drive) from an existing image using Restore

Because the host machine has a few VMs, you should be able to freely restore an image to the target disk, if you match the image to the type of hard-drive.

1. Start up the host machine, and sign in as 'George Cloney'
1. Unplug the USB caddy if it's connected
1. Plug the HDD into the USB caddy
1. Plug the USB caddy into the computer
1. Start Macrium Reflect
1. Select the Restore tab
1. Select the appropriate image for the harddrive you've plugged in.
1. Click the 'Restore image' link.
1. Select the 'JMicron Data' disk to restore to
1. Delete any partitions in the target disk
1. Click the 'Copy all partitions' link
1. Click through to start the process.
1. At this point you might be prompted to confirm that you're going to be deleting the content on the disk. Check the checkbox and confirm.
1. It should take 29 minutes to clone one of the HGST drives, and 19 minutes to for the Toshiba drives.
1. Close Macrium Reflect (so you can release the USB caddy)
1. Safely eject the USB caddy.
1. Label the drive if it doesn't have one

Job done! :D

## Creating a new image (Backup)

If you get a series of identical drives, and one of them has already been installed with Windows 10 Pro N, and is configured correctly, you can use it to create a main image that you can restore to other identical drives.

Make sure you've followed [the steps to create a new Windows install](./windows-install.md) before using it as the primary drive.

[At the time of writing, we haven't created images for the Western Digital 320GB drives yet, so this section could prove useful.]

1. Start up the host machine, and sign in as 'George Cloney'
1. Unplug the USB caddy if it's connected
1. Plug the HDD into the USB caddy
1. Plug the USB caddy into the computer
1. Start Macrium Reflect
1. Select the Backup tab
1. Click the 'Create image' link
1. Store the image in the `C:\VMs` folder
1. In the filename, include a nickname, harddrive description, and configuration label, e.g.: "Golly-WD-320GB-clean-install-configured"
1. Click Next
1. Don't fret about the backup plan, uncheck that.
1. Start the process. It should take 5-10 minutes. Job's done!
1. Close Macrium Reflect.
1. Safely eject the USB caddy.
1. Label the drvie as the primary 'Golly' clone.

