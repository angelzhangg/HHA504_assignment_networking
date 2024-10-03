# Objective
The objective of this assignment is to explore the networking features in Azure and Google Cloud Platform (GCP), focusing on Virtual Private Cloud (VPC), Virtual Private Network (VPN), IP addresses, and domain management. You will gain practical experience in assigning dedicated IPs and mapping them to domains.

## 1. Create a Virtual Private Cloud (VPC)
**Azure:**
  - Navigate to the Azure portal and create a new Virtual Network (VNet).

Choose a simple IP address range and subnet configuration.
![pic1](<Screenshot 2024-09-22 at 5.01.02 PM.png>)
![pic2](<Screenshot 2024-09-22 at 5.01.42 PM.png>)
![pic3](<Screenshot 2024-09-22 at 5.02.20 PM.png>)
![pic4](<Screenshot 2024-09-22 at 5.03.02 PM.png>)
**GCP:**
  - Access the Google Cloud Console and create a new VPC network.

Configure the IP address range and subnets similarly to your Azure setup.
![pic1](<Screenshot 2024-09-29 at 8.42.33 PM.png>)
![pic2](<Screenshot 2024-09-29 at 8.42.41 PM.png>)
![pic3](<Screenshot 2024-09-29 at 8.42.49 PM.png>)
![pic4](<Screenshot 2024-09-29 at 8.44.39 PM.png>)

## 2. Assign a Dedicated IP
**Azure:**
  - Reserve a static public IP address for a resource (e.g., a virtual machine) within your VNet.

![pic1](<Screenshot 2024-09-22 at 5.25.23 PM.png>)
![pic2](<Screenshot 2024-09-22 at 5.44.09 PM.png>)
![pic3](<Screenshot 2024-09-22 at 5.45.03 PM.png>)
![pic4](<Screenshot 2024-09-22 at 5.46.14 PM.png>)
**GCP:**
  - Reserve a static external IP address for a Compute Engine instance within your VPC.

Go to **VPC Network > External IP addresses** <br/>
Click **Reserve static address** 
![pic1](<Screenshot 2024-09-29 at 9.09.52 PM-1.png>)
![pic2](Screenshots.png)
![pic3](<Screenshot 2024-09-29 at 9.05.27 PM-1.png>)

Next, we will assign the static IP to a VM instance <br/>
Go to **VM instances**



## 3. Map IP to a Domain Acquired via GitHub Student Pack
- Use your GitHub Student Developer Pack to acquire a domain through Namecheap (or another supported registrar).
- Set up an **A record** for your main domain (e.g., `yourdomain.com`) and a **subdomain** (e.g., `app.yourdomain.com`).

## 4. Deploy Flask Application
- Deploy the provided Flask application located at [HHA 504 Flask Networking](https://github.com/hantswilliams/hha-504-flask-networking) to your virtual machine on Azure or GCP.
- Ensure that the Flask application is running on a specific port (e.g., port 5007).

## 5. Configure Firewall Settings
- Make sure that the port on which your Flask application is running is accessible to the general public.
  - **Azure:** Configure Network Security Group (NSG) rules to allow inbound traffic on the specified port.
  - **GCP:** Configure Firewall rules to allow traffic on the specified port.

## 6. Access Your Application via Domain
- Visit your deployed Flask application using the custom domain or subdomain you mapped, including the port number in the URL (e.g., `http://app.yourdomain.com:5000`).