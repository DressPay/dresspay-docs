# Payment Callback

Callback from DressPay API to notify the merchant the result of transaction.

## Location

`Your endpoint in the params of payment.`

## Method

`POST`

## Parameter

- `status`: The result of the transaction. (SUCCESS / FAILED)
- `price`: The total amount of price in the transaction. (Currently in USD only)
- `out_trade_no`: The identifier for the invoice of merchants.
- `uid`: The unique identifier of the transaction. Also the identifier of submitted photos. (Optional if the status is FAILED)
- `reason`: The reason why the transaction is failed. (Only if the status is FAILED)
- `sign`: The encrypted signature of previous data.