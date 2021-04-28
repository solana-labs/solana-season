# Solana Season Hackathon Project Ideas

Hackathon participants are free to explore and build projects that span a variety of use cases across NFTs, DeFi, and Web3.** The following is a list of interesting possible ideas sourced from the Solana community, Project Serum, and the participating judges/speakers. One of the beauties of utilizing DeFi’s composable building blocks is that they can be remixed and modified to build entirely new financial services. So take a look if you or your team is in need of some inspiration! 

* Serum Ideas: The Serum team has produced an exclusive Serum-related list that can be found here: https://serum-academy.com/en/serum-project-ideas/project-ideas/ 
* Lending front end and primitive: Money market lending protocol native to Solana (akin to Compound or Aave)
* Cross-Chain Lending: A lending protocol that immediately provides liquidity for assets transferred cross-chain, utilizing the Wormhole bridge - such that users don't need to wait for the cross-chain assets to be fully confirmed on both chains - in return for a fee
* Fixed-Rate Loans: Where users can take out a fixed-rate loan on an Ethereum Lending/Borrowing protocol that is enabled by an on-chain interest rate swap order book on Serum
* Censorship resistant Wallstreetbets
* Basis Trade Stablecoin
* Make use of Coingecko API in Solana dapps: https://www.coingecko.com/en/api
* Liquidation bot for undercollateralized positions
* Aggregator that combines key functions like Furucombo and DeFi Saver, but does it automatically. Like Borrow with insurance wrapped or Borrow with fixed rate or borrow and automatically fix your collateral ratio. These functions exist is a unbundled way but someone should bundle them to make it super easy for the user
* Reinsurance markets: An expansion yInsure
* On-chain subscriptions: A protocol that is a factory for any app to create on-chain payment streaming and subscriptions. Combine elements like NFTs to increase engagement and unlock features
* Analytics: perhaps the aggregator above can also roll in key on-chain KPIs that tell you if you’re going to swap token A then what % of buy vs. sell orders and sentiment in the past [24] hrs, whale movements, project developments etc.
- Education- a game-type protocol that walks a user thu the DeFi journey. Combining video clips, resources and yield-farming/NFT quest type journey to get normies up to speed
* DeFi asset manager: A single interface consolidating all DeFi assets and liabilities across different platforms (and different chains) into one.
* DEX Aggregator: A cross-chain DEX aggregator that allows users to choose the best price for execution across multiple DeFi platforms, including cross-chain platforms.
* Build-your-own Liquidity Mining platform: Utilize yield farming to jumpstart your product
* Synthetic Assets: Build out support for tokenized synthetic assets using Chainlink oracles and listing the SPL Synthetics on Serum
* Arbitrage bots: A bot that automatically moves funds from Serum CLOB when vol is low and moves it to AMM when vol is high
* Compute implied vol or black scholes from Serum market data for a volatility index/product
* On-chain NFT market with seamless USDC payment usage, connected to Wormhole for folks who need to get in and out of ERC20, but also native USDC. Ideally some app where there is content creation in a browser connected to IPFS and then loaded directly into NFT market. In turn, connect the NFT market into Serum DEX markets -- e.g. markets on Serum get created automatically, and demonstrate order books on a free floating NFT.
* Prediction market minter with Chainlink Oracle integration
* Oracles: An on-chain oracle that takes prices from Serum markets, does sophisticated risk and sanity checks on them, and creates a clean price feed that other projects working on Serum can use. Furthermore, once there are on-chain cross-chain bridges, those can be combined with this to create a fully on-chain cross-chain pricing oracle.
* Fee Compare: A simple interface that tracks and compares cost to execute something given certain parameters across various DeFi platforms. Parameters include desired spread, transaction fees, trading pair set. Can also track total value saved in transaction fees/spread
* Creating Custom Markets on Serum: An interface to create custom markets on Serum from Ethereum. Including the set-up of decentralized market makers.
* Slashing Insurance: A simple insurance protocol where the community can provide insurance for validators against the risk of being slashed
* Smart Contract Insurance: Something akin to Nexus Mutual
* DeFi visualization dashboards: Plugging into and displaying data from Serum, Orca, Structured Product, Oxygen
* Security audits of existing Serum/Solana infrastructure
* Serum DeFi app store: dashboard of all Serum dAPPs
* Extend the wormhole bridge to allow assets locked on Ethereum to earn interests through lending protocols such as Aave or Compound
* Build a simple oracle that allows Solana Dapps to connect to an off-chain API or Websocket (e.g. a price feed)
* Demonstrate how staking should work for any SPL Token




# Swap, Borrow/lend, and Margin Implementation Ideas

Ideas to extend existing source-code (token-swap, token-lending)

* Add support for new token-swap curve that’s using Chainlink as oracle
* Add support for cross-asset collateral to token-lending.
* Single collateral token for all deposits can be used across loans
* Add support for adding/removing collateral from token-lending obligation (top-up collateral)
* Add support for liquidations using ordered heap: Liquidator will be only to liquidate positions with lowest health score first
* Add support for token-swap LP as collateral to token-lending. Use-case: single token exposure in AMM
* Add support to token-lending for stable borrowing rates
* Margin trading using token-lending: User can initiate (short/long) margin trade with predefined max leverage 
* Token lending stores position in escrow
* Solana integration for https://xchainjs.org/ (a little boring tho ha), but a PoC for a web-wallet that can do Stateful solana transactions
* Solana Bifrost Spec & PoC (observing solana transactions into a CosmosSDK state machine)
* economic model for zero-slippage synthetic asset swaps on THORChain
* PoC for a lightweight, smart-contract (or other) leaderless SeedService that has consensus on the correct Node IP list
* economic model for a safe debt-based stablecoin using LP tokens on THORChain (ie, live state machine that can re-balance every 5 seconds)
* Relayer (mobile and/or desktop) for traders on Solana to trade on dYdX. Can be achieved by having the app act as the market maker between dydx and the trader.
* Simplified UI for obtaining leverage on dydx perpetuals (for more inexperienced users)

# Solana Data Viz Idea
A web-based tool through which any user can query all data on the Solana blockchain by using SQL queries. Pre-populated databases with parsed data from Solana blocks. This can all be built on Redash just like Dune (https://redash.io/)


* Any user would be able to write a query
  * free users would have to open source their queries so others could work
  * paid users would have the ability to write queries privately

* Automatic hourly updates on the most viewed queries and charts
  * Paid users could hook an API to any publicly available query and get results

* Dashboarding functionality
  * Curated queries shared in a visualized form
  * The team would write several popularly requested queries to launch this product to expedite the kick-off
  * Charts that should be launched with
    * Number of daily transactions on Solana
    * Number of daily active Solana addresses 
    * Number of new daily Solana addresses
    * Daily volume of SOL transfers
    * Daily fees of all SOL/SPL transfers
    * Daily median USD cost of SOL&SPL transfer
    * Daily USD revenue of Solana stakers
    * Daily Solana addresses with balance over $X ($1k, $10k, $100k, $1M, $10M
    * Total monthly DEX trading volume on Solana (with DEX splits - Serum&Raydium etc.)
    * Number of monthly unique liquidity providers on Serum
    * Number of monthly unique trading addresses on Serum
    * Number of monthly trades on Serum
    * Total number of unique addresses interacting with Solana DeFi apps with splits by each project
    * Total stacked daily TVL of all Solana DeFi projects
    * Daily outstanding debt of Jet Protocol
    * Total daily supply of stablecoins issued on Solana

---------- 
** The Solana Season Hackathon is a competition where projects will be evaluated by judges on their technological merits without consideration of legal viability. Participants in the Hackathon will create software solely for purposes of evaluation by judges as part of a competition and not for commercial deployment or release as part of the Hackathon.All participants must comply with applicable laws and regulations when releasing any software that they develop as part of the Hackathon.

The Hackathon ideas and developer resources that Solana provides are for educational and inspirational purposes only. The Solana Foundation (“SF”) does not encourage, induce or sanction the deployment of any such applications in violation of applicable laws or regulations. SF does not encourage, induce or sanction the deployment, integration or use of any such applications (including the code comprising the Solana blockchain protocol) in violation of applicable laws or regulations and hereby prohibits any such deployment, integration or use. This includes use of any such applications by the reader (a) in violation of export control or sanctions laws of the United States or any other applicable jurisdiction, (b) if the reader is located in or ordinarily resident in a country or territory subject to comprehensive sanctions administered by the U.S. Office of Foreign Assets Control (OFAC), (c) if the reader is or is working on behalf of a Specially Designated National (SDN) or a person subject to similar blocking or denied party prohibitions, or (d) in violation of the Commodities and Exchange Act.
The reader should be aware that U.S. export control and sanctions laws prohibit U.S. persons (and other persons that are subject to such laws) from transacting with persons in certain countries and territories or that are on the SDN list. As a project based primarily on open-source software, it is possible that such sanctioned persons may nevertheless bypass prohibitions, obtain the code comprising the Solana blockchain protocol (or other project code or applications) and deploy, integrate, or otherwise use it. Accordingly, there is a risk to individuals that other persons using the Solana blockchain protocol may be sanctioned persons and that transactions with such persons would be a violation of U.S. export controls and sanctions law. This risk applies to individuals, organizations, and other ecosystem participants that deploy, integrate, or use the Solana blockchain protocol code directly (e.g., as a node operator), and individuals that transact on the Solana blockchain through light clients, third party interfaces, and/or wallet software.
