# community/pinterest

Pinterest API client for managing pins, boards, and media. Built on `aux4/curl`.

## Installation

```bash
aux4 aux4 pkger install community/pinterest
```

## Prerequisites

You need a Pinterest developer account and an OAuth2 access token. Create an app at [Pinterest Developers](https://developers.pinterest.com/), then generate an access token (it starts with `pina_`).

## Authentication

Login with your Pinterest access token:

```bash
aux4 pinterest login --token pina_YOUR_ACCESS_TOKEN
```

The token is saved to `.oauth/pinterest.json`. Add `.oauth/` to your `.gitignore`.

Check authentication status:

```bash
aux4 pinterest status
```

Logout:

```bash
aux4 pinterest logout
```

## Sandbox

By default, commands use the production API (`https://api.pinterest.com`). To use the sandbox environment, either pass `--apiUrl` or set the `PINTEREST_API_URL` environment variable:

```bash
# Per command
aux4 pinterest pin list --apiUrl https://api-sandbox.pinterest.com

# Or set once for all commands
export PINTEREST_API_URL=https://api-sandbox.pinterest.com
aux4 pinterest pin list
```

## Pins

### Create a pin

```bash
aux4 pinterest pin create --body '{
  "title": "My Pin",
  "description": "A great pin",
  "board_id": "123456",
  "media_source": {
    "source_type": "image_url",
    "url": "https://example.com/image.jpg"
  }
}'
```

### List pins

```bash
aux4 pinterest pin list
aux4 pinterest pin list --pageSize 10
```

### Get a pin

```bash
aux4 pinterest pin get 123456789
```

### Update a pin

```bash
aux4 pinterest pin update 123456789 --body '{"title":"Updated Title"}'
```

### Delete a pin

```bash
aux4 pinterest pin delete 123456789
```

### Save a pin to a board

```bash
aux4 pinterest pin save 123456789 --body '{"board_id":"987654"}'
```

### Pin analytics

```bash
aux4 pinterest pin analytics 123456789 --startDate 2026-01-01 --endDate 2026-01-31
```

## Boards

### Create a board

```bash
aux4 pinterest board create --body '{"name":"My Board","description":"A collection","privacy":"PUBLIC"}'
```

### List boards

```bash
aux4 pinterest board list
```

### Get a board

```bash
aux4 pinterest board get 123456
```

### Update a board

```bash
aux4 pinterest board update 123456 --body '{"name":"New Name"}'
```

### Delete a board

```bash
aux4 pinterest board delete 123456
```

### List pins on a board

```bash
aux4 pinterest board pins 123456
```

## Board Sections

### Create a section

```bash
aux4 pinterest board section create 123456 --body '{"title":"My Section"}'
```

### List sections

```bash
aux4 pinterest board section list 123456
```

### Update a section

```bash
aux4 pinterest board section update --boardId 123456 789012 --body '{"title":"New Title"}'
```

### Delete a section

```bash
aux4 pinterest board section delete --boardId 123456 789012
```

### List pins in a section

```bash
aux4 pinterest board section pins --boardId 123456 789012
```

## Search

### Search pins

```bash
aux4 pinterest search pins "summer recipes"
```

### Search boards

```bash
aux4 pinterest search boards "travel"
```

## User

### Get user info

```bash
aux4 pinterest user info
```

### User analytics

```bash
aux4 pinterest user analytics --startDate 2026-01-01 --endDate 2026-01-31
```

### List followers

```bash
aux4 pinterest user followers
```

## Media

### Register a media upload

```bash
aux4 pinterest media upload --body '{"media_type":"video"}'
```

### List media uploads

```bash
aux4 pinterest media list
```

### Get upload status

```bash
aux4 pinterest media get abc123
```

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `PINTEREST_API_URL` | Pinterest API base URL | `https://api.pinterest.com` |
