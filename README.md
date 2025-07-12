# IndieFi - Tokenized Micro-Economies for Indie Developers

IndieFi is a comprehensive platform that enables indie developers to easily create, launch, and manage tokenized micro-economies for their apps without needing deep blockchain or finance knowledge.

## 🚀 Features

### Core Features
- **Token Creation Module**: Create custom ERC-20 tokens with adjustable parameters
- **Fundraising Dashboard**: Enable crypto-based crowdfunding with real-time stats
- **Token Utility Integrations**: Add staking, reward distribution, and token gating
- **Governance & Treasury Management**: Enable token holders to vote on development priorities
- **Gas Optimization Layer**: Optimized contracts to minimize gas usage
- **Developer SDK**: React-based plug-and-play widget system

### Tech Stack
- **Frontend**: Next.js 14, TypeScript, TailwindCSS, ShadCN/UI
- **Smart Contracts**: Solidity, Hardhat, OpenZeppelin
- **Backend**: Node.js, Express.js, Socket.io
- **Blockchain**: Polygon, Ethereum testnets
- **Wallet Integration**: RainbowKit, wagmi

## 📦 Installation

### Prerequisites
- Node.js 18+ 
- npm or yarn
- Git

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/your-username/indiefi.git
cd indiefi
```

2. **Install dependencies**
```bash
npm run install:all
```

3. **Set up environment variables**
```bash
cp .env.example .env.local
```

4. **Deploy smart contracts**
```bash
cd contracts
npm run compile
npm run deploy:testnet
```

5. **Start the development servers**
```bash
# Terminal 1: Frontend
npm run dev

# Terminal 2: Backend
npm run backend:dev
```

## 🏗️ Project Structure

```
indiefi/
├── app/                    # Next.js app directory
│   ├── globals.css        # Global styles
│   ├── layout.tsx         # Root layout
│   ├── page.tsx           # Home page
│   └── providers.tsx      # Web3 providers
├── components/            # React components
│   ├── ui/               # ShadCN UI components
│   ├── Hero.tsx          # Landing hero section
│   ├── Features.tsx      # Features showcase
│   ├── TokenCreation.tsx # Token creation flow
│   ├── Dashboard.tsx     # User dashboard
│   └── Footer.tsx        # Footer component
├── contracts/            # Smart contracts
│   ├── contracts/        # Solidity contracts
│   │   ├── IndieFiToken.sol
│   │   └── IndieFiFactory.sol
│   ├── scripts/          # Deployment scripts
│   └── hardhat.config.js # Hardhat configuration
├── backend/              # Express.js API
│   ├── index.js          # Main server file
│   └── package.json      # Backend dependencies
├── lib/                  # Utility functions
├── hooks/                # Custom React hooks
└── package.json          # Root package.json
```

## 🔧 Configuration

### Environment Variables

Create a `.env.local` file in the root directory:

```env
# Blockchain Networks
NEXT_PUBLIC_POLYGON_RPC_URL=https://polygon-rpc.com
NEXT_PUBLIC_MUMBAI_RPC_URL=https://rpc-mumbai.maticvigil.com
NEXT_PUBLIC_SEPOLIA_RPC_URL=https://rpc.sepolia.org

# Contract Addresses (after deployment)
NEXT_PUBLIC_FACTORY_ADDRESS=0x...
NEXT_PUBLIC_TOKEN_ADDRESS=0x...

# API Keys
NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=your-project-id
POLYGONSCAN_API_KEY=your-polygonscan-api-key
ETHERSCAN_API_KEY=your-etherscan-api-key

# Backend
BACKEND_PORT=3001
FRONTEND_URL=http://localhost:3000
```

### Smart Contract Deployment

1. **Compile contracts**
```bash
cd contracts
npm run compile
```

2. **Deploy to testnet**
```bash
npm run deploy:testnet
```

3. **Update contract addresses**
Update the contract addresses in your `.env.local` file with the deployed addresses.

## 🚀 Usage

### Creating a Token

1. Connect your wallet using RainbowKit
2. Navigate to the token creation flow
3. Fill in token details (name, symbol, supply, price)
4. Review and deploy your token
5. Monitor your token through the dashboard

### Token Management

- **Dashboard**: View all your deployed tokens
- **Analytics**: Track performance and user engagement
- **Governance**: Create and vote on proposals
- **Staking**: Stake tokens to earn rewards

### Developer SDK

Integrate IndieFi features into your own apps:

```jsx
import { IndieFiWidget } from '@indiefi/sdk'

function MyApp() {
  return (
    <IndieFiWidget 
      tokenAddress="0x..."
      features={['staking', 'governance']}
    />
  )
}
```

## 🧪 Testing

### Smart Contracts
```bash
cd contracts
npm run test
```

### Frontend
```bash
npm run lint
npm run build
```

### Backend
```bash
cd backend
npm test
```

## 📚 API Documentation

### Endpoints

- `GET /api/health` - Health check
- `GET /api/tokens` - Get all tokens
- `GET /api/tokens/:address` - Get token by address
- `POST /api/tokens` - Create new token
- `GET /api/tokens/:address/stats` - Get token statistics
- `GET /api/users/:address/tokens` - Get user's tokens
- `GET /api/analytics/overview` - Get platform analytics
- `POST /api/gas/estimate` - Estimate gas costs

## 🔒 Security

- Smart contracts are built with OpenZeppelin libraries
- Gas optimization to minimize costs
- Input validation and error handling
- Secure wallet integration

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- **Documentation**: [docs.indiefi.com](https://docs.indiefi.com)
- **Discord**: [discord.gg/indiefi](https://discord.gg/indiefi)
- **Email**: support@indiefi.com
- **GitHub Issues**: [github.com/indiefi/issues](https://github.com/indiefi/issues)

## 🙏 Acknowledgments

- OpenZeppelin for secure smart contract libraries
- RainbowKit for wallet integration
- ShadCN for beautiful UI components
- Polygon for low-cost transactions

---

Built with ❤️ for the indie developer community 