# NC land dashboard

Land for sale in Montgomery, Stanly, Anson, Richmond and Rowan Counties, North Carolina: more than 10 and less than 50 acres, under $1,000,000.

Live page: https://brentwhichel.github.io/nc-land-dashboard/

Listings are gathered from LandWatch (the Land.com network, which also covers Land And Farm, Lands of America and Land.com), Homes.com, Realtor.com, LandSearch and Redfin, then de-duplicated so each property appears once with links to every site that lists it. Photos load from the listing sites (or an aerial image where no photo was published). Distances are approximate straight-line miles from a private reference address. Listing data and photos belong to the respective sites and brokers. Confirm price, status, acreage, access and soils with the listing agent and the county before acting on anything here.

How it publishes: a GitHub Action reads the update posted to the "Publish channel (automated)" issue, commits `docs/`, clears any stuck Pages deployment, deploys the page, and replaces the issue text with a receipt. A second Action ("Map location helper") looks up approximate map locations for listings that don't publish one, using the US Census geocoder and OpenStreetMap, and saves the results on the `geo-data` branch.
