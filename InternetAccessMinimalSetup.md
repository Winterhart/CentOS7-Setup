
## Internet Access
Since no wifi drivers were installed, the first task is to get internet access. On my side, I've use a bridge with a Windows 10 laptop.
I have used this tutorial: https://www.windowscentral.com/how-set-and-manage-network-bridge-connection-windows-10

### Activation of the Bridge
Once in the CentOS terminal, use the command: `nmtui` 
This command will bring a menu:

![menu](https://www.cyberciti.biz/media/new/faq/2015/05/nmtui-tui-1.jpg)

Choose Activate a connection and choose your ethernet adapter.

You can verify the current internet status with: `nmcli d`
You should be able to see your Ethernet adapter with the status 'connected':


![Internet Status](https://ptpimg.me/8vg0eu.png)
