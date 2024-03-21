# Wallet API
### Description of the API
The purpose of this API is to help the user pay with their crypto currency using their 3040Crypto card. Our biggest draw back is the speed at which our company successfully completes the requests of our users. With this API, our users will be able to pay using their crypto in a similar way the debit card does. This API will get a request from the company our customer is at buying their needs and will return with the success or failure of the request to the company and the customer.

### Endpoints and parameters
[https://3040CryptoWallet.org/wallet?Customer_ID=1234567&Amount=100.05&ID=1234567](https://3040CryptoWallet.org/wallet?Customer_ID=1234567&Amount=100.05&ID=1234567)

* Customer_ID(int): Customer's ID. Required.
* Amount(float): Amount needed to be paid. Required.
* PIN(int): Security pin the user enters for the validity of the transaction. Required.

### Resources
```json
{
    "Transaction_Info":[
        {
            "Amount": "100.05",
            "Success": "Transaction Failed",
            "Reference": "R2C415461FG2"
        }
    ]
}
```

* Amount(float): Amount paid to the company.
* Success(string): Success of the transaction.
* Reference(string): reference to the transaction if successful.

### Sample request and sample response
#### Request:
```json
{
    "Customer_Info":[
        {
            "Customer_ID": "1234567",
            "Amount": "100.05",
            "PIN": "0000"
        }
    ]
}
```
#### Response:
```json
{
    "Transaction_Info":[
        {
            "Amount": "100.05",
            "Success": "Transaction Failed",
            "Reference": "R2C415461FG2"
        }
    ]
}
```
