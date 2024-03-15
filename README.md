# KB-API

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




