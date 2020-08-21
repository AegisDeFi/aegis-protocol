# Aegis-Protocol

Aegis is an Ethereum smart contract that provides supply and borrow. After eth or ERC-20 token is supplied and be used as collateral，users can borrow ERC-20 token from in Aegis contract. Aegis contract calculates borrow rate and supply rate according to block number, and adjusts dynamically according to the market utilization rate.

Suppose: one block is generated in 15s, 5760 blocks a day and 2102400 blocks a year.

Aegis is a scalable Liquidity Bridge between fiat and DeFi Ecology. 

Current DeFi platforms such as Compound offers lending and borrowing services underpinned by the over-collateralization of crypto assets. However, one downside of this methodology is that capital extraction is inefficient, and users are unable to unlock the full value of their digital asset portfolio. Aegis is a scalable DeFi platform that solves this problem by giving users access to lending and unsecured borrowing services, based on their credit scores. An "Aegis Score" is then assigned to the individual users, which allows users to unlock corresponding capital loans in the crypto ecosystem. Aegis therefore plays the critical role of a capital bridge that gives users the ability to leverage and move liquidity seamlessly between fiat and crypto ecosystems.

Please read:
  - [Aegis Whitepaper](https://aegis.finance/whitepage/AegisNetworkLitepaperEN.pdf)
  - our official website: https://aegis.finance, feel free to email us [official@aegis.finance](mailto:official@aegis.finance)
 
## Contracts
 
The core of Aegis contract
 
### AToken Contract

Erc-20 token contract

The following operations are allowed: `supply/collateral/borrow/repay/withdraw`

After supply, users will get atoken as proof of supply. With the change of exchange rate, the extra atoken in withdraw as the profit of supply. It can also be used as collateral, and then borrow.
 
### Aegis Protocol Contract

Allow Ethereum account do operation

### Price Oracle

Multiple Oracle machines are used to enhance the reliability to ensure the accuracy of the results and ensure the correct triggering of smart contracts.

### ApyModel Init Contract

Initial interest rate model of token.

Each token initializes its base rate and multiplier rate in its constructor
  - borrowRate: current borrow APY
  - supplyRate: current supply APY

### library

Some library contracts in contract can be regarded as implicit

#### Math

Mature and secure computing library

#### Safe

Authority verification.

For security, sensitive operations will be verified, whether operation is allowed or not, risk parameter control, etc.

#### Error/Exception

Capture error messages and exceptions
