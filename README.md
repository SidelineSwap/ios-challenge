# sls-ios-challenge

## Main Task

1. Implement a scrollable collection
    - Each cell (Item) must have an image, title, seller's name, and price
    - Each cell has fixed dimensions
    - When a cell is clicked, nothing needs to happen, unless you want to get fancy.
    - Data for the scrollable collection must be retrieved from our public API
    - Implement infinite pagination
2. Implement a search bar
    - The search bar is docked at the top of the screen
    - Implement a product search by keyword
    - Parameterize the request to our public API

## Optional Subtasks

1. Implement a loading indicator when loading an image.
2. Implement error handling, if a bad response code comes from our API.
3. Implement debounced type ahead search.
4. Implement an image caching mechanism.
5. Invent your own functionality.

## Technical details

1. Use the latest Xcode version (not beta).
2. Use > Swift 5.
3. Minimum iOS version 13.0.
4. Any architecture is fine. We like to see some focus on clean separation of concerns.
5. Use any frameworks you need.

## Public API

__Request__

```text
GET https://api.sidelineswap.com/v2/facet_items?q=nike%20bag&page=2
```

__Response__

```json
{
    "data": [
        {
            "id": 3789009,
            "state": "available",
            "name": "Nike Rival Zoom Rival D",
            "category_1": "other-others",
            "category_2": null,
            "price": 30,
            "list_price": 30,
            "price_retail": null,
            "condition_detail": {
                "id": 31,
                "type": "condition",
                "url": "https://sidelineswap.com/shop/other-others/new/l76743",
                "destination_lander_name": "New Other",
                "slug": "new",
                "name": "New"
            },
            "url": "https://sidelineswap.com/gear/other-others/3789009-nike-rival-zoom-rival-d",
            "favoriters_count": 0,
            "favorite": null,
            "sync_gmc": false,
            "visit_count": 1,
            "created_at": "2021-09-13T08:48:38.000-04:00",
            "updated_at": "2021-09-13T08:48:40.000-04:00",
            "label": null,
            "actions": [],
            "categories": [],
            "images": [],
            "seller": {
                "id": 977383,
                "username": "NJHoward",
                "emblems": []
            },
            "primary_image": {
                "id": 22370963,
                "thumb_url": "https://images.sidelineswap.com/production/022/370/963/c13569827a2e6f37_thumb.jpeg",
                "mobile_thumb_url": "https://images.sidelineswap.com/production/022/370/963/c13569827a2e6f37_mobile_thumb.jpeg",
                "small_url": "https://images.sidelineswap.com/production/022/370/963/c13569827a2e6f37_small.jpeg",
                "large_url": "https://images.sidelineswap.com/production/022/370/963/c13569827a2e6f37_original.jpeg"
            }
        },
        ...
        ],
        "paging": {
            "total_count": 167,
            "total_count_truncated": false,
            "total_pages": 9,
            "page_size": 20,
            "page": 2,
            "has_next_page": true
        }
    }
}
```
