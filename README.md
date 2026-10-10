# Google Reviews

> Google reviews for Statamic.

Syncs your Google reviews (via [Apify](https://apify.com)) into a `reviews` collection and keeps a `review` global with the average score and review count up to date.

This addon only handles the data. The frontend (review cards, masonry, summary) lives in [`letsdeploy/statamic-basecamp`](https://github.com/letsdeploy-nl/statamic-basecamp) as the `reviews` section and the `social_proof` component.

## How to Install

``` bash
composer require letsdeploy/statamic-reviews
php artisan vendor:publish --tag=ldp-reviews-collections
php artisan vendor:publish --tag=ldp-reviews-globals
```

Add to your `.env`:

```
APIFY_TOKEN=
GOOGLE_PLACE_IDS=        # comma separated
GOOGLE_MAX_REVIEWS=1000
```

## How to Use

``` bash
php please reviews:sync
```
