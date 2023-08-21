# alphaline.wtf/alphacookies

[alphaline.wtf](https://alphaline.wtf/) is a bounty platform that quantifies and rewards user contributions to the Solana ecosystem through alphacookies and alphapoints.

## alphacookies

Alphacookies are Compressed NFTs (cNFTs) designed to monitor and record users' on-chain activity. To claim completed bounties listed by protocols, users must activate their alphacookie. The alphacookie metadata updates as bounties are claimed, reflecting users' real-time contributions to the Solana ecosystem.

### Features of alphacookies:

- Data self-custody
- Efficient data indexing and storage
- Composable and interpretable data showcase
- On-chain user profiling

Alphacookies currently support protocols in the following sectors:

- DeFi
- NFTFi
- NFT Marketplaces (MarketFi)
- Regenerative Finance (ReFi)

## Supported Protocols

### DeFi:

- MarginFi, Solend, Hubble, Meteora, Drift, Mango, Jupiter, SolBlaze, Marinade, Jito, Orca, Rayduim, Lulo.Finance, Mercurial, Aldrin, Saber, Kamino

### MarketFi:

- Tensor, Magic Eden, Exchange.art

### NFTFi:

- SharkyFi, Citrus, Frakt, RainFi

### ReFi:

- Sunrise Stake, Coral Tribe

## Core Features

- Mint a compressed cookie via sphere
- Customizable bounties (live/milestone) across four sectors
- Earn alphapoints by completing bounties
- Alphapoints marketplace: Redeem points for rewards ($SOL, NFTs, raffle entries, early access to protocols)
- Alphapoints leaderboard
- [Credit score explorer](https://www.alphaline.wtf/creditScore) for NFTFi protocols (SharkyFi, Citrus, Frakt, Aggregate)
- Public APIs to query credit scores

## Architecture Overview

**alphaline.wtf** consists of three main components: _client, server, and database_.

![Architecture Image](https://www.alphaline.wtf/images/alphaline-logo1.png)

### Server:

- Contains ~80 edge & serverless functions
  - Verify bounties
  - Retrieve data from database
  - Calculate credit scores
  - Redeem points, and more.
- **Tech Stack:** Next.js, Typescript, Prisma, Vercel CRON
- **Data Providers:** Helius DAS, HelloMoon, SonarWatch

### Client:

- Frontend app connecting all components
- Features:
  - Search credit scores
  - Activate cookies
  - Claim & redeem bounties
  - View completed bounties
  - Access leaderboard
- **Tech Stack:** React, Tailwind, CSS, GraphQL

### Database:

- PostgreSQL database
  - Contains all relevant data
  - User analytics
  - Total Volume Directed (TVD)
  - Bounty/points relational data, etc.
- **Tech Stack:** Prisma, PostgreSQL, Supabase

## Open Source Credit Score APIs

- [SharkyFi API](https://www.alphaline.wtf/api/sharkyFi/creditScore/sharkyfiCreditScore?publicKey=48JdX3hT4SgrYRh4EgxJcek2qbKTsEoMWSa4nHGgYhQB)
- [Citrus API](https://www.alphaline.wtf/api/citrus/citrusCreditScore?publicKey=9kYGFYZds6bEdG3brwBoS8CjiUB22CoTGYMEH254jH5z)
- [Aggregate Scores API](https://www.alphaline.wtf/api/aggregate/creditScore?publicKey=9kYGFYZds6bEdG3brwBoS8CjiUB22CoTGYMEH254jH5z)

## Links

- [Site](https://alphaline.wtf/)
- [Twitter](https://twitter.com/Alphaline_wtf)
- 
