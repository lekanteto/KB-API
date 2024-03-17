# KB-API

## Information sources
- [https://www.bazun.me/blog/kiterboard/](https://www.bazun.me/blog/kiterboard/)
- [https://tim.wants.coffee/posts/kilterboard-app/](https://tim.wants.coffee/posts/kilterboard-app/)
- [BoardLib](https://github.com/lemeryfertitta/BoardLib)
- [https://gitlab.com/terminallyill/waydroid-mitmproxy-guide](https://gitlab.com/terminallyill/waydroid-mitmproxy-guide)

## Login
```http
POST https://kilterboardapp.com/sessions
Content-Type: application/json
```

```json
{
    "password": "my password",
    "pp": "accepted",
    "tou": "accepted",
    "ua": "app",
    "username": "my username"
}
```
The response contains a session token (my_session_token) and a user id (my_id) that are used in later API calls.

## Logout
```http
DELETE https://kilterboardapp.com/sessions/my_session_token
Authorization: Bearer my_session_token
```

## Sync
```http
POST https://api.kilterboardapp.com/v1/sync
Authorization: Bearer my_session_token
```

```json
{
    "GET": {
        "query": {
            "include_all_beta_links": 1,
            "include_multiframe_climbs": 1,
            "include_null_climb_stats": 1,
            "syncs": {
                "shared_syncs": [
                    {
                        "last_synchronized_at": "2021-11-01 21:39:02.287083",
                        "table_name": "gyms"
                    },
                    {
                        "last_synchronized_at": "2021-11-01 21:39:02.287083",
                        "table_name": "boards"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "attempts"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "kits"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "products"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "product_sizes"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "holes"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "leds"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "sets"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "products_angles"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "layouts"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "product_sizes_layouts_sets"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "placement_roles"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "placements"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "climbs"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "climb_stats"
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:13:38.533549",
                        "table_name": "beta_links"
                    }
                ],
                "user_syncs": [
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "ascents",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "bids",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "circuits",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "draft_climbs",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "tags",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "users",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "wall_expungements",
                        "user_id": my_id
                    },
                    {
                        "last_synchronized_at": "2024-03-15 11:08:37.599407",
                        "table_name": "walls",
                        "user_id": my_id
                    }
                ]
            },
            "tables": [
                "products",
                "product_sizes",
                "holes",
                "leds",
                "products_angles",
                "layouts",
                "product_sizes_layouts_sets",
                "placements",
                "sets",
                "placement_roles",
                "climbs",
                "climb_stats",
                "beta_links",
                "attempts",
                "kits",
                "users",
                "walls",
                "wall_expungements",
                "draft_climbs",
                "ascents",
                "bids",
                "tags",
                "circuits"
            ],
            "user_id": my_id
        }
    },
    "client": {
        "enforces_layout_passwords": 1,
        "enforces_product_passwords": 1,
        "manages_power_responsibly": 1,
        "ufd": 1
    }
}
```

## User data including circuits
```http
GET https://api.kilterboardapp.com/v2/users/my_id
Authorization: Bearer my_session_token
```

# Dimensions 12x12 w/ kb
x 0 - 144
y 0 - 156




