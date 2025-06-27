# **Method to create a bootable USB:**
## *1:Using a tool*
First, install the operating system ISO file that you want. Afterwards, you will need to install a tool that helps format and create the bootable USB.   
For example, you can use Rufus. 
Insert your USB drive and make sure there is nothing on it.    
Lauche the tool and select the USB drive.    
Pick the partition scheme (MBR or GPT), file system (NTFS or FAT32), and other options.     
Start the process and wait until it is done.    
You should now have a bootable USB. If it doesn't work, do the steps again or re-install the tool and the ISO file.    

Here's a link explaining the steps on rufus:    
https://ubuntu.com/tutorials/create-a-usb-stick-on-windows#2-requirements    


## *2:Using diskpart*
First, look up command prompt on your search bar and right click it.             
Select the run as an administrator. If it asks "do you want to continue?", click yes.            
Now you have to enter the following commands:            
DISKPART               
DISK LIST - Will display the disks available              
SELECT DISK *      - Will select the disk   ** Change the "*" to the right disk (USB drive) **              
CLEAN     
CREATE PARTITION PRIMARY      
SELECT PARTITION *    - The Nº of the partition that you wish to make primary      
ACTIVE           - Makes the selected partition active    
FORMAT FS=NTFS      - Can take a bit of time    
ASSIGN          - This will assign a drive letter    
EXIT           - To leave "DiskPart"

Now you have a bootable USB on windows. 

## Extra Information

*What is the minimum size for my bootable USB?*     
*-The recommended minimum size for the USB drive is 8GB.*

*Can you do multiple boots from on key?*     
-Yes you can. It isn't recommended to put many of them on a singular one because it can cause issues.

*Here's some other software you can use to make a bootable USB:*      
UNetbootin, Balena Etcher, Ventoy and Yumi
