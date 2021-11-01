# Azure Virtual machines
With Azure Virtual Machines, you can create and use VMs in the cloud. VMs provide infrastructure as a service (IaaS) in the form of a virtualized server and can be used in many ways. Just like a physical computer, you can customize all of the software running on the VM. VMs are an ideal choice when you need:

Total control over the operating system (OS).
The ability to run custom software.
To use custom hosting configurations.

# Azure Virtual Machine components
When you create a Windows Virtual Machine in Azure, you don't get just one resource. An Azure VM relies on 5 resources, created by default:

Virtual machine
Disk
Network interface
Virtual network (or choose to use an existing virtual network)
Network security group (optional but highly recommended)

If you want to make this VM publicly available over the internet, you also need a Public IP address.

# Types of VM Size 

General purpose - General-purpose VMs are designed to have a balanced CPU-to-memory ratio. Ideal for testing and development, small to medium databases, and low to medium traffic web servers.

Compute optimized - Compute optimized VMs are designed to have a high CPU-to-memory ratio. Suitable for medium traffic web servers, network appliances, batch processes, and application servers.

Memory optimized - Memory optimized VMs are designed to have a high memory-to-CPU ratio. Great for relational database servers, medium to large caches, and in-memory analytics.

Storage optimized - Storage optimized VMs are designed to have high disk throughput and IO. Ideal for VMs running databases.

GPU - GPU VMs are specialized virtual machines targeted for heavy graphics rendering and video editing. These VMs are ideal options for model training and inferencing with deep learning.

# Compute Payment Options 
Pay as you go -With the pay-as-you-go option, you pay for compute capacity by the second, with no long-term commitment or upfront payments. You're able to increase or decrease compute capacity on demand as well as start or stop at any time. 

Reserved Virtual Machine Instances - The Reserved Virtual Machine Instances (RI) option is an advance purchase of a virtual machine for one or three years in a specified region. The commitment is made up front, and in return, you get up to 72% price savings compared to pay-as-you-go pricing. RIs are flexible and can easily be exchanged or returned for an early termination fee

# The virtual machine resource - power states and billing
The state of the virtual machine impacts whether the virtual machine resource is being billed or not, in relation to the virtual machine resource and its reliance and use of underlying hardware.
 
Running - The virtual machine is powered up and working, and currently being billed for.

Stopped - The VM has been shut down from within the guest operating system or using PowerOff APIs. The VM will be showing as Stopped. This does not release the lease that the VM has on the underlying hardware, which means the hardware is unavailable for other customers. In this state, the virtual machine is still billed for.

Deallocated - The VM has released the lease on the underlying hardware and is completely powered off, so the virtual machine resource is not billed. It will appear in the Azure portal as Stopped (Deallocated).

# What if I shut the VM down using the Azure CLI or Cloud Shell?
It depends on which command you use. az vm stop will not deallocate the VM from the hardware and will display the warning "About to power off the specified VM... It will continue to be billed. To deallocate a VM, run: az vm deallocate"

# Billing of other Azure Virtual machine components
Even if the virtual machine is deallocated and not consuming "compute" time (holding a lease on hardware), there are components of this virtual machine that you are still using. Most commonly, this is storage and networking.

# Storage - disk costs
While the VM is shut down, there is still a storage cost for the disk that is holding the virtual hard drive file, as well as any other data storage disks you may have created, as you are still consuming file storage.

# Networking
The network interface, virtual network and network security group will not incur any charges. Visit Virtual Network pricing.
A static Public IP address will still be billed if the VM is shut down or even deleted, unless you delete the static public IP address.

# When to Choose virtual machines
=> Complete control over development environment
=> Migrate legacy apps to the cloud
=> Extend on-prem data center


