# OpenShift Virtualization Test - Web Console Edition

**Course:** OpenShift Container Platform - Virtualization  
**Duration:** 90 minutes (Can be longer)
**Total Points:** 100 points  
**Instructions:** Complete all tasks using the OpenShift Web Console UI. Take screenshots of key steps and provide explanations where requested.

---

## Question 1: Basic VM Creation via Web Console (20 points)

You need to create a Virtual Machine using the OpenShift Web Console.

**Requirements:**
- VM name: `centos-vm-01`
- Namespace: `student-vms-userx` (Please change userx to your user number)
- Operating System: CentOS 9 Stream
- CPU: 2 cores
- Memory: 4 GiB
- Storage: 30 GiB
- Boot source: Container disk from Red Hat registry

**Tasks:**
1. Navigate to the correct section in the OpenShift Web Console to create VMs
2. Describe the step-by-step process to create this VM using the web interface
3. What options are available for boot sources in the UI? List at least 4 different types
4. After creating the VM, how do you start it using the web console?
5. Take a screenshot of the VM overview page once it's running

**Questions:**
- What is the difference between "Create from template" and "Create from YAML" options?
- Where can you monitor the VM creation progress in the UI?

---

## Question 2: VM Console Access and Basic Configuration (15 points)

Your VM from Question 1 is now running. You need to access it and perform basic configuration.

**Tasks:**
1. Access the VM console through the web interface - describe how to do this
2. What are the different console access methods available in the UI?
3. Using the console, log into the VM and run the following commands:
   - Check the hostname
   - Check available memory
   - Check CPU information
   - List network interfaces
4. Take screenshots of the console showing these command outputs

**Troubleshooting Scenario:**
If the VM console shows a black screen or is unresponsive, what steps would you take using the web console to troubleshoot this issue?

---

## Question 3: Network Configuration via UI (20 points)

Configure networking for your VM using the OpenShift Web Console.

**Requirements:**
- Create a NetworkAttachmentDefinition called `vm-bridge-network`
- Configure it as a Linux bridge
- Bridge name: `br1`
- Attach this network to your existing VM as a secondary interface

**Tasks:**
1. Navigate to the networking section and create the NetworkAttachmentDefinition
2. Describe the step-by-step process to create this network configuration
3. Edit your existing VM to add the secondary network interface
4. Explain how to verify the network configuration is applied correctly
5. What information is displayed in the "Network Interfaces" section of the VM details?

**Questions:**
- What's the difference between "Pod networking" and "NMstate" networking options in the UI?
- How can you test network connectivity from the VM using the web console tools?

---

## Question 4: Storage Management and Cloud-Init (25 points)

Configure additional storage and use cloud-init for VM customization.

**Part A: Additional Storage (12 points)**
- Add a second disk (10 GiB) to your VM
- Use a PersistentVolumeClaim as the source
- Storage class: Use the default available storage class

**Part B: Cloud-Init Configuration (13 points)**
Create a new VM with cloud-init configuration:
- VM name: `centos-vm-02`
- Set hostname to `centos-vm-02.lab.local`
- Create user `student` with password `redhat123`
- Install packages: `htop`, `git`
- Set timezone to `America/New_York`

**Tasks:**
1. Show how to add additional storage to an existing VM through the UI
2. Create the cloud-init configuration using the web console's cloud-init form
3. Describe where to find the cloud-init options in the VM creation wizard
4. What are the different cloud-init input methods available in the UI?
5. After VM creation, how do you verify cloud-init ran successfully using the console?

**Screenshot Requirements:**
- Storage configuration page
- Cloud-init configuration form
- VM with additional disk attached

---

## Question 5: VM Operations and Monitoring (20 points)

Perform various VM operations using the OpenShift Web Console.

**Scenario:** You have multiple VMs running and need to perform maintenance operations.

**Tasks:**
1. **VM Lifecycle Management:**
   - Stop your VM using the web console
   - Restart the VM
   - Describe the different VM states visible in the UI

2. **Resource Monitoring:**
   - Access the VM metrics/monitoring page
   - What performance metrics are displayed for VMs?
   - How do you view CPU and memory usage over time?

3. **VM Migration:**
   - Initiate a live migration of your VM
   - Where do you find migration options in the UI?
   - How do you monitor migration progress?

4. **Snapshot Management:**
   - Create a snapshot of your VM
   - List the steps to restore from a snapshot
   - Where are snapshots managed in the web console?

5. **Event Monitoring:**
   - Navigate to the Events section for your VM
   - What types of events are typically shown?
   - How do you filter events by severity or time?

**Questions:**
- How do you resize VM resources (CPU/Memory) using the web console?
- What's the difference between "Stop" and "Force Stop" options?
- How can you clone an existing VM using the UI?

---

## Bonus Question: VM Templates and Customization (10 points)

**Scenario:** You need to create a standardized VM template for your team.

**Tasks:**
1. Create a VM template from your existing VM
2. Describe the process of creating custom VM templates
3. How do you make templates available to other users/projects?
4. What parameters can be customized when deploying from a template?
5. Show how to deploy a new VM from your custom template

**Advanced Questions:**
- How do you manage template versions in the UI?
- What's the difference between common templates and custom templates?
- How can you share templates across different namespaces?

---

## Submission Requirements:

**Documentation:**
- Provide step-by-step instructions for each task
- Include screenshots of key configuration pages
- Explain any errors encountered and how you resolved them

**Screenshots Must Include:**
- VM creation wizard pages
- VM overview/details pages
- Console access screens
- Network and storage configuration pages
- Monitoring/metrics pages
- Any error messages or troubleshooting steps

**Written Explanations:**
- Describe UI navigation paths clearly
- Explain the purpose of each configuration option
- Provide reasoning for configuration choices
- Include troubleshooting approaches

Please create your tab on Google Sheet file and provide all answer and screenshot there.

https://docs.google.com/spreadsheets/d/1r9Az9WhhyCiQP_ZgECpaXeBHBN3y2YCZVO8jMroq6qA/edit?usp=sharing

---

**Evaluation Criteria:**
- Correct completion of tasks (60%)
- Quality of screenshots and documentation (25%)
- Understanding demonstrated through explanations (15%)

**Good luck! If you are able to complete this, you have a good chance to pass the certification already, contact me for more info. **
