# True Tithe

Empowering Organizations to Accept Donations on the XRPL via HTML landing pages.
Using GemWallet API. Hooks & XUMM Wallet API is under review.

###### - [HTML Starter (use GemWallet within your browser without any frontend framework)](/html-starter/)

## Getting started with True Tithe Templates

1. Clone this repository:
```
git clone https://github.com/mworks-proj/True-Tithe.git
```

2. Serve the index.html in your browser.
To serve th index.html in your browser follow these steps:

0. Switch to desired template using `cd template-01`
1. Install required modules via `npm install`
2. Install any updates using `sudo npm install -g npm`
3. Launch local dev enviornment `npm start`


## Usage

 Find GemWallet API in `<script>` section and add your business/ orgs xrpl address to recieve $XRP $USD and trustline info. For more info on how to establish these address see 

 ### The script contains three buttons that trigger the following actions:

<details>
<summary>1. Pay XRP: Sends 20 XRP to the specified destination address.</summary>

```
    
    // The `handleXRPPayment` function is called when the "Pay XRP" button is clicked.
      function handleXRPPayment() {
        // Check if GemWallet is connected (installed).
        GemWalletApi.isConnected()
        .then((isConnected) => {
          if (isConnected) {
          // Define the payment details.
          const payment = {
            amount: "20",
            destination: "YOUR XRPL TESTNET ADDRESS GOES HERE",
          };
```
</details>

<details>
<summary>2. Pay USD: Sends 20 USD to the specified issuer address.</summary>


```
    [Obtain $USD Wallet Address](https://xrpl.services/tools).
    
    // The `handleUSDPayment` function is called when the "Pay USD" button is clicked.
      function handleUSDPayment(currency) {
        // Define the payment issuer.
        const issuer = "YOUR USD TESTNET ADDRESS GOES HERE";
```
</details>



<details>
<summary>
3. Add Trustline: Adds a Trustline for USD with the specified issuer. 
   </summary>
   
```
    [Setup USD Trustline](https://issue.cash/)
    
    q// The `handleTrustline` function is called when the "Add trustline" button is clicked.
      function handleTrustline() {
        // Check if GemWallet is connected (installed).
        GemWalletApi.isConnected()
        .then((isConnected) => {
          if (isConnected) {
          // Define the transaction details.
          const transaction = {
            currency: "USD",
            issuer: "YOUR $USD TESTNET ADDRESS / ADDRESS WHERE YOU WILL RECIEVE $USD",
            value: "10000000",
          };
          // Add the trustline using GemWallet.
    (!THIS IS YOUR XRPL TOKEN ADDRESS ISSUED BY YOUR ORGANIZATIONS)

```
</details>

