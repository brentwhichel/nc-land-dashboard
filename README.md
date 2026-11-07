# NC land dashboard

Land for sale in Montgomery, Stanly and Anson Counties, North Carolina: more than 25 acres, under $1,000,000. Only listings with a listing photo are shown, and listings under contract are left out.

Live page: https://brentwhichel.github.io/nc-land-dashboard/

Listings are gathered from LandWatch (the Land.com network, which also covers Land And Farm, Lands of America and Land.com), Realtor.com, Redfin and Homes.com, then de-duplicated so each property appears once with links to every site that lists it. Photos load from LandWatch or Redfin. Distances are approximate driving miles and minutes (OpenStreetMap routing) from a private reference address.

The NO / Interested checkboxes are stored only in the viewer's own browser. Ticking NO hides a listing (with an Undo, and a view to bring hidden ones back). A listing marked Interested stays on the page even if a later search no longer includes it, labeled "Kept for you".

Listing data and photos belong to the respective sites and brokers. Confirm price, status, acreage, access and soils with the listing agent and the county before acting on anything here.

How it publishes: a GitHub Action reads the update posted to the "Publish channel (automated)" issue, commits `docs/`, clears any stuck Pages deployment, deploys the page, and replaces the issue text with a receipt. A second Action ("Map location helper") can look up approximate map locations for listings that don't publish one, using the US Census geocoder and OpenStreetMap, and saves the results on the `geo-data` branch.
