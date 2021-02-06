# ScandiSent
Sentiment Corpus for Swedish 🇸🇪 Norwegian 🇳🇴 Danish 🇩🇰 Finnish 🇫🇮 (and English 🏴󠁧󠁢󠁥󠁮󠁧󠁿)

## Information
The corpus is crawled from [se.trustpilot.com](https://se.trustpilot.com/), [no.trustpilot.com](https://no.trustpilot.com/), [dk.trustpilot.com](https://dk.trustpilot.com/), [fi.trustpilot.com](https://fi.trustpilot.com/) and [trustpilot.com](https://trustpilot.com/).
It consists of reviews from all the corresponding 22 categories:

```javascript
categories = ['animals_pets', 'electronics_technology', 'events_entertainment', 'vehicles_transportation',
'business_services', 'health_medical', 'home_garden', 'hobbies_crafts', 'home_services',
'legal_services_government', 'construction_manufactoring', 'food_beverages_tobacco', 'media_publishing',
'money_insurance', 'travel_vacation', 'restaurants_bars', 'public_local_services', 'shopping_fashion',
'education_training', 'beauty_wellbeing', 'sports', 'housing_utility_company']
```

The size for each language is 10 000 texts evenly balanced between positive and negative reviews. A positive review is considered as a text with the rating `4 or 5`, and a negative review is rated as `1 or 2`. The texts rated as `3` were not used. The zip files consist of csv files for each language with the columns `text` and `label`, were `label` == `1` is a positive review and `label` == `0`is a negative review.

For our paper: `Stop Training, Start Translating` we used the first 7500 texts for training and the last 2500 texts for evaluating.

#### [ScandiSent.zip](ScandiSent.zip) 🇸🇪 🇳🇴 🇩🇰 🇫🇮 + 🏴󠁧󠁢󠁥󠁮󠁧󠁿
Is the raw data for each language where we used [fastText](https://fasttext.cc/docs/en/language-identification.html) language identification to ensure that the texts were of the right language.

#### [ScandiSent-mt.zip](ScandiSent-mt.zip) 🏴󠁧󠁢󠁥󠁮󠁧󠁿
Consists of the raw data from `ScandiSent` machine translated to English 🏴󠁧󠁢󠁥󠁮󠁧󠁿 using Googles Neural Machine Translation API.

## Version 1.0
2021-02-06
