# System Infomation

Get basic information of payment gateway.

## Location

`/sysinfo`

## Method

`GET`

## Request Parameter

`No parameter for this API.`

## Request Examples

`GET /sysinfo`

## Response

Format: `json`

- `error`: Error indicator.
- `data`: Response data (if no error).
  - `version`: API version of the system.
- `reason`: Error reason (if has error).

## Response Examples

```json
{
  "error": "false",
  "data": {
    "version": "0.0.1"
  }
}
```
