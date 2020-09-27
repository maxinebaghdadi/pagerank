# Pagerank

This repo implements Sergey Brin and Larry Pages' Page Rank search algorithm for the website https://www.lawfareblog.com

## Task One
**Part One**
```
python3 pagerank.py --data=./small.csv.gz --verbose
DEBUG:root:computing indices
DEBUG:root:computing values
INFO:root:rank=0 pagerank=1.0908e+00 url=4
INFO:root:rank=1 pagerank=8.7980e-01 url=6
INFO:root:rank=2 pagerank=7.3707e-01 url=5
INFO:root:rank=3 pagerank=6.9623e-01 url=2
INFO:root:rank=4 pagerank=4.2704e-01 url=3
INFO:root:rank=5 pagerank=3.9290e-01 url=1
```
**Part Two**
```
python3 pagerank.py --data=./lawfareblog.csv.gz --search_query='corona'
INFO:root:rank=0 pagerank=3.0175e-02 url=www.lawfareblog.com/lawfare-podcast-united-nations-and-coronavirus-crisis
INFO:root:rank=1 pagerank=2.6610e-02 url=www.lawfareblog.com/house-oversight-committee-holds-day-two-hearing-government-coronavirus-response
INFO:root:rank=2 pagerank=1.7209e-02 url=www.lawfareblog.com/britains-coronavirus-response
INFO:root:rank=3 pagerank=1.6732e-02 url=www.lawfareblog.com/prosecuting-purposeful-coronavirus-exposure-terrorism
INFO:root:rank=4 pagerank=1.5532e-02 url=www.lawfareblog.com/israeli-emergency-regulations-location-tracking-coronavirus-carriers
INFO:root:rank=5 pagerank=1.5099e-02 url=www.lawfareblog.com/why-congress-conducting-business-usual-face-coronavirus
INFO:root:rank=6 pagerank=1.4955e-02 url=www.lawfareblog.com/livestream-house-oversight-committee-holds-hearing-government-coronavirus-response
INFO:root:rank=7 pagerank=1.4849e-02 url=www.lawfareblog.com/congressional-homeland-security-committees-seek-ways-support-state-federal-responses-coronavirus
INFO:root:rank=8 pagerank=1.4424e-02 url=www.lawfareblog.com/paper-hearing-experts-debate-digital-contact-tracing-and-coronavirus-privacy-concerns
INFO:root:rank=9 pagerank=1.3404e-02 url=www.lawfareblog.com/cyberlaw-podcast-how-israel-fighting-coronavirus
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --search_query='trump'
INFO:root:rank=0 pagerank=4.2280e-01 url=www.lawfareblog.com/donald-trump-and-politically-weaponized-executive-branch
INFO:root:rank=1 pagerank=3.9297e-01 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=2 pagerank=2.2943e-01 url=www.lawfareblog.com/trump-administrations-worrying-new-policy-israeli-settlements
INFO:root:rank=3 pagerank=2.1147e-01 url=www.lawfareblog.com/document-trump-revokes-obama-executive-order-counterterrorism-strike-casualty-reporting
INFO:root:rank=4 pagerank=2.0324e-01 url=www.lawfareblog.com/dc-circuit-overrules-district-courts-due-process-ruling-qasim-v-trump
INFO:root:rank=5 pagerank=1.8675e-01 url=www.lawfareblog.com/how-trumps-approach-middle-east-ignores-past-future-and-human-condition
INFO:root:rank=6 pagerank=1.6584e-01 url=www.lawfareblog.com/why-trump-cant-buy-greenland
INFO:root:rank=7 pagerank=1.4754e-01 url=www.lawfareblog.com/oral-argument-summary-qassim-v-trump
INFO:root:rank=8 pagerank=1.4090e-01 url=www.lawfareblog.com/dc-circuit-court-denies-trump-rehearing-mazars-case
INFO:root:rank=9 pagerank=1.3857e-01 url=www.lawfareblog.com/second-circuit-rules-mazars-must-hand-over-trump-tax-returns-new-york-prosecutors
```

```
INFO:root:rank=0 pagerank=4.2207e-01 url=www.lawfareblog.com/praise-presidents-iran-tweets
INFO:root:rank=1 pagerank=1.9159e-01 url=www.lawfareblog.com/how-us-iran-tensions-could-disrupt-iraqs-fragile-peace
INFO:root:rank=2 pagerank=1.1614e-01 url=www.lawfareblog.com/cyber-command-operational-update-clarifying-june-2019-iran-operation
INFO:root:rank=3 pagerank=9.5624e-02 url=www.lawfareblog.com/aborted-iran-strike-fine-line-between-necessity-and-revenge
INFO:root:rank=4 pagerank=5.5515e-02 url=www.lawfareblog.com/iranian-hostage-crisis-and-its-effect-american-politics
INFO:root:rank=5 pagerank=5.5179e-02 url=www.lawfareblog.com/parsing-state-departments-letter-use-force-against-iran
INFO:root:rank=6 pagerank=5.4256e-02 url=www.lawfareblog.com/announcing-united-states-and-use-force-against-iran-new-lawfare-e-book
INFO:root:rank=7 pagerank=5.2631e-02 url=www.lawfareblog.com/trump-moves-cut-irans-oil-revenues-whats-his-endgame
INFO:root:rank=8 pagerank=4.7311e-02 url=www.lawfareblog.com/us-names-iranian-revolutionary-guard-terrorist-organization-and-sanctions-international-criminal
INFO:root:rank=9 pagerank=3.9046e-02 url=www.lawfareblog.com/iran-shoots-down-us-drone-domestic-and-international-legal-implications
```
**Part Three**
```
python3 pagerank.py --data=./lawfareblog.csv.gz
INFO:root:rank=0 pagerank=5.3262e+01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
INFO:root:rank=1 pagerank=5.3262e+01 url=www.lawfareblog.com/lawfare-job-board
INFO:root:rank=2 pagerank=5.3262e+01 url=www.lawfareblog.com/masthead
INFO:root:rank=3 pagerank=5.3262e+01 url=www.lawfareblog.com/litigation-documents-resources-related-travel-ban
INFO:root:rank=4 pagerank=5.3262e+01 url=www.lawfareblog.com/subscribe-lawfare
INFO:root:rank=5 pagerank=5.3262e+01 url=www.lawfareblog.com/documents-related-mueller-investigation
INFO:root:rank=6 pagerank=5.3262e+01 url=www.lawfareblog.com/topics
INFO:root:rank=7 pagerank=5.3262e+01 url=www.lawfareblog.com/our-comments-policy
INFO:root:rank=8 pagerank=5.3262e+01 url=www.lawfareblog.com/upcoming-events
INFO:root:rank=9 pagerank=5.3262e+01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2
INFO:root:rank=0 pagerank=2.6856e+01 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=1 pagerank=1.7573e+01 url=www.lawfareblog.com/livestream-nov-21-impeachment-hearings-0
INFO:root:rank=2 pagerank=1.7454e+01 url=www.lawfareblog.com/opening-statement-david-holmes
INFO:root:rank=3 pagerank=1.1628e+01 url=www.lawfareblog.com/senate-examines-threats-homeland
INFO:root:rank=4 pagerank=1.0791e+01 url=www.lawfareblog.com/what-make-first-day-impeachment-hearings
INFO:root:rank=5 pagerank=1.0787e+01 url=www.lawfareblog.com/livestream-house-armed-services-committee-hearing-f-35-program
INFO:root:rank=6 pagerank=1.0746e+01 url=www.lawfareblog.com/whats-house-resolution-impeachment
INFO:root:rank=7 pagerank=1.0143e+01 url=www.lawfareblog.com/congress-us-policy-toward-syria-and-turkey-overview-recent-hearings
INFO:root:rank=8 pagerank=9.8176e+00 url=www.lawfareblog.com/summary-david-holmess-deposition-testimony
INFO:root:rank=9 pagerank=5.7312e+00 url=www.lawfareblog.com/events
```

**Part Four**
```
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose 
DEBUG:root:computing indices
DEBUG:root:computing values
INFO:root:rank=0 pagerank=5.3262e+01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
INFO:root:rank=1 pagerank=5.3262e+01 url=www.lawfareblog.com/lawfare-job-board
INFO:root:rank=2 pagerank=5.3262e+01 url=www.lawfareblog.com/masthead
INFO:root:rank=3 pagerank=5.3262e+01 url=www.lawfareblog.com/litigation-documents-resources-related-travel-ban
INFO:root:rank=4 pagerank=5.3262e+01 url=www.lawfareblog.com/subscribe-lawfare
INFO:root:rank=5 pagerank=5.3262e+01 url=www.lawfareblog.com/documents-related-mueller-investigation
INFO:root:rank=6 pagerank=5.3262e+01 url=www.lawfareblog.com/topics
INFO:root:rank=7 pagerank=5.3262e+01 url=www.lawfareblog.com/our-comments-policy
INFO:root:rank=8 pagerank=5.3262e+01 url=www.lawfareblog.com/upcoming-events
INFO:root:rank=9 pagerank=5.3262e+01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose --alpha=0.99999
DEBUG:root:computing indices
DEBUG:root:computing values
INFO:root:rank=0 pagerank=1.3771e+03 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
INFO:root:rank=1 pagerank=1.3771e+03 url=www.lawfareblog.com/lawfare-job-board
INFO:root:rank=2 pagerank=1.3771e+03 url=www.lawfareblog.com/documents-related-mueller-investigation
INFO:root:rank=3 pagerank=1.3771e+03 url=www.lawfareblog.com/litigation-documents-resources-related-travel-ban
INFO:root:rank=4 pagerank=1.3771e+03 url=www.lawfareblog.com/subscribe-lawfare
INFO:root:rank=5 pagerank=1.3771e+03 url=www.lawfareblog.com/topics
INFO:root:rank=6 pagerank=1.3771e+03 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
INFO:root:rank=7 pagerank=1.3771e+03 url=www.lawfareblog.com/our-comments-policy
INFO:root:rank=8 pagerank=1.3771e+03 url=www.lawfareblog.com/upcoming-events
INFO:root:rank=9 pagerank=1.3771e+03 url=www.lawfareblog.com/masthead
```

```
DEBUG:root:computing indices
DEBUG:root:computing values
INFO:root:rank=0 pagerank=2.6856e+01 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=1 pagerank=1.7573e+01 url=www.lawfareblog.com/livestream-nov-21-impeachment-hearings-0
INFO:root:rank=2 pagerank=1.7454e+01 url=www.lawfareblog.com/opening-statement-david-holmes
INFO:root:rank=3 pagerank=1.1628e+01 url=www.lawfareblog.com/senate-examines-threats-homeland
INFO:root:rank=4 pagerank=1.0791e+01 url=www.lawfareblog.com/what-make-first-day-impeachment-hearings
INFO:root:rank=5 pagerank=1.0787e+01 url=www.lawfareblog.com/livestream-house-armed-services-committee-hearing-f-35-program
INFO:root:rank=6 pagerank=1.0746e+01 url=www.lawfareblog.com/whats-house-resolution-impeachment
INFO:root:rank=7 pagerank=1.0143e+01 url=www.lawfareblog.com/congress-us-policy-toward-syria-and-turkey-overview-recent-hearings
INFO:root:rank=8 pagerank=9.8176e+00 url=www.lawfareblog.com/summary-david-holmess-deposition-testimony
INFO:root:rank=9 pagerank=5.7312e+00 url=www.lawfareblog.com/events
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose --filter_ratio=0.2 --alpha=0.99999
DEBUG:root:computing indices
DEBUG:root:computing values
INFO:root:rank=0 pagerank=3.6819e+03 url=www.lawfareblog.com/covid-19-speech-and-surveillance-response
INFO:root:rank=1 pagerank=3.6817e+03 url=www.lawfareblog.com/lawfare-live-covid-19-speech-and-surveillance
INFO:root:rank=2 pagerank=5.3428e+02 url=www.lawfareblog.com/cost-using-zero-days
INFO:root:rank=3 pagerank=2.6278e+02 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=4 pagerank=1.8033e+02 url=www.lawfareblog.com/events
INFO:root:rank=5 pagerank=1.6982e+02 url=www.lawfareblog.com/senate-examines-threats-homeland
INFO:root:rank=6 pagerank=1.6754e+02 url=www.lawfareblog.com/lawfare-podcast-former-congressman-brian-baird-and-daniel-schuman-how-congress-can-continue-function
INFO:root:rank=7 pagerank=1.6423e+02 url=www.lawfareblog.com/what-make-first-day-impeachment-hearings
INFO:root:rank=8 pagerank=1.6423e+02 url=www.lawfareblog.com/livestream-house-armed-services-committee-hearing-f-35-program
INFO:root:rank=9 pagerank=1.6415e+02 url=www.lawfareblog.com/whats-house-resolution-impeachment
```

## Task Two

**Part One**
```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='corona'
INFO:root:rank=0 pagerank=4.8010e+00 url=www.lawfareblog.com/covid-19-speech-and-surveillance-response
INFO:root:rank=1 pagerank=4.8008e+00 url=www.lawfareblog.com/lawfare-live-covid-19-speech-and-surveillance
INFO:root:rank=2 pagerank=9.8843e-01 url=www.lawfareblog.com/chinatalk-how-party-takes-its-propaganda-global
INFO:root:rank=3 pagerank=5.7034e-01 url=www.lawfareblog.com/trump-cant-reopen-country-over-state-objections
INFO:root:rank=4 pagerank=5.3873e-01 url=www.lawfareblog.com/rational-security-my-corona-edition
INFO:root:rank=5 pagerank=5.3873e-01 url=www.lawfareblog.com/brexit-not-immune-coronavirus
INFO:root:rank=6 pagerank=5.0694e-01 url=www.lawfareblog.com/prosecuting-purposeful-coronavirus-exposure-terrorism
INFO:root:rank=7 pagerank=5.0694e-01 url=www.lawfareblog.com/britains-coronavirus-response
INFO:root:rank=8 pagerank=4.8629e-01 url=www.lawfareblog.com/lawfare-podcast-mom-and-dad-talk-clinical-trials-pandemic
INFO:root:rank=9 pagerank=4.4195e-01 url=www.lawfareblog.com/lawfare-podcast-united-nations-and-coronavirus-crisis
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --search_query='corona'
INFO:root:rank=0 pagerank=7.0192e-01 url=www.lawfareblog.com/congress-needs-coronavirus-failsafe-its-too-late
INFO:root:rank=1 pagerank=3.5540e-01 url=www.lawfareblog.com/house-oversight-committee-holds-day-two-hearing-government-coronavirus-response
INFO:root:rank=2 pagerank=3.0870e-01 url=www.lawfareblog.com/britains-coronavirus-response
INFO:root:rank=3 pagerank=3.0641e-01 url=www.lawfareblog.com/prosecuting-purposeful-coronavirus-exposure-terrorism
INFO:root:rank=4 pagerank=3.0105e-01 url=www.lawfareblog.com/livestream-house-oversight-committee-holds-hearing-government-coronavirus-response
INFO:root:rank=5 pagerank=2.9014e-01 url=www.lawfareblog.com/paper-hearing-experts-debate-digital-contact-tracing-and-coronavirus-privacy-concerns
INFO:root:rank=6 pagerank=2.6583e-01 url=www.lawfareblog.com/why-congress-conducting-business-usual-face-coronavirus
INFO:root:rank=7 pagerank=1.6576e-01 url=www.lawfareblog.com/lawfare-podcast-united-nations-and-coronavirus-crisis
INFO:root:rank=8 pagerank=1.5861e-01 url=www.lawfareblog.com/israeli-emergency-regulations-location-tracking-coronavirus-carriers
INFO:root:rank=9 pagerank=1.1787e-01 url=www.lawfareblog.com/congressional-homeland-security-committees-seek-ways-support-state-federal-responses-coronavirus
```

**Part Two**
```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='corona' --search_query='-corona'
INFO:root:rank=0 pagerank=4.8010e+00 url=www.lawfareblog.com/covid-19-speech-and-surveillance-response
INFO:root:rank=1 pagerank=4.8008e+00 url=www.lawfareblog.com/lawfare-live-covid-19-speech-and-surveillance
INFO:root:rank=2 pagerank=9.8843e-01 url=www.lawfareblog.com/chinatalk-how-party-takes-its-propaganda-global
INFO:root:rank=3 pagerank=5.7034e-01 url=www.lawfareblog.com/trump-cant-reopen-country-over-state-objections
INFO:root:rank=4 pagerank=4.8629e-01 url=www.lawfareblog.com/lawfare-podcast-mom-and-dad-talk-clinical-trials-pandemic
INFO:root:rank=5 pagerank=4.2211e-01 url=www.lawfareblog.com/fault-lines-foreign-policy-quarantined
INFO:root:rank=6 pagerank=4.1513e-01 url=www.lawfareblog.com/limits-world-health-organization
INFO:root:rank=7 pagerank=3.7045e-01 url=www.lawfareblog.com/chinatalk-dispatches-shanghai-beijing-and-hong-kong
INFO:root:rank=8 pagerank=3.2373e-01 url=www.lawfareblog.com/trump-cant-play-politics-aid-states
INFO:root:rank=9 pagerank=3.1845e-01 url=www.lawfareblog.com/lawfare-podcast-former-congressman-brian-baird-and-daniel-schuman-how-congress-can-continue-function
```

**Part Three**
```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='philippines' --search_query='lebanon'
INFO:root:rank=0 pagerank=3.9626e-03 url=www.lawfareblog.com/country-fire-lebanons-october-revolution-context
INFO:root:rank=1 pagerank=1.5163e-09 url=www.lawfareblog.com/lebanon-making-fragile-progress-now-wrong-time-pull-us-assistance
INFO:root:rank=2 pagerank=0.0000e+00 url=www.lawfareblog.com/dispatch-1-tragic-choices-lebanon-overwhelmed
INFO:root:rank=3 pagerank=0.0000e+00 url=www.lawfareblog.com/dispatch-3-strange-sectarian-peace-syrian-refugees-lebanon
INFO:root:rank=4 pagerank=0.0000e+00 url=www.lawfareblog.com/another-war-lebanon
INFO:root:rank=5 pagerank=0.0000e+00 url=www.lawfareblog.com/keeping-peace-lebanon
INFO:root:rank=6 pagerank=0.0000e+00 url=www.lawfareblog.com/way-out-libya-conundrum-lebanon-and-somalia-analogies
INFO:root:rank=7 pagerank=0.0000e+00 url=www.lawfareblog.com/lawfare-podcast-new-arab-spring-iraq-and-lebanon
INFO:root:rank=8 pagerank=0.0000e+00 url=www.lawfareblog.com/lebanons-election-potential-departures-status-quo
INFO:root:rank=9 pagerank=0.0000e+00 url=www.lawfareblog.com/lebanons-elections-beyond-iranian-saudi-rivalry
```
