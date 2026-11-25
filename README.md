# MGI HR Portal

A one-page HR portal for staff. It shows quick links into PeopleHub (leave, overtime, payslips, clock-in, claims, helpdesk),
HR news, upcoming holidays, policies and HR contact details. The content comes live from PeopleHub, so you never edit this file again
after setup.

## 1. Connect it to PeopleHub (once)
1. In the PeopleHub spreadsheet: **PeopleHub > Staff & access > Show app links**, and copy the **staff app link** (it ends in `/exec`).
2. Open `index.html`, find this line near the top and paste the link between the quotes:

       const PEOPLEHUB_URL = 'https://script.google.com/macros/s/XXXX/exec';

3. Make sure the PeopleHub web app is deployed with **Who has access: Anyone** (Deploy > Manage deployments).

## 2. Put it online with GitHub Pages (free)
1. Create a free account at https://github.com (if you do not have one).
2. Click **New repository**, name it e.g. `hr-portal`, choose **Public**, then **Create repository**.
3. Click **uploading an existing file**, drag `index.html` into the page, then **Commit changes**.
4. Go to **Settings > Pages**. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**.
5. After about a minute your portal is live at: `https://YOUR-USERNAME.github.io/hr-portal/`

## 3. Use your own domain (optional)
1. Buy a domain, or use a sub-address of your company domain, e.g. `hr.yourcompany.com`.
2. In GitHub: **Settings > Pages > Custom domain**, type `hr.yourcompany.com`, then **Save**, and tick **Enforce HTTPS** when it appears.
3. At your domain seller, add a DNS record: type **CNAME**, name **hr**, value **YOUR-USERNAME.github.io**.
4. Wait for DNS to update (from a few minutes up to a day).

## What you change, and where (no code)
| What | Where |
| --- | --- |
| Buttons and documents | PeopleHub > SYSTEM > Lists & tables > **Portal links**, or the **Portal_Links** tab |
| News on the portal | Post an announcement in PeopleHub and tick **Also show on the public HR portal website** (or set **Show on Portal = YES** in the Announcements tab) |
| Holidays | The **Holidays** tab (the next ones are shown automatically) |
| Welcome text, HR phone | Settings: **HR Portal Welcome Text**, **HR Contact Phone** |
| Working hours, HR email, logo | Settings / PeopleHub logo (already used by PeopleHub) |

The portal refreshes its information about every 5 minutes.

## Privacy
This page is public. It only shows information meant for all staff. Personal data (leave balances, payslips, time records)
always stays inside PeopleHub behind the login. Keep confidential announcements **not** shown on the portal.
