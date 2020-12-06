# Pagerank

This repo implements Sergey Brin and Larry Pages' Page Rank search algorithm for the website https://www.lawfareblog.com

# December 2020

```
python3 pagerank.py --data=./small.csv.gz --verbose
DEBUG:root:computing indices
DEBUG:root:computing values
DEBUG:root:i=0 accuracy=tensor(0.2563)
DEBUG:root:i=1 accuracy=tensor(0.1184)
DEBUG:root:i=2 accuracy=tensor(0.0707)
DEBUG:root:i=3 accuracy=tensor(0.0318)
DEBUG:root:i=4 accuracy=tensor(0.0205)
DEBUG:root:i=5 accuracy=tensor(0.0101)
DEBUG:root:i=6 accuracy=tensor(0.0064)
DEBUG:root:i=7 accuracy=tensor(0.0034)
DEBUG:root:i=8 accuracy=tensor(0.0021)
DEBUG:root:i=9 accuracy=tensor(0.0012)
DEBUG:root:i=10 accuracy=tensor(0.0007)
DEBUG:root:i=11 accuracy=tensor(0.0004)
DEBUG:root:i=12 accuracy=tensor(0.0002)
DEBUG:root:i=13 accuracy=tensor(0.0001)
DEBUG:root:i=14 accuracy=tensor(8.1083e-05)
DEBUG:root:i=15 accuracy=tensor(4.7251e-05)
DEBUG:root:i=16 accuracy=tensor(2.7704e-05)
DEBUG:root:i=17 accuracy=tensor(1.6164e-05)
DEBUG:root:i=18 accuracy=tensor(9.4778e-06)
DEBUG:root:i=19 accuracy=tensor(5.5066e-06)
DEBUG:root:i=20 accuracy=tensor(3.2042e-06)
DEBUG:root:i=21 accuracy=tensor(1.8612e-06)
DEBUG:root:i=22 accuracy=tensor(1.1283e-06)
DEBUG:root:i=23 accuracy=tensor(6.1907e-07)
INFO:root:rank=0 pagerank=6.6270e-01 url=4
INFO:root:rank=1 pagerank=5.2179e-01 url=6
INFO:root:rank=2 pagerank=4.1434e-01 url=5
INFO:root:rank=3 pagerank=2.3175e-01 url=2
INFO:root:rank=4 pagerank=1.8590e-01 url=3
INFO:root:rank=5 pagerank=1.6917e-01 url=1
```


```
python3 pagerank.py --data=./lawfareblog.csv.gz --search_query='corona'
INFO:gensim.models.keyedvectors:precomputing L2-norms of word weight vectors
INFO:root:rank=0 pagerank=1.0038e-03 url=www.lawfareblog.com/lawfare-podcast-united-nations-and-coronavirus-crisis
INFO:root:rank=1 pagerank=8.9224e-04 url=www.lawfareblog.com/house-oversight-committee-holds-day-two-hearing-government-coronavirus-response
INFO:root:rank=2 pagerank=7.0390e-04 url=www.lawfareblog.com/britains-coronavirus-response
INFO:root:rank=3 pagerank=6.9153e-04 url=www.lawfareblog.com/prosecuting-purposeful-coronavirus-exposure-terrorism
INFO:root:rank=4 pagerank=6.7041e-04 url=www.lawfareblog.com/israeli-emergency-regulations-location-tracking-coronavirus-carriers
INFO:root:rank=5 pagerank=6.6256e-04 url=www.lawfareblog.com/why-congress-conducting-business-usual-face-coronavirus
INFO:root:rank=6 pagerank=6.5046e-04 url=www.lawfareblog.com/congressional-homeland-security-committees-seek-ways-support-state-federal-responses-coronavirus
INFO:root:rank=7 pagerank=6.3620e-04 url=www.lawfareblog.com/paper-hearing-experts-debate-digital-contact-tracing-and-coronavirus-privacy-concerns
INFO:root:rank=8 pagerank=6.1248e-04 url=www.lawfareblog.com/house-subcommittee-voices-concerns-over-us-management-coronavirus
INFO:root:rank=9 pagerank=6.0187e-04 url=www.lawfareblog.com/livestream-house-oversight-committee-holds-hearing-government-coronavirus-response
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --search_query='trump'
INFO:gensim.models.keyedvectors:precomputing L2-norms of word weight vectors
INFO:root:rank=0 pagerank=5.7826e-03 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=1 pagerank=5.2338e-03 url=www.lawfareblog.com/document-trump-revokes-obama-executive-order-counterterrorism-strike-casualty-reporting
INFO:root:rank=2 pagerank=5.1297e-03 url=www.lawfareblog.com/trump-administrations-worrying-new-policy-israeli-settlements
INFO:root:rank=3 pagerank=4.6599e-03 url=www.lawfareblog.com/dc-circuit-overrules-district-courts-due-process-ruling-qasim-v-trump
INFO:root:rank=4 pagerank=4.5934e-03 url=www.lawfareblog.com/donald-trump-and-politically-weaponized-executive-branch
INFO:root:rank=5 pagerank=4.3071e-03 url=www.lawfareblog.com/how-trumps-approach-middle-east-ignores-past-future-and-human-condition
INFO:root:rank=6 pagerank=4.0935e-03 url=www.lawfareblog.com/why-trump-cant-buy-greenland
INFO:root:rank=7 pagerank=3.7591e-03 url=www.lawfareblog.com/oral-argument-summary-qassim-v-trump
INFO:root:rank=8 pagerank=3.4509e-03 url=www.lawfareblog.com/dc-circuit-court-denies-trump-rehearing-mazars-case
INFO:root:rank=9 pagerank=3.4484e-03 url=www.lawfareblog.com/second-circuit-rules-mazars-must-hand-over-trump-tax-returns-new-york-prosecutors
```


```
python3 pagerank.py --data=./lawfareblog.csv.gz --search_query='iran'
INFO:gensim.models.keyedvectors:precomputing L2-norms of word weight vectors
INFO:root:rank=0 pagerank=5.1297e-03 url=www.lawfareblog.com/trump-administrations-worrying-new-policy-israeli-settlements
INFO:root:rank=1 pagerank=5.0168e-03 url=www.lawfareblog.com/update-military-commissions-continued-health-issues-recusal-motion-and-new-cell-al-iraqi
INFO:root:rank=2 pagerank=4.5746e-03 url=www.lawfareblog.com/praise-presidents-iran-tweets
INFO:root:rank=3 pagerank=4.4174e-03 url=www.lawfareblog.com/how-us-iran-tensions-could-disrupt-iraqs-fragile-peace
INFO:root:rank=4 pagerank=4.3659e-03 url=www.lawfareblog.com/haftar-attacking-tripoli-us-needs-re-engage-libya
INFO:root:rank=5 pagerank=3.4237e-03 url=www.lawfareblog.com/france-makes-play-try-foreign-fighters-iraq
INFO:root:rank=6 pagerank=2.6928e-03 url=www.lawfareblog.com/cyber-command-operational-update-clarifying-june-2019-iran-operation
INFO:root:rank=7 pagerank=2.2567e-03 url=www.lawfareblog.com/document-sens-kaine-and-young-introduce-bill-revoke-iraq-force-authorizations
INFO:root:rank=8 pagerank=1.9391e-03 url=www.lawfareblog.com/aborted-iran-strike-fine-line-between-necessity-and-revenge
INFO:root:rank=9 pagerank=1.8263e-03 url=www.lawfareblog.com/its-not-only-iraq-and-syria
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz
INFO:root:rank=0 pagerank=2.8741e-01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
INFO:root:rank=1 pagerank=2.8741e-01 url=www.lawfareblog.com/lawfare-job-board
INFO:root:rank=2 pagerank=2.8741e-01 url=www.lawfareblog.com/masthead
INFO:root:rank=3 pagerank=2.8741e-01 url=www.lawfareblog.com/litigation-documents-resources-related-travel-ban
INFO:root:rank=4 pagerank=2.8741e-01 url=www.lawfareblog.com/subscribe-lawfare
INFO:root:rank=5 pagerank=2.8741e-01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
INFO:root:rank=6 pagerank=2.8741e-01 url=www.lawfareblog.com/documents-related-mueller-investigation
INFO:root:rank=7 pagerank=2.8741e-01 url=www.lawfareblog.com/our-comments-policy
INFO:root:rank=8 pagerank=2.8741e-01 url=www.lawfareblog.com/upcoming-events
INFO:root:rank=9 pagerank=2.8741e-01 url=www.lawfareblog.com/topics
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2
INFO:root:rank=0 pagerank=3.4696e-01 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=1 pagerank=2.9521e-01 url=www.lawfareblog.com/livestream-nov-21-impeachment-hearings-0
INFO:root:rank=2 pagerank=2.9040e-01 url=www.lawfareblog.com/opening-statement-david-holmes
INFO:root:rank=3 pagerank=1.5179e-01 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
INFO:root:rank=4 pagerank=1.5099e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
INFO:root:rank=5 pagerank=1.5099e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
INFO:root:rank=6 pagerank=1.5071e-01 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
INFO:root:rank=7 pagerank=1.4957e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
INFO:root:rank=8 pagerank=1.4367e-01 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google
INFO:root:rank=9 pagerank=1.4240e-01 url=www.lawfareblog.com/lawfare-podcast-bonus-edition-gordon-sondland-vs-committee-no-bull
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose 
INFO:root:rank=0 pagerank=2.8741e-01 url=www.lawfareblog.com/about-lawfare-brief-history-term-and-site
INFO:root:rank=1 pagerank=2.8741e-01 url=www.lawfareblog.com/lawfare-job-board
INFO:root:rank=2 pagerank=2.8741e-01 url=www.lawfareblog.com/masthead
INFO:root:rank=3 pagerank=2.8741e-01 url=www.lawfareblog.com/litigation-documents-resources-related-travel-ban
INFO:root:rank=4 pagerank=2.8741e-01 url=www.lawfareblog.com/subscribe-lawfare
INFO:root:rank=5 pagerank=2.8741e-01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
INFO:root:rank=6 pagerank=2.8741e-01 url=www.lawfareblog.com/documents-related-mueller-investigation
INFO:root:rank=7 pagerank=2.8741e-01 url=www.lawfareblog.com/our-comments-policy
INFO:root:rank=8 pagerank=2.8741e-01 url=www.lawfareblog.com/upcoming-events
INFO:root:rank=9 pagerank=2.8741e-01 url=www.lawfareblog.com/topics
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose --alpha=0.99999
INFO:root:rank=0 pagerank=2.8859e-01 url=www.lawfareblog.com/snowden-revelations
INFO:root:rank=1 pagerank=2.8859e-01 url=www.lawfareblog.com/lawfare-job-board
INFO:root:rank=2 pagerank=2.8859e-01 url=www.lawfareblog.com/documents-related-mueller-investigation
INFO:root:rank=3 pagerank=2.8859e-01 url=www.lawfareblog.com/litigation-documents-resources-related-travel-ban
INFO:root:rank=4 pagerank=2.8859e-01 url=www.lawfareblog.com/subscribe-lawfare
INFO:root:rank=5 pagerank=2.8859e-01 url=www.lawfareblog.com/topics
INFO:root:rank=6 pagerank=2.8859e-01 url=www.lawfareblog.com/masthead
INFO:root:rank=7 pagerank=2.8859e-01 url=www.lawfareblog.com/our-comments-policy
INFO:root:rank=8 pagerank=2.8859e-01 url=www.lawfareblog.com/upcoming-events
INFO:root:rank=9 pagerank=2.8859e-01 url=www.lawfareblog.com/litigation-documents-related-appointment-matthew-whitaker-acting-attorney-general
```

```
(base) Maxines-MBP:pagerank maxinebaghdadi$ python3 pagerank.py --data=./lawfareblog.csv.gz --verbose --filter_ratio=0.2
INFO:root:rank=0 pagerank=3.4696e-01 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=1 pagerank=2.9521e-01 url=www.lawfareblog.com/livestream-nov-21-impeachment-hearings-0
INFO:root:rank=2 pagerank=2.9040e-01 url=www.lawfareblog.com/opening-statement-david-holmes
INFO:root:rank=3 pagerank=1.5179e-01 url=www.lawfareblog.com/lawfare-podcast-ben-nimmo-whack-mole-game-disinformation
INFO:root:rank=4 pagerank=1.5099e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1964
INFO:root:rank=5 pagerank=1.5099e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1963
INFO:root:rank=6 pagerank=1.5071e-01 url=www.lawfareblog.com/lawfare-podcast-week-was-impeachment
INFO:root:rank=7 pagerank=1.4957e-01 url=www.lawfareblog.com/todays-headlines-and-commentary-1962
INFO:root:rank=8 pagerank=1.4367e-01 url=www.lawfareblog.com/cyberlaw-podcast-mistrusting-google
INFO:root:rank=9 pagerank=1.4240e-01 url=www.lawfareblog.com/lawfare-podcast-bonus-edition-gordon-sondland-vs-committee-no-bull
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose --filter_ratio=0.2 --alpha=0.99999
INFO:root:rank=0 pagerank=7.0149e-01 url=www.lawfareblog.com/covid-19-speech-and-surveillance-response
INFO:root:rank=1 pagerank=7.0149e-01 url=www.lawfareblog.com/lawfare-live-covid-19-speech-and-surveillance
INFO:root:rank=2 pagerank=1.0552e-01 url=www.lawfareblog.com/cost-using-zero-days
INFO:root:rank=3 pagerank=3.1755e-02 url=www.lawfareblog.com/lawfare-podcast-former-congressman-brian-baird-and-daniel-schuman-how-congress-can-continue-function
INFO:root:rank=4 pagerank=2.2040e-02 url=www.lawfareblog.com/events
INFO:root:rank=5 pagerank=1.6027e-02 url=www.lawfareblog.com/water-wars-increased-us-focus-indo-pacific
INFO:root:rank=6 pagerank=1.6026e-02 url=www.lawfareblog.com/water-wars-drill-maybe-drill
INFO:root:rank=7 pagerank=1.6023e-02 url=www.lawfareblog.com/water-wars-disjointed-operations-south-china-sea
INFO:root:rank=8 pagerank=1.6020e-02 url=www.lawfareblog.com/water-wars-song-oil-and-fire
INFO:root:rank=9 pagerank=1.6020e-02 url=www.lawfareblog.com/water-wars-sinking-feeling-philippine-china-relations
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='corona'
INFO:gensim.models.keyedvectors:precomputing L2-norms of word weight vectors
INFO:root:rank=0 pagerank=6.3213e-01 url=www.lawfareblog.com/covid-19-speech-and-surveillance-response
INFO:root:rank=1 pagerank=6.3211e-01 url=www.lawfareblog.com/lawfare-live-covid-19-speech-and-surveillance
INFO:root:rank=2 pagerank=1.4962e-01 url=www.lawfareblog.com/chinatalk-how-party-takes-its-propaganda-global
INFO:root:rank=3 pagerank=1.1626e-01 url=www.lawfareblog.com/rational-security-my-corona-edition
INFO:root:rank=4 pagerank=1.1626e-01 url=www.lawfareblog.com/brexit-not-immune-coronavirus
INFO:root:rank=5 pagerank=8.8833e-02 url=www.lawfareblog.com/trump-cant-reopen-country-over-state-objections
INFO:root:rank=6 pagerank=8.5443e-02 url=www.lawfareblog.com/prosecuting-purposeful-coronavirus-exposure-terrorism
INFO:root:rank=7 pagerank=8.5443e-02 url=www.lawfareblog.com/britains-coronavirus-response
INFO:root:rank=8 pagerank=7.1883e-02 url=www.lawfareblog.com/lawfare-podcast-united-nations-and-coronavirus-crisis
INFO:root:rank=9 pagerank=6.8968e-02 url=www.lawfareblog.com/house-oversight-committee-holds-day-two-hearing-government-coronavirus-response
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='corona' --search_query='-corona'
INFO:gensim.models.keyedvectors:precomputing L2-norms of word weight vectors
INFO:root:rank=0 pagerank=6.3213e-01 url=www.lawfareblog.com/covid-19-speech-and-surveillance-response
INFO:root:rank=1 pagerank=6.3211e-01 url=www.lawfareblog.com/lawfare-live-covid-19-speech-and-surveillance
INFO:root:rank=2 pagerank=1.4962e-01 url=www.lawfareblog.com/chinatalk-how-party-takes-its-propaganda-global
INFO:root:rank=3 pagerank=8.8833e-02 url=www.lawfareblog.com/trump-cant-reopen-country-over-state-objections
INFO:root:rank=4 pagerank=6.8562e-02 url=www.lawfareblog.com/lawfare-podcast-mom-and-dad-talk-clinical-trials-pandemic
INFO:root:rank=5 pagerank=6.5838e-02 url=www.lawfareblog.com/fault-lines-foreign-policy-quarantined
INFO:root:rank=6 pagerank=6.1389e-02 url=www.lawfareblog.com/limits-world-health-organization
INFO:root:rank=7 pagerank=5.5939e-02 url=www.lawfareblog.com/chinatalk-dispatches-shanghai-beijing-and-hong-kong
INFO:root:rank=8 pagerank=5.4060e-02 url=www.lawfareblog.com/trump-asks-supreme-court-stay-congressional-subpeona-tax-returns
INFO:root:rank=9 pagerank=4.9363e-02 url=www.lawfareblog.com/us-moves-dismiss-case-against-company-linked-ira-troll-farm
```

```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='lebanon' --search_query='lebanon'
INFO:root:rank=0 pagerank=2.6187e-01 url=www.lawfareblog.com/how-us-iran-tensions-could-disrupt-iraqs-fragile-peace
INFO:root:rank=1 pagerank=2.5793e-01 url=www.lawfareblog.com/cancellation-algerias-elections-opportunity-democratization
INFO:root:rank=2 pagerank=9.5502e-02 url=www.lawfareblog.com/france-makes-play-try-foreign-fighters-iraq
INFO:root:rank=3 pagerank=8.5608e-02 url=www.lawfareblog.com/its-not-only-iraq-and-syria
INFO:root:rank=4 pagerank=8.3504e-02 url=www.lawfareblog.com/sexuality-and-gender-based-crackdowns-under-egyptian-law
INFO:root:rank=5 pagerank=8.3504e-02 url=www.lawfareblog.com/could-latest-blunder-egypts-sissi-be-nail-his-coffin
INFO:root:rank=6 pagerank=8.3504e-02 url=www.lawfareblog.com/egypts-constitutional-amendments-further-decay-state-institutions
INFO:root:rank=7 pagerank=8.3504e-02 url=www.lawfareblog.com/egypt-cracking-down-ngos-when-it-needs-them-most
INFO:root:rank=8 pagerank=8.3504e-02 url=www.lawfareblog.com/rebels-and-regime-clash-syria-while-fighting-islamic-state-iraqi-forces-enter-mosul-and-washington
INFO:root:rank=9 pagerank=7.1566e-02 url=www.lawfareblog.com/egypts-counterterrorism-law-enshrining-security-expense-civil-rights
```


# September 2020 

## Task One
**Part One:** Checking implementation of power method on small.csv.gz data 
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
**Part Two:** Testing search_query with multiple strings 
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
python3 pagerank.py --data=./lawfareblog.csv.gz --search_query='iran'
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
**Part Three:** The list of pages with the largest pagerank 
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

Applying a filter ratio to to estimate the most important articles. This function removes all the pages that have more links than the specified fraction. 

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

**Part Four:** Runtime of pagerank depends heavily on the eigengap of the $\bar\bar P$ matrix. It is bounded by an alpha parameter. I now compare previous commands with new ones that account for the alpha parameter. 

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
python3 pagerank.py --data=./lawfareblog.csv.gz --verbose --filter_ratio=0.2
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

**Part One:** Implementing the WebGraph.make_personalization_vector function to enable the --personalization_vector_query command line argument. 
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
These results are significantly different to when compared to the --search_query option. 

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

**Part Two:** Looking at webpages that relate to coronavirus but don't directly mention it.  

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

**Part Three:** Another example to coronavirus, I also looked into the query 'lebanon.'
```
python3 pagerank.py --data=./lawfareblog.csv.gz --filter_ratio=0.2 --personalization_vector_query='lebanon' --search_query='lebanon'
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
