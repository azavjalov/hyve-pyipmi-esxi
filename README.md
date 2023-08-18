# ipmitool alternative for ESXi 8.0, based on Hyve PyIPMI

You may know that ipmitool is not available for ESXi after 7.0 because of the new policies for the packages introduced in 8.0 (please see more details in this blogpost https://vswitchzero.com/ipmitool-vib).
PyIPMI is a simple workaround for this problem. This tool may not provide all capabilities existing in ipmitool - you may want to check the functions implemented and supported today and see if this works for you.

This tool is only for home/experimental use. Not for production use!

In order to install it in ESXi you would need to get zipped copy of master branch and place it somewhere in your installed ESXi.
Before running the tool you will need to disable the enforcment from using non-installed apps following this article - https://docs.vmware.com/en/VMware-vSphere/8.0/vsphere-security/GUID-DF6A7974-62F9-47DB-A990-963F3B3AEA77.html. This opens the window for ransomware attacks on your host. It is advised to enable the protection back once you are done using the tool.

Now you can you can unpack the package, make pyipmi executeable (chmod +x pyipmi) and run ./pyipmi app. You should the syntax very similar to ipmitool.

![image](https://github.com/azavjalov/hyve-pyipmi-esxi/assets/25473191/f58e42ae-8113-4d75-8d71-ca8a965ee0f8)

To see all the options for the app run "./pyipmi -h"

![image](https://github.com/azavjalov/hyve-pyipmi-esxi/assets/25473191/5e04c6f4-8456-43d8-8fc2-33168d20f83d)

Example of running one of the standard commands to see the chassis power status

![image](https://github.com/azavjalov/hyve-pyipmi-esxi/assets/25473191/d987ddc7-f308-4514-a10c-057a57ab9a90)


### If you are interested in running this tool on Linux or other non-ESXi environment please visit page for the original Hyve PyIPMI tool here -- https://github.com/hyvedesignsolutions/hyve-pyipmi
