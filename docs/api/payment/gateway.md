# Gateway Redirection

Redirect POST request to frontend with parameters.

## Location

`/gateway`

## Method

`POST`

## Parameter

- `subject`: The subject of current transaction.
- `notify_url`: A URL to be called back when the given transaction is finished.
- `price`: The total amount of price in the transaction. (Currently in USD only)
- `return_url`: A URL to be redirected when the given transaction is finished.
- `clientid`: The unique ID for merchants to identify themselves.
- `out_trade_no`: The identifier for the invoice of merchants.
- `sign`: The encrypted signature of previous data.

## Response

- `301 redirect`: Redirect to the page of payment frontend.
- `500 error`: Redirect to the page of error frontend and display the reason.
