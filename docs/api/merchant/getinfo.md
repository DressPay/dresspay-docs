# Get Merchant Info

Get basic information of a merchant by its clientid.

## Location

`/client`

## Method

`GET`

## Request Parameters

Format: `GET Query String`

- `clientid`: The ID of a merchant.

## Request Examples

`GET /client?clientid=0`

## Response

Format: `json`

- `error`: Error indicator.
- `data`: Response data (if no error).
  - `id`: The clientid of the merchant.
  - `name`: The name of the merchant.
- `reason`: Error reason (if has error).

## Response Examples

```json
{ "error": false, "data": { "id": "0", "name": "DressPay" } }
```

```json
{ "error": true, "reason": "notfound" }
```
