# flood-lookup-watch

A nightly test of the flood zone address lookup on https://floodinsurancedata.com/flood-zone-map/.

For five public addresses it asks the Census geocoder and FEMA's National Flood Hazard Layer directly, works out the
sentences the page must show (`tools/test_zonemap.py`, `oracle`), then drives the live page like a reader and checks
that it prints every one of them. A red run means the page and FEMA disagree, or FEMA did not answer.
