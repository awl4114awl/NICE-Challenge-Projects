<p align="center">
<img src="https://i.imgur.com/ARGlAoP.png" height="100%" width="100%" alt="install kali"/>
</p>
<h1>Secure Domain Accounts & Passwords? Probably Worth [NG]</h1>

    A couple of months ago our policy team came up with some new security policies to improve operational security at the company, you have been tasked with verifying that these policy guidelines are being enforced techincally on our employee's Windows-based workstations that authenticate through the Domain Controller. 
    
    If any of these new policies are not being enforced you will also be in charge of creating technical policies in form of a GPO on the Domain Controller to enforce these security policies.

<h2>Solution</h2>

    I first opened the Workstation-Desk and logged on. I went to the Network fileshare tab, clicked on dasShare then opened the "Dynamic Arbitrary Solutions Policy" pdf to get the policies needed.

    Then I opened up the Domain-Controller VM and logged on. Once on the Domain-Controller, I opened up Server Manager and went to Group Policy Management. I expanded Forest > daswebs.com > Group Policy Object. Under this folder I created a new GPO called "DasPol". Then I right clicked the newly created GPO and clicked "edit".

    Next I clicked on "Computer Configuration" > "Policies" > "Windows Settings" > "Security Settings" > "Account Policies".

    Then I changed the Password Policy and Account Lockout Policy according to the pdf I pulled up on Workstation-Desk. 

    To link the new GPO to the domain-level I right clicked on the "daswebs.com" domain and selected "Link an Existing GPO...". From there I selected the GPO "DasPol" and hit "Detect Now".

<h2>Report</h2>
<br />
<br />
<img src="https://i.imgur.com/O5RRGzC.png" height="80%" width="80%" alt="NICE Challenge"/>
<br />
<br />
<img src="https://i.imgur.com/z2vj0D2.png" height="80%" width="80%" alt="NICE Challenge"/>
<br />
<br />
<img src="https://i.imgur.com/PYkn3iW.png" height="80%" width="80%" alt="NICE Challenge"/>
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
