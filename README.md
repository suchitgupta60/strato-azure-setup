# strato-azure-setup

I had the same issue when setting up with Azure instance. I had to create and delete instances several times to get the right configurations to work. But once you get it right it works like a charm.

Here is what you need to check when you are creating the instance on azure:
1. There are couple different flavor of instances (individual node, single-node, multi-node) that you can pick from. In my case I picked individual node.
2. Make sure user name of your instance is "strato" and nothing else. Like this:
![screen shot 2017-08-18 at 4 09 17 am](https://user-images.githubusercontent.com/12634462/29450091-4da52da2-83cb-11e7-97bf-fb0132a7659c.png)

Follow this link if you need to setup new key: https://docs.microsoft.com/en-us/azure/virtual-machines/linux/mac-create-ssh-keys

3. For virtual machine size try and search for F2S Standard with 2 Cores and 4 GB RAM.
4. Assign some static DNS name to your public IP address here like this:
![screen shot 2017-08-18 at 4 17 00 am](https://user-images.githubusercontent.com/12634462/29450294-2881794e-83cc-11e7-8838-aa08e8afb20d.png)

5. In terminal navigate to the folder where your ssh key file is. From that folder run this command ssh strato@example.eastus.cloudapp.azure.com

![screen shot 2017-08-18 at 4 25 14 am](https://user-images.githubusercontent.com/12634462/29450605-493753ec-83cd-11e7-8ae3-9425f46b0494.png)

6. Make sure you add DNS name when starting the script otherwise it will keep showing the Health Network yellow.
![screen shot 2017-08-18 at 4 31 06 am](https://user-images.githubusercontent.com/12634462/29450978-dfe9f014-83ce-11e7-9d58-da7c8d046d4f.png)

Now you should be able to access your strato dashboard at http://example.eastus.cloudapp.azure.com/
with ID: admin and Password: admin
