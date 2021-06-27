# Payment Callback

Callback from DressPay API to notify the merchant the result of transaction.

## Location

`Your endpoint in the params of payment.`

## Method

`POST`

## Request Parameters

Format: `form-data`

- `status`: The result of the transaction. (SUCCESS / FAILED)
- `price`: The total amount of price in the transaction. (Currently in USD only)
- `out_trade_no`: The identifier for the invoice of merchants.
- `uid`: The unique identifier of the transaction. Also the identifier of submitted photos. (Optional if the status is FAILED)
- `reason`: The reason why the transaction is failed. (Only if the status is FAILED)
- `sign`: The encrypted signature of previous data.

## Request Examples

`POST [Your Endpoint of Notification]`

- `status`: `SUCCESS`
- `price`: `114514`
- `uid`: `9fd0ba77-15eb-4d31-9252-0e427f51a58f`
- `out_trade_no`: `f782d822-9b51-44ad-afe4-172a4e26e463`
- `sign`: `[Generated with token]`
