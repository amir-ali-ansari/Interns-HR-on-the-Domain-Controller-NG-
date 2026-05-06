# Interns-HR-on-the-Domain-Controller-NG-
Manage accounts, network right and access to system

1.login to Domain-Controller console using Playerone credentials
verification: login successfully

2. create groups
location: start > Server Manager >Tools (top right tabs) > Active Directory Users and Computers
in the new opened windos right click on dasweb.com (on left side of the window)> New > Group>  for Group name in the new window put HRSec and leave the other options untouched.
repeat these steps for AccountingSec (for Accounting) and Miscellaneous groups
verification: click on daswebs.com and you can see three new groups 

3. Add Brimlock in the Accounting Security Group and Sergio in the HR Security Group
location: Server Manager > ADUC > dasweb.com > right click on HRSec group > Properties > click on Members (top tabs) > Add > type Sergio in Enter the object names to select field > Ok > Apply > Ok
verification: You can see Sergio is added when click on Members tab
location: Server Manager > ADUC > dasweb.com > right click on AccountingSec group > Properties > click on Members (top tabs) > Add > type Brimlockin Enter the object names to select field > Ok > Apply > Ok
verification: You can see Brimlock Stones is added when click on Members tab

4. Add gthatcher to the Domain Admins group
location: dasweb.com > Users > find Domain Admis group on the right panel of the window (groups icon is a two person image and users are one person image) > right click on Domain Admins >properties > Members > Add 
> type Gary > Check Names > Ok > apply > Ok
verification: you can see Gary is in the Members

5. Add all non-admins to the Miscellaneous group
location: dasweb.com > Users > select all except Playerone, Sergio, Gary, Gilly, Administrator and Brimlock> right click > Add to a group > type Miscellaneous in the Enter the object names to select field> check name> ok > ok
verification: you can see users are added to the group (click on dasweb.com > Miscellaneous > Members)

6. Add HR Share access to HRSec, AccountingSec and Miscelaneous security groups
location: find HR shared folder in this directory: File Explorer > Network (on the left side of the window)> click on "Network discovery is turned off" message> click on Turn on network discovery and file sharing
> double click on FILESHARE > rihgt click on hr folder > properties > security tab (on top level of the window) > edit > Add > type HRsec in Enter the object name to select > ok (Add AccountingSec and Miscelaneous goups by repeating same steps.)
verificatin: you can see the added groups in the Group or user names field

7. Assign permissions to the users through the secuity groups
location: right click on hr folder > properties > security>.select Domain Admins in the list of Groups and user names > select Allow for all permissions (just double click on the first permission) > Apply > Ok
then select HRSec in the list of Groups and user names > Allow only List foldr contents, Read, Wrire > Apply > Ok
for Miscellaneous and AccountingSec Deny all permissions
follow the same steps for accounting folder. just remember to give Write, Read and List folder contents to AccountingSec group and all permissions to Domain Admins group and Deny permissions to other two groups. 
verification: you can see the permissions of each group in the permissions list

8. Disable Rob account
location: Server Manager > Tools > ADCU > dasweb.com > Users> find Rob and right click on it > Disable account > ok
verification: right click on Rob and you see enable account instead of disable account

9. Brimlock Stones can only log onto Workstation-Desk
location: Server Manager > Tools > ADCU > dasweb.com > Users> find Brimlock Stones and right click on it > properties > click on Acount tab> click on Log On To > select The following computers > type Workstation-Desk > ok > ok
verification: user can not login to other computers

10. Sergio Chanel can only log onto Workstation-Desk
follow the same steps of Brimlock user in step 9.
