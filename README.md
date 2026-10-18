# citycubedxb.ae – website setup (about 15 minutes)

## 1. Fill in your details
Open `index.html`, find the block marked `EDIT THESE` near the bottom and fill in: WHATSAPP (digits only, e.g. 971501234567), PHONE, EMAIL, ADDRESS, working hours and, if you like, MAP_QUERY.
Anything left blank is hidden from the page (no empty boxes). The WhatsApp button and floating chat bubble appear once WHATSAPP is filled in.

## 2. Publish on GitHub Pages (free)
1. GitHub → New repository → name `citycubedxb-site` (Public) → Create.
2. Add file → Upload files → upload everything in this folder (`index.html`, `logo-mark.png`, `logo-full.png`, `CNAME`, `robots.txt`, `sitemap.xml`, and the `staff` folder) → Commit.
   Tip: to upload the `staff` folder, drag the whole folder in.
3. Settings → Pages → Source: *Deploy from a branch* → Branch `main` / root → Save.
4. Same page → Custom domain → `citycubedxb.ae` → Save → tick **Enforce HTTPS** when it becomes available (can take up to an hour).

## 3. Point the domain (at your .ae registrar's DNS panel)
| Type  | Host | Value |
|-------|------|-------|
| A     | @    | 185.199.108.153 |
| A     | @    | 185.199.109.153 |
| A     | @    | 185.199.110.153 |
| A     | @    | 185.199.111.153 |
| CNAME | www  | citycubedxb-stack.github.io |
Delete any old A/CNAME records for @ and www first. DNS changes can take from a few minutes to a few hours.

## 4. Staff login
- The small **Staff login** link in the page footer opens the inventory system: https://citycubedxb-stack.github.io/citycube-firebase/
- `citycubedxb.ae/staff` also redirects there – easy for staff to remember.
- The system itself still requires an email and password, so the link is safe to leave public.

## Later (optional)
Give the system its own address such as `staff.citycubedxb.ae`: in the inventory repo set Pages → Custom domain to it, add a CNAME record `staff` → `citycubedxb-stack.github.io`, and add `staff.citycubedxb.ae` under Firebase → Authentication → Settings → Authorised domains. Then change STAFF_URL in `index.html` and the two URLs in `staff/index.html`.

## Photos (recommended – real photos of your warehouse build trust)
Create a folder called `photos` next to `index.html` and add JPG files with these exact names. Anything missing is simply left out – the page never shows empty boxes. If no gallery photos exist, the "Inside CityCube" section and its menu link are hidden automatically.

| File | What to shoot | Size |
|------|---------------|------|
| `photos/hero.jpg` | Wide shot down the main aisle or across the warehouse floor, well lit. Used as the dim background of the top banner. | 1920 px wide |
| `photos/1.jpg` | Bigger lead picture: the warehouse interior with racked/stacked goods | 1600 px wide |
| `photos/2.jpg` | A pallet with its QR label and wrap, close up | 1200 px wide |
| `photos/3.jpg` | Forklift or loading/unloading at the dock | 1200 px wide |
| `photos/4.jpg` | A team member photographing goods at check-in | 1200 px wide |
| `photos/5.jpg` | Neatly arranged goods ready for collection | 1200 px wide |

Tips: shoot landscape in daylight or with all lights on, tidy the frame first, keep customer goods and labels unreadable (no customer names or ID papers visible), and compress each file to about 200–400 KB (free: squoosh.app). Upload the `photos` folder to the same GitHub repository.

### Pictures from the internet
I could not download photos from this workspace, so the page is set up for you to add them in two minutes:
1. Search free-to-use sites – unsplash.com, pexels.com or pixabay.com (free for commercial use, no credit needed; check each site's licence note) – for: "warehouse interior", "warehouse pallets racking", "forklift warehouse", "warehouse worker scanning", "stacked boxes warehouse".
2. Download the images, rename them to the file names above and put them in `photos/`.
3. Or, instead of files, paste full `https://…jpg` addresses into `PHOTO_HERO` and `PHOTOS` in the `EDIT THESE` block. (Files you host yourself are more reliable than links to other sites.)
Your own photos beat stock photos: customers can tell, and it shows who they are really dealing with.
