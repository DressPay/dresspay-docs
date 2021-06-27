# Gateway Redirection

Redirect POST request to frontend with parameters.

## Location

`/gateway`

## Method

`POST`

## Request Parameters

Format: `form-data`

- `subject`: The subject of current transaction.
- `notify_url`: A URL to be called back when the given transaction is finished.
- `price`: The total amount of price in the transaction. (Currently in USD only)
- `return_url`: A URL to be redirected when the given transaction is finished.
- `clientid`: The unique ID for merchants to identify themselves.
- `out_trade_no`: The identifier for the invoice of merchants.
- `sign`: The encrypted signature of previous data.

## Request Examples

`POST /gateway`

- `subject`: `Example Payment`
- `notify_url`: `https://api.dresspay.org/demo/notify`
- `return_url`: `https://dresspay.org/demo?notify=yes`
- `price`: `114514`
- `clientid`: `0`
- `out_trade_no`: `f782d822-9b51-44ad-afe4-172a4e26e463`
- `sign`: `[Generated with token]`

## Response

Format: `Page Redirection`

- `301 redirect`: Redirect to the page of payment frontend.
- `500 error`: Redirect to the page of error frontend and display the reason.
