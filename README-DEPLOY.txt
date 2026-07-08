KHOSHBIN ORTHOPAEDICS — GOING LIVE ON GITHUB PAGES
Final launch build. Draft bars and internal review notes removed. Patient
disclaimers kept (those are for patients and belong on the live site).

WHAT'S IN THIS ZIP
  A single folder of files: 25 web pages, styles.css, 5 PDFs (referral form,
  QR posters, front-desk cards), 4 operating-room video clips, plus the files
  GitHub Pages needs (.nojekyll, CNAME, robots.txt, sitemap.xml).
  These files ARE the website. Upload the CONTENTS of the folder to the repo
  root (not the folder itself). The pages link to each other and to the PDFs
  and videos by relative name, so they must all sit together in the root.

--------------------------------------------------------------------------------
PART 1 — CREATE THE REPOSITORY AND UPLOAD (about 10 minutes)
--------------------------------------------------------------------------------
1. Sign in at https://github.com (create a free account if needed).

2. Create the repository:
   - Click the "+" (top right) > "New repository".
   - Repository name: drkhoshbin   (any name is fine; this is not the web address)
   - Set it to PUBLIC. (GitHub Pages needs public on the free plan.)
   - Do NOT tick "Add a README". Leave everything else empty.
   - Click "Create repository".

3. Upload the files:
   - On the new empty repo page, click "uploading an existing file"
     (the link in the "Quick setup" box), or go to Add file > Upload files.
   - Open the unzipped folder on your computer, select ALL the files inside it
     (including the hidden .nojekyll — see the note below), and drag them into
     the browser upload area.
   - Scroll down and click "Commit changes".

   NOTE ON THE HIDDEN FILE (.nojekyll):
   - Its name starts with a dot, so your computer may hide it.
   - Mac: in Finder press  Cmd + Shift + .  to show hidden files, then include it.
   - Windows: in File Explorer, View > Show > Hidden items, then include it.
   - If you can't get it uploaded, do this instead after uploading everything
     else: on the repo page click Add file > Create new file, type  .nojekyll
     as the name, leave the file empty, and commit. (It stops GitHub from
     mishandling files and folders; the site works better with it.)

4. Turn on GitHub Pages:
   - In the repo, go to Settings > Pages (left sidebar).
   - Under "Build and deployment", Source: "Deploy from a branch".
   - Branch: "main"  and folder "/ (root)".  Click Save.
   - Wait 1-2 minutes. A message appears with your live address, which at this
     stage is:  https://YOUR-USERNAME.github.io/drkhoshbin/
   - Open it to confirm the site works. (The custom domain comes next.)

--------------------------------------------------------------------------------
PART 2 — CONNECT THE CUSTOM DOMAIN drkhoshbin.ca (at your registrar)
--------------------------------------------------------------------------------
The CNAME file in this upload already tells GitHub the domain is drkhoshbin.ca.
Now point the domain at GitHub. Log in to wherever the domain was bought
(e.g., GoDaddy) and open its DNS settings.

5. Add four A records on the root (name "@"), each pointing to GitHub:
      185.199.108.153
      185.199.109.153
      185.199.110.153
      185.199.111.153
   (Type: A, Name: @, Value: each IP above. Four separate A records.)

6. Add one CNAME record:
      Type: CNAME   Name: www   Value: YOUR-USERNAME.github.io
   (Use your actual GitHub username. Note this is a DNS CNAME record, which is
   different from the CNAME file already in the repo.)

7. Remove the registrar's default "parked" A record if present, and turn OFF
   any domain forwarding/redirect the registrar set up.

8. Back in GitHub, Settings > Pages > "Custom domain": type  drkhoshbin.ca
   and Save. GitHub re-checks the DNS.

9. HTTPS: DNS can take from a few minutes up to 24 hours to verify. Once it
   shows verified, tick "Enforce HTTPS". If it seems stuck, clear the custom
   domain field, Save, wait a minute, retype drkhoshbin.ca, and Save again.

--------------------------------------------------------------------------------
PART 3 — AFTER IT'S LIVE
--------------------------------------------------------------------------------
- Scan-test the QR codes on the posters and front-desk cards; they point to
  drkhoshbin.ca and only resolve once the domain and HTTPS are live.
- Play one of the operating-room videos on the live site to confirm playback.
- Google Search Console (https://search.google.com/search-console): add the
  property for drkhoshbin.ca, verify it, and submit  sitemap.xml . Getting
  indexed takes days to weeks. The single strongest boost is an inbound link
  from St. Michael's / Unity Health.

TO UPDATE THE SITE LATER
  Edit or re-upload files in the repo (Add file > Upload files, keep the same
  names, commit). The site republishes automatically in a minute or two.
  Never commit a referral form that has any patient details filled in.

STILL WORTH CONFIRMING (not blockers to the mechanics above, but before you
promote the site widely): the St. Michael's / Unity Health communications
clearance for the hospital name and the operating-room photos and videos, and
that the Hana table product photo (credited to Mizuho OSI) is cleared for use.
