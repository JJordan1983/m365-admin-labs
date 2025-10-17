# SharePoint Lab 1.1 — Modern Site Provisioning and Role Permissions

## Objective
Provision a modern Communication site in SharePoint Online, configure group-based permissions, and prove least privilege with a test user.

---

## Steps

### A. Create a Communication Site
1. Go to **Microsoft 365 Admin Center → Admin Centers → SharePoint → Active Sites**.
2. Select **Create** → **Communication Site**.
3. Enter site name, owners, and URL. Click **Finish**.
4. Alternatively, use PnP PowerShell:

```powershell
Connect-PnPOnline -Url https://contoso-admin.sharepoint.com -Interactive
New-PnPSite -Type CommunicationSite -Title "Corp Comms" -Url https://contoso.sharepoint.com/sites/corp-comms
