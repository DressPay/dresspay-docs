# Sign Demo Request

Sign the provided payment request for demo purpose using testing token.

## Location

`/demo/getsign`

## Method

`POST`

## Request Parameters

Format: `form-data`

- `subject`: The subject of current transaction.
- `notify_url`: (Optional, Dropped) A URL to be called back when the given transaction is finished.
- `price`: The total amount of price in the transaction. (Currently in USD only)
- `return_url`: A URL to be redirected when the given transaction is finished.
- `clientid`: (Optional, Dropped) The unique ID for merchants to identify themselves.
- `out_trade_no`: The identifier for the invoice of merchants.

## Request Examples

`POST /demo/getsign`

- `subject`: `Example Payment`
- `return_url`: `https://dresspay.org/demo?notify=yes`
- `price`: `114514`
- `out_trade_no`: `f782d822-9b51-44ad-afe4-172a4e26e463`

## Response

Format: `json`

- `error`: Error indicator.
- `data`: Response data (if no error).
  - `sign`: The signature signed by demo token.
- `reason`: Error reason (if has error).

## Response Examples

```json
{ "error": false, "data": { "sign": "c07b6de331d7365b008bb9da58934b84" } }
```

```json
{ "error": true, "reason": "param" }
```
