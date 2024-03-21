# Wallet API
### Description of the API
The 3040Crypto Wallet API is a way to change how users interact with cryptocurrencies in their daily transactions. The purpose of this API is to help users pay for their cryptocurrency with their 3040Crypto card. With this API, our users will be able to make fast and instant payments using their cryptocurrency in a similar way to a debit card. The API will get requests from the company our customer is buying their needs from and will return success or failure of the request to both the company and the customer. This API is capable of significantly improving the speed and reliability of cryptocurrency transactions, addressing widespread concerns among users about the efficiency of using digital currencies in a retail environment.  

At the same time, our API acts as a bridge between the digital currency world and traditional commerce, enabling instant conversion and processing of cryptocurrency transactions. The ultimate goal is to provide a user-friendly, secure and efficient trading experience.

### Endpoints and parameters
[https://3040CryptoWallet.org/wallet?Customer_ID=1234567&Amount=30&PIN=0000](https://3040CryptoWallet.org/wallet?Customer_ID=1234567&Amount=30&PIN=0000)

* Customer_ID(int): Customer's ID. Required.
* Amount(float): Amount needed to be paid in bitcoins. Required.
* PIN(int): Security pin the user enters for the validity of the transaction. Required.

### Resources
```json
{
    "Transaction_Info":[
        {
            "Amount": "30",
            "Success": "Transaction Failed",
            "Reference": "R2C415461FG2"
        }
    ]
}
```

* Amount(float): Amount paid to the company in bitcoins.
* Success(string): Success of the transaction.
* Reference(string): reference to the transaction if successful.

### Sample request and sample response
#### Request:
```json
{
    "Customer_Info":[
        {
            "Customer_ID": "1234567",
            "Amount": "30",
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
            "Amount": "30",
            "Success": "Transaction Failed",
            "Reference": "R2C415461FG2"
        }
    ]
}
```
