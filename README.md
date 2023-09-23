# Fixed Finance

Fixed is a subscription enabled, zero cost trading product on Uniswap for stable swaps designed to increase capital efficiency and limit sandwich attacks. Using Uniswap Hooks, Unbound and Safe, Fixed allows traders to pay subscription to access 0 fee stable pools with no gas fees

## Detailed description
Fixed is a subscription trading product for stable pools to increase capital efficiency in DeFi. Fixed allows whales and frequent traders to reduce cost of trading, while providing a steady stream of income for LPs.  Fixed leverages Uniswap V4 hooks to subscription accessible Uniswap liquidity pools, Unbound Protocol to manage subscription sales and Safe Protocol to enable gasless trades for users.

Fixed Protocol also provides MEV protection to swappers by enabling only one transaction per block per address. As a result, an MEV bot will not be able to create a sandwich attack unless the bot controls multiple addresses.

Fixed Liquidity Pools are also usable by traders who do not own a subscription token in order to ensure effective markets and increased revenue stream to LPs. When a trader submits signed a transaction to the relayer, Uniswap V4 hook checks whether the user has a valid subscription NFT and determines the trading fee for the swap. In other words, if Alice holds an active subscription NFT she would pay 0 trading fees and if not, she would pay the fee associated with the trading pool.

Value proposition
Traders: Frequent traders that swap a large volume of tokens over a month, benefit from Fixed’s subscription model to cap their trading fees regardless of how much they trade. In addition to eliminating trade fees, Fixed traders benefit from gasless transactions that are enabled by Safe Account Abstraction. Given its free nature, Fixed will be able to attract a lot of traders and will be able to bundle transactions. In addition to lower cost of trading, traders using 

Liquidity providers: Fixed enables LPs to receive a fixed income stream in exchange for providing liquidity.

User experience:
Fixed is a decentralized browser application, which enables traders to buy a subscription (Unbound NFT) and access Fixed stable (Uniswap V4) liquidity pools to swap tokens with zero trading and transaction fee. Traders submit all signed transactions to a relayer (Safe Protocol) without paying any gas. Assuming that the user holds an active subscription token, Safe Protocol account abstraction relayer submits the transaction to the 0 fee stable swap pool. Traders can renew their subscriptions at the end of each month. If Alice doesn’t have a subscription token and wants to trade for free, the relayer first buys a subscription for Alice and enables a free trade.

Liquidity providers will be able to deposit to Fixed liquidity pools using the same browser application. No subscription token is required for the LPs. Subscription revenue is distributed to LPs similar to trading fees. LPs receive subscription revenue proportional to their share of liquidity at the given tick. 

Improvement areas:
Subscription revenue distribution: Our hackathon project distributes subscription revenue to LPs in the same block the subscription NFT is purchased. This creates a major limitation: LPs receive subscription revenue regardless of satisfactory service (providing liquidity) over the subscription period. Future work in this area would calculate subscription revenue per liquidity provider on a per block basis and allow LPs to claim their fees at a future time. This would prevent an adversary LP to collect subscription revenue without providing service.

Pricing optimization: Analyzing on-chain stable swap data, Fixed needs to implement an optimal pricing strategy that both creates value capture
