# Azure Vwan lab with SpokeFW and S2S

This creates a vwan with a hub and a couple of spoke vnets with VM's and a firewall vnet all connected to the vhub. It also creates an onprem vnet connected to the hub via a site to site vpn tunnel. All internet traffic is pointed to the Azure firewall in the firewall vnet. You'll be prompted for the resource group name, location where you want the resources created, your public ip and username and password to use for the VM's. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip and route tables are added sending traffic to your public ip to the internet.

The topology will look like this:

![wvanlabwithspokefwands2s](https://user-images.githubusercontent.com/128983862/233090367-6f825429-a4cb-4d08-99e8-1a66700d6a7a.png)

You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone https://github.com/quiveringbacon/AzureVwanlabwithSpokeFWandS2S.git ./terraform".

Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.
