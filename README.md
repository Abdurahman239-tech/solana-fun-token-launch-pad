# Solana Token LaunchPad

A comprehensive Next.js-based token launchpad platform for creating and managing SPL tokens on the Solana blockchain. This application provides an intuitive interface for token creation, liquidity management, market creation, and token authority management.

## Features

### Core Functionality
- **Token Creation**: Create custom SPL tokens with metadata, logos, and custom parameters
- **Liquidity Management**: Add and manage liquidity pools for your tokens
- **Market Creation**: Create trading markets for your tokens
- **Token Management**: 
  - View your created tokens
  - Revoke freeze authority
  - Revoke mint authority
  - Burn LP tokens
- **Token Discovery**: Browse and discover hot tokens and trending projects
- **Wallet Integration**: Seamless Solana wallet connection using Wallet Adapter

### User Interface
- Modern, responsive design with Tailwind CSS
- Interactive landing page with token discovery
- FAQ section for user guidance
- Beautiful UI components with custom styling

## 🛠️ Tech Stack

### Frontend
- **Next.js 14**: React framework with App Router
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first CSS framework
- **React 18**: Latest React features

### Blockchain Integration
- **@solana/web3.js**: Solana blockchain interaction
- **@solana/wallet-adapter-react**: Wallet connection management
- **@solana/wallet-adapter-react-ui**: Pre-built wallet UI components
- **@solana/wallet-adapter-wallets**: Multiple wallet support
- **@solana/spl-token**: SPL token operations

### Additional Libraries
- **@metaplex-foundation/js**: Metaplex protocol integration for token metadata
- **@metaplex-foundation/mpl-token-metadata**: Token metadata program
- **@raydium-io/raydium-sdk**: Raydium DEX integration for liquidity pools
- **@project-serum/anchor**: Solana program framework
- **zustand**: State management
- **react-query**: Data fetching and caching

## Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v18 or higher)
- **npm**, **yarn**, **pnpm**, or **bun** package manager
- A Solana wallet (Phantom, Solflare, etc.)

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Solana_Token_LaunchPad
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   ```

3. **Set up environment variables**
   
   Create a `.env.local` file in the root directory:
   ```env
   NEXT_PUBLIC_SOLANA_RPC=your_solana_rpc_endpoint
   ```
   
   You can use:
   - Public RPC: `https://api.mainnet-beta.solana.com` (for mainnet)
   - Or get a custom RPC endpoint from providers like Helius, QuickNode, or Alchemy

4. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   # or
   bun dev
   ```

5. **Open your browser**
   
   Navigate to [http://localhost:3000](http://localhost:3000) to see the application.

##  Project Structure

```
Solana_Token_LaunchPad/
├── public/                 # Static assets (images, icons, etc.)
├── src/
│   ├── app/               # Next.js App Router pages
│   │   ├── create-token/ # Token creation page
│   │   ├── add-lp/       # Add liquidity page
│   │   ├── burn-lp/       # Burn LP tokens page
│   │   ├── create-market/# Market creation page
│   │   ├── my-token/     # My tokens page
│   │   ├── revoke-freeze/# Revoke freeze authority
│   │   ├── revoke-mint/  # Revoke mint authority
│   │   └── faq/          # FAQ page
│   ├── components/        # React components
│   │   ├── Banner/       # Landing banner component
│   │   ├── DiscoverTokens/# Token discovery component
│   │   ├── HotTokens/    # Hot tokens display
│   │   ├── Header/       # Header component
│   │   ├── Footer/       # Footer component
│   │   └── MyToken/      # Token management component
│   ├── contexts/         # React contexts
│   │   ├── SolanaWalletProvider.tsx
│   │   ├── createSPLToken.tsx
│   │   ├── createLiquidity.tsx
│   │   ├── createMarket.tsx
│   │   └── ...
│   ├── utils/            # Utility functions
│   └── config.ts         # Configuration file
├── next.config.js        # Next.js configuration
├── tailwind.config.ts    # Tailwind CSS configuration
└── package.json          # Dependencies and scripts
```

## Usage

### Creating a Token

1. Navigate to the **Create Token** page
2. Connect your Solana wallet
3. Fill in the token details:
   - Token Name
   - Token Symbol
   - Token Logo (upload image)
   - Decimals (default: 9)
   - Initial Supply
4. Click **Create Token** and approve the transaction

### Adding Liquidity

1. Go to the **Add LP** page
2. Select your token
3. Specify the amount of tokens and SOL to add
4. Confirm the transaction

### Managing Token Authorities

- **Revoke Freeze Authority**: Remove the ability to freeze token accounts
- **Revoke Mint Authority**: Remove the ability to mint additional tokens
- Both operations are irreversible, so use with caution

##  Security Considerations

- **Never share your private keys** or seed phrases
- Always verify transaction details before signing
- Use a hardware wallet for large transactions
- Test on devnet before deploying to mainnet
- Review smart contract interactions carefully

##  Network Support

The application supports:
- **Solana Mainnet**: Production environment
- **Solana Devnet**: Testing environment (configure RPC accordingly)

##  Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

##  Deployment

### Deploy on Vercel

The easiest way to deploy this Next.js app is using [Vercel](https://vercel.com):

1. Push your code to GitHub
2. Import your repository on Vercel
3. Add environment variables in Vercel dashboard
4. Deploy!

### Other Platforms

You can also deploy to:
- **Netlify**: Configure Next.js build settings
- **AWS Amplify**: Use Next.js hosting
- **Self-hosted**: Use Node.js server with `npm run start`

## Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Solana Web3.js Documentation](https://solana-labs.github.io/solana-web3.js/)
- [Metaplex Documentation](https://docs.metaplex.com/)
- [Raydium SDK Documentation](https://raydium.gitbook.io/raydium/)

##  Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

##  License

This project is private and proprietary.

##  Contact & Support

For questions, support, or inquiries, please contact:

**Telegram**: [@BlackSky_jose](https://t.me/BlackSky_jose)

---

**Note**: This is a beta version of the Mirage Launchpad. Use at your own risk and always verify transactions before signing.
