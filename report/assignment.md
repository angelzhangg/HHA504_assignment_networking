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
![pic5](<Screenshot 2024-10-02 at 6.36.25 PM.png>)

## 2. Assign a Dedicated IP
**Azure:**
  - Reserve a static public IP address for a resource (e.g., a virtual machine) within your VNet.

![pic1](<Screenshot 2024-09-22 at 5.25.23 PM.png>)
![pic2](<Screenshot 2024-09-22 at 5.44.09 PM.png>)
![pic3](<Screenshot 2024-09-22 at 5.45.03 PM.png>)
![pic4](<Screenshot 2024-09-22 at 5.46.14 PM.png>)

Next, we will assign the static IP to a VM instance <br/>
Go to **VM instances**

![IP](https://github.com/user-attachments/assets/39e86072-d786-4279-8e90-5fe5384d78fd)
![IP1](https://github.com/user-attachments/assets/94c93914-32ed-4b78-a342-b021b12d3e11)
![IP2](https://github.com/user-attachments/assets/82131f67-6783-443d-832d-8086a7351e21)
![IP3](https://github.com/user-attachments/assets/d524570c-8207-4bbb-86f9-48904fead4a3)


> Assign the virtual network to the one you created <br/>
Assign Public IP to the one you created

![vm]("https://github.com/user-attachments/assets/2de2d83f-59ae-47e0-b67a-fe02797b3f9c")
![vm1](https://github.com/user-attachments/assets/ef83536a-eaa7-4acb-8179-1f0e72e0d7c6)

**GCP:**
  - Reserve a static external IP address for a Compute Engine instance within your VPC.

Go to **VPC Network > External IP addresses** <br/>
Click **Reserve static address** 
![pic1](<Screenshot 2024-09-29 at 9.09.52 PM-1.png>)
![pic2](<Screenshot 2024-10-02 at 8.51.06 PM.png>)
![pic3](<Screenshot 2024-09-29 at 9.05.27 PM-1.png>)

Next, we will assign the static IP to a VM instance <br/>
Go to **VM instances**
![gcp IP](https://github.com/user-attachments/assets/380d93f7-3352-43df-a993-ad6de0492798)
![gcp IP 1](https://github.com/user-attachments/assets/29150c19-5931-4a3d-ba2e-3952b2271b48)
![gcp IP 2](https://github.com/user-attachments/assets/a57f5879-f814-4eb1-bfd7-ef71324ffc1f)


Map IP to a domain name

<img width="946" alt="Screenshot 2024-10-02 at 10 52 16 PM" src="https://github.com/user-attachments/assets/bd049fb2-726d-4346-bb83-07f823be9eed">
<img width="756" alt="Screenshot 2024-10-02 at 10 53 24 PM" src="https://github.com/user-attachments/assets/8dd04c9c-b0a2-4c15-b78f-95d0e37ce30f">


## 3. Map IP to a Domain Acquired via GitHub Student Pack
- Use your GitHub Student Developer Pack to acquire a domain through Namecheap (or another supported registrar).
- Set up an **A record** for your main domain (e.g., `yourdomain.com`) and a **subdomain** (e.g., `app.yourdomain.com`).

![namecheap](https://github.com/user-attachments/assets/9b27e77d-381e-464f-aadd-aa2d39cc6702)

## 4. Deploy Flask Application
- Deploy the provided Flask application located at [HHA 504 Flask Networking](https://github.com/hantswilliams/hha-504-flask-networking) to your virtual machine on Azure or GCP.
- Ensure that the Flask application is running on a specific port (e.g., port 5007)

![flask](https://github.com/user-attachments/assets/e32220ea-2171-4011-ae35-6ede95158a6e)


## 5. Configure Firewall Settings
- Make sure that the port on which your Flask application is running is accessible to the general public.
  - **Azure:** Configure Network Security Group (NSG) rules to allow inbound traffic on the specified port.
  - **GCP:** Configure Firewall rules to allow traffic on the specified port.

## 6. Access Your Application via Domain
- Visit your deployed Flask application using the custom domain or subdomain you mapped, including the port number in the URL (e.g., `http://app.yourdomain.com:5000`).

![domain](https://github.com/user-attachments/assets/63b72714-e75a-4ba8-a25a-25c7fdb806e5)
