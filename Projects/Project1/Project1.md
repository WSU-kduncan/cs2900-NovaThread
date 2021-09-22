VirtualBox was used to create the VM

PART 1
-VM Creation
1. To start I had to find an iso of an operating system, lucky for me I had an Ubuntu iso laying around on a server of mine.
2. To start click new icon in the VirtualBox gui and locate your iso file. You can also name your os as well as select what version you are running.
3. Click next and alocate some ram for your vm. make sure to leave enough ram for your host machine to still operate adequately. I added 4000MB.
4. In the next screen create a virtual hard disk. this will allocate an amount of storage for your vm to take up.
5. The nect windo leave the selection on VDI. this is the default for VirtualBox.
6. The next window leave the selection on Dynamically Allocated This will ensure your VM can have enough storage and won't break itself by running out of storage space.
7. Finally create the VM.

-Settings for VM
1. Now select the vm on the left of the window and select settings.
2. Go to system. Here you can change the alocated ram as well as boot order for your hardware.
3. In the Display settings you can enable 3D acceleration, this will allow usage of your GPU if you have one in your system.
4. Now it is time to start the VM and see how it works.
![image 1(img/img1)

-Making The VM Fullscreen Compatible
1. Select the Devices on the top of the VM window and select "Insert Guest Additions CD image".
![image 1(img/img2)

2. After the installation restart the VM. You should now be able to use the VM in full screen.

PART 2
-Accesing the VM data on your Host Machine and making snapshots and templates
1. In your vm window on the top left select machine then select take snapshot. This will take a snapshot and store it in your host systems file directory. Shut down the VM
2. In the VBox Manager window select file in the top left and select Export Appliance. You shouldn't have to change anything in the Gui just click next until you can click Export.
3. Open the directory of where you store your vms. Here you can see the files that are your OS on your VM.

PART 3
-Enabling Bridged Adapter
1. With the VM closed open settings and go to networking, in the drop down menu select "bridged adapter"
2. Select the name of your adapter on your host machine.
3. Start the VM and open command prompt. Ping your host machine and you will get a reply.
![image 1(img/img3)
