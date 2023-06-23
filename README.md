# True Tithe

Empowering Organizations to Accept Donations on the XRPL via HTML landing pages.
Using GemWallet API. Hooks & XUMM Wallet API is under review.

## Getting started with True Tithe Templates

1. Clone this repository:
```
git clone https://github.com/mworks-proj/True-Tithe.git
```

2. Serve the index.html in your browser
To serve th index.html in your browser follow these steps:

0. switch to desired template using `cd template-01`
1. install required modules via `npm install`
2. install any updates using `sudo npm install -g npm`
3. launch local dev enviornment `npm start`


## Usage

 Find GemWallet API in `<script>` section and add your orgs xrpl address

The script contains three buttons that trigger the following actions:
1. Pay XRP: Sends 20 XRP to the specified destination address.

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
2. Pay USD: Sends 20 USD to the specified issuer address.

```
    // The `handleUSDPayment` function is called when the "Pay USD" button is clicked.
      function handleUSDPayment(currency) {
        // Define the payment issuer.
        const issuer = "YOUR USD TESNET ADDRESS GOES HERE";
```
3. Add trustline: Adds a trustline for USD with the specified issuer.

```
    // The `handleTrustline` function is called when the "Add trustline" button is clicked.
      function handleTrustline() {
        // Check if GemWallet is connected (installed).
        GemWalletApi.isConnected()
        .then((isConnected) => {
          if (isConnected) {
          // Define the transaction details.
          const transaction = {
            currency: "USD",
            issuer: "YOUR XRPL TESTNET TOKEN TRUSTLINE ADDRESS",
            value: "10000000",
          };
          // Add the trustline using GemWallet.
    (!THIS IS YOUR XRPL TOKEN ADDRESS ISSUED BY YOUR ORGANIZATIONS)

```
- [HTML Starter (use GemWallet within your browser without any frontend framework)](/html-starter/)


