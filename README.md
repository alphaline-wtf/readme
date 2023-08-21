# alphaline.wtf/alphacookies

[alphaline.wtf](https://alphaline.wtf/) is a bounty platform that quantifies and rewards user contributions to the Solana ecosystem using alphacookies+alphapoints.

alphacookies

- alphacookies are compressed NFTs (cNFTs) that listen to and record users' on-chain activity. Users must activate their alphacookie to start claiming completed bounties listed by protocols. The alphacookie metadata is updated as bounties are claimed, reflecting users' live contributions to the Solana ecosystem.

alphacookies enable the following:

- Data self-custody
- Streamlined data indexing and storage
- Composable and interpretable data showcase
- On-chain user profiling

alphacookies currently support protocols in four sectors:

- DeFi
- NFTFi
- NFT Marketplaces (MarketFi)
- Regenerative Finance (ReFi)

## Supported Protocols:

- `DeFi:`

  - `MarginFi, Solend, Hubble, Meteora, Drift, Mango, Jupiter, SolBlaze (bSOL), Marinade (mSOL), Jito (jitoSOL), Orca, Rayduim, Lulo.Finance, Mercurial, Aldrin, Saber, Kamino`

- `MarketFi:`

  - `Tensor, Magic Eden`

- `NFTFi:`

  - `SharkyFi, Citrus, Frakt, RainFi`

- `ReFi:`
  - `Sunrise Stake, Coral Tribe`

## Core Features

- Mint a compresssed cookie through sphere
- Customizable bounties (live/milestone) that encomapass four different sectors
- Earn alphapoints by completing bounties
- alphapoints marketplace: users can redeem their points for tangible rewards ($sol, nfts, raffle entries, early acess to protocols)
- alphapoints leaderboard
- [credit score explorer](https://www.alphaline.wtf/creditScore) for NFTfi protocols (SharkyFi, Citrus, Frakt, Aggreagte)
- Public APIs to query credit scores

## Architecture Overview

alphaline.wtf is comprised of three main components: *client, server, and database*

![image](https://www.alphaline.wtf/images/alphaline-logo1.png)

Server - Consists of approx 80 edge & serverless functions that verify bounties, return data from database, calculate credit scores, redeem points, cron job to check bounty status, webhook to listen to sphere payments, webhook that updates metadata of compressed cookies upon completion of a bounty, etc.

Tech Stack: Next.js, Typescript, Prisma, Vercel CRON
Data providers: Helius DAS, HelloMoon, SonarWatch

Client - The main frontend app that connects all the components together. It allows users search credit scores on our explorer, acivate a cookie, claim bounties, redeem bounties, check their completed bounties, and a leaderboard.

Tech Stack: React, Tailwind, CSS, GraphQL

Database - A PostgreSQL database that stores all relevant data and additional analytics on users interacting with our protocol. This includes the total volume directed (TVD), bounty/points relational data, & other metrics to measure user retention.

Tech Stack: Prisma, PostgreSQL, Supabase

## Open Source Credit Score APIs

- SharkyFi: https://www.alphaline.wtf/api/sharkyFi/creditScore/sharkyfiCreditScore?publicKey=48JdX3hT4SgrYRh4EgxJcek2qbKTsEoMWSa4nHGgYhQB
- Citrus: https://www.alphaline.wtf/api/citrus/citrusCreditScore?publicKey=9kYGFYZds6bEdG3brwBoS8CjiUB22CoTGYMEH254jH5z
- Aggreagted Scores: https://www.alphaline.wtf/api/aggregate/creditScore?publicKey=9kYGFYZds6bEdG3brwBoS8CjiUB22CoTGYMEH254jH5z

## Links

Site: https://alphaline.wtf/

Twitter: https://twitter.com/Alphaline_wtf
