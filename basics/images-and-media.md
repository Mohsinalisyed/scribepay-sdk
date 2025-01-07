---
icon: image-landscape
---

# APIs

### `GET Transactions:`

`` `https://api.scribepay.org/api/transaction?buyerWallet=0xd00faF7c2a837DC457389758Ea1271aE6256dc44&token=0x0000000000000000000000000000000000000000&chain=1&txStatus= ``SUCCESS`&tx=`0xacca8dc156d36db1d7642cc380d36117aaec2e073d1051e7718b2ea2ddea3e00\&expectedDelivery=1735490149\`

{% tabs %}
{% tab title="Query Parameters" %}


| Parameter        | Description                                                                                                                                                                                  |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| buyerWallet      | `Optional`Wallet `address`of the consumer with which the item has been purchased                                                                                                             |
| token            | `Optional`Token `address of currency by which transaction took place`                                                                                                                        |
| chain            | `Optional`Chain `id`of the network where transaction has happened                                                                                                                            |
| txStatus         | <p><code>Optional</code>Current status of the transaction<br><code>Note:</code>It's possible status not update if the transaction hasn't been synced by the merchant from business panel</p> |
| tx               | `Optional`Hash of the transaction                                                                                                                                                            |
| expectedDelivery | `Optional`Delivery time provided by business                                                                                                                                                 |
{% endtab %}

{% tab title="Header" %}
| Parameter | Description                                                                           |
| --------- | ------------------------------------------------------------------------------------- |
| x-api-key | `Required API key can be obtained from business panel, each business have their own.` |


{% endtab %}

{% tab title="Response" %}
Sample Response

```json
{
    "status": "success",
    "data": {
        "docs": [
            {
                "_id": "67717a00bef5718c7ab46845",
                "txStatus": "SUCCESS",
                "productIndex": 0,
                "tx": "0xacca8dc156d36db1d7642cc380d36117aaec2e073d1051e7718b2ea2ddea3e00",
                "buyerWallet": "0xd00faf7c2a837dc457389758ea1271ae6256dc44",
                "expectedDelivery": 1735490149,
                "amount": 0.01,
                "token": "0x0000000000000000000000000000000000000000",
                "chain": 80002,
                "createdAt": "2024-12-29T16:34:09.023Z",
                "updatedAt": "2024-12-29T16:46:06.351Z",
                "id": "67717a00bef5718c7ab46845"
            }
        ],
        "totalDocs": 2,
        "limit": 10,
        "totalPages": 1,
        "page": 1,
        "pagingCounter": 1,
        "hasPrevPage": false,
        "hasNextPage": false,
        "prevPage": null,
        "nextPage": null
    }
}
```
{% endtab %}
{% endtabs %}

