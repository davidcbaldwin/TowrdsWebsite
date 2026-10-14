# Towrds 10: Work With Me

Static landing page for GitHub Pages. No build step. Upload everything in this folder to the root of the repo.

## Files
- `index.html` : the full page (layout, styles, and the small script at the bottom)
- `images/` : team photo and logo
- `privacy.html` : privacy notice linked in the footer
- `p/work-with-me/index.html` : forwards the old Substack address (towrds.com/p/work-with-me) to the new page
- `og-image.png` : preview image when the link is shared on LinkedIn, email, Slack
- favicons, `site.webmanifest` : browser tab and home screen icons
- `robots.txt`, `sitemap.xml` : for search engines
- `.nojekyll` : tells GitHub Pages to serve files as-is

## Updating seats, quarter, or deadline
Open `index.html`, scroll to the bottom, and edit the block marked "Towrds 10 settings":

    var TOWRDS = {
      quarter: "Q1 FY2027",
      seatsTotal: 3,
      seatsFilled: 0,
      deadline: [2026, 12, 15]
    };

Change `seatsFilled` the day a seat fills. The top strip, seat panel, and hero line all update from it. The countdown recalculates daily on its own; after the deadline the strip shows the quarter as closed.

Note: the quarter name also appears in the page text in a few places (top strip, seat panel, hero line, video section, final call to action). When the quarter changes, search `index.html` for "Q1 FY2027" and "December 15" and update those too.

## Deploy
1. Create a repo and upload these files to the root of the `main` branch.
2. Settings > Pages: Source = "Deploy from a branch", Branch = `main`, folder = `/ (root)`. Save.
3. Custom domain: enter `www.towrds.com` and save (GitHub adds a `CNAME` file).
4. DNS: `www` CNAME to `<your-github-username>.github.io`. Apex `towrds.com` A records: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
5. Once DNS resolves, check **Enforce HTTPS**.

## After launch
- Add the site in Google Search Console and Bing Webmaster Tools, then submit `sitemap.xml`.
- Check the share preview with LinkedIn Post Inspector.
- When analytics or the LinkedIn Insight Tag are added, update `privacy.html` to say so.
