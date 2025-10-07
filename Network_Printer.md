# Network Printer Configuration and Installation:

### Make sure the printer is connected to the network first and turn it on. Go through the menu, find the configuration page and select to print it out. From there you can find the MAC address. Example MAC: 9cb6544d30ec.

### In the network settings, make sure it's configured to automatically get an IP address. When the printer is connected to the network, type in the IP address on the web browser and it should display a printer embedded web server. In the network tab, choose to configure IP automatically. 


### Things to do on the Server:
- Go to the DHCP server on windows. Expand the DC. Select IPv4 and go to Scope. In the Address Pool, you can find the Start IP address and the End IP address.

<img width="588" height="394" alt="Image" src="https://github.com/user-attachments/assets/c35c5be9-3706-4b4b-a041-3cc2bbe71248" />

- Right-click on the Reservation and click on new reservation. In the Reservation name, come up with the printer name that will be used for the network to identify. Example name: printer1athr. In the IP address, choose one that's within scope. Example IP: 10.1.10.50. In the MAC address, put in the MAC address of the printer.

<img width="344" height="304" alt="Image" src="https://github.com/user-attachments/assets/cc887812-42e5-46a1-a6b5-87ee344fed06" />
<img width="348" height="340" alt="Image" src="https://github.com/user-attachments/assets/2ac29651-902a-4768-bef2-13611eaa548a" />

- Now go to the DNS Manager. Under the Domain Controller, go to Forward Lookup Zones. Right-click on the domain and select New Host (A or AAAA).

<img width="387" height="570" alt="Image" src="https://github.com/user-attachments/assets/b10b52fb-cfdc-4bef-9564-d9d62eea7daf" />

- In the New Host tab, choose the name that was used before (printer1athr). Type in the IP address that was chosen previously (10.1.10.50). Now click on Add Host. This is basically saying that the host name printer1athr is using the IP address 10.1.10.50 so that we can use the host name and not have to memorize the IP address of the printer. 


<img width="350" height="361" alt="Image" src="https://github.com/user-attachments/assets/2a6820a9-685e-46a1-8b82-aab88b2c8c12" />

- Now go to Print Management. Right-click on Printers and select 'Add Printer'. 

<img width="303" height="392" alt="Image" src="https://github.com/user-attachments/assets/51340a82-ae92-479f-846f-b1d48985b8f7" />

- Select 'Add an IPP, TCP/IP, or Web Services Printer by IP address or hostname'. Click on Next. Select TCP/IP Device for the 'Type of Device' and in the Host name or IP address, put in the hostname.

<img width="578" height="442" alt="Image" src="https://github.com/user-attachments/assets/5fd04253-14f7-4bd5-8d40-8536e1074440" />
<img width="579" height="443" alt="Image" src="https://github.com/user-attachments/assets/08070ec4-f207-4da2-acc6-b2dba28b878d" />

- When the driver is added, you can right click on it and go to properties. Print a test page if needed. In the ports tab, you can see that the driver is pointing to the port of the printer. 

<img width="467" height="507" alt="Image" src="https://github.com/user-attachments/assets/df51fa06-6505-4749-aea3-acb83a8e5f3d" />

- You can now go to a client computer and add the network shared printer. Go to Printers and Scanners. Click on Add device. The printer should show up, but if it doesn't, try to add it manually via an IP address or hostname.  

<img width="615" height="452" alt="Image" src="https://github.com/user-attachments/assets/836c4d6b-0838-4ff4-997b-5252ae568bf4" />
<img width="620" height="445" alt="Image" src="https://github.com/user-attachments/assets/e824574e-cdf0-4cfc-bbe0-fed92fecc2ed" />
<img width="616" height="452" alt="Image" src="https://github.com/user-attachments/assets/a8b3faa3-09a8-41ba-8cac-ccbb28cb3004" />
<img width="465" height="402" alt="Image" src="https://github.com/user-attachments/assets/71ddc0c4-ca6b-41db-991c-71c65892597f" />


