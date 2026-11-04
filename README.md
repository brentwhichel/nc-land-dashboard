# NC land dashboard

Land for sale in Montgomery and Stanly Counties, North Carolina: more than 10 and less than 50 acres, under $750,000.

Live page: https://brentwhichel.github.io/nc-land-dashboard/

Listings are gathered from LandWatch (the Land.com network, which also covers Land And Farm, Lands of America and Land.com), Homes.com, Realtor.com, LandSearch and Redfin, then de-duplicated so each property appears once with links to every site that lists it. Listing data belongs to the respective sites and brokers. Confirm price, status, acreage, access and soils with the listing agent and the county before acting on anything here.

How it publishes: a GitHub Action reads the update posted to the "Publish channel (automated)" issue, commits `docs/`, deploys it to GitHub Pages, and replaces the issue text with a receipt.
