<p align="left">
<img src="https://i.imgur.com/ARGlAoP.png" height="20%" width="20%" alt="install kali"/>
</p>
<h1>Secure Domain Accounts & Passwords? Probably Worth [NG]</h1>

##### A couple of months ago our policy team came up with some new security policies to improve operational security at the company, you have been tasked with verifying that these policy guidelines are being enforced techincally on our employee's Windows-based workstations that authenticate through the Domain Controller. 
    
##### If any of these new policies are not being enforced you will also be in charge of creating technical policies in form of a GPO on the Domain Controller to enforce these security policies.

## Tools Used

    Workstation-Desk
    PDF Viewer
    Domain-Controller VM
    Server Manager
    Group Policy Management Console (GPMC)
    Windows Security Settings

## Network Map
<img src="https://i.imgur.com/Ms9L7zn.jpeg" height="80%" width="80%" alt="NICE Challenge"/>
    
## Solution

##### I started by logging into the Workstation-Desk and navigating to the Network fileshare tab. I clicked on dasShare and opened the "Dynamic Arbitrary Solutions Policy" PDF to review the necessary policies.

##### Next, I logged into the Domain-Controller VM. In Server Manager, I accessed Group Policy Management, expanded Forest > daswebs.com > Group Policy Objects, and created a new GPO named "DasPol". I right-clicked on the new GPO and selected "edit".

##### In the editor, I navigated to "Computer Configuration" > "Policies" > "Windows Settings" > "Security Settings" > "Account Policies". 

##### I updated the Password Policy and Account Lockout Policy according to the PDF from Workstation-Desk.

##### Finally, I linked the new GPO to the domain by right-clicking the "daswebs.com" domain, selecting "Link an Existing GPO...", choosing "DasPol", and clicking "Detect Now".

<p align="center"><img src="https://i.imgur.com/O5RRGzC.png" height="80%" width="80%" alt="NICE Challenge"/>

<p align="center"><img src="https://i.imgur.com/z2vj0D2.png" height="80%" width="80%" alt="NICE Challenge"/>

<p align="center"><img src="https://i.imgur.com/PYkn3iW.png" height="80%" width="80%" alt="NICE Challenge"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
