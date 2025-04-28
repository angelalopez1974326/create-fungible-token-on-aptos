# create-fungible-token-on-aptos

## Project Description

**create-fungible-token-on-aptos** is a Move smart contract template for creating, managing, and interacting with fungible tokens (FT) on the Aptos blockchain. It serves as a foundational project for developers looking to launch their own tokens with standard capabilities such as minting, burning, and transferring.

## Features

- 🪙 Deploy your own fungible token on Aptos
- 🔥 Mint, burn, and transfer token functionality
- 🛡️ Secure and compliant with Aptos token standards
- ⚡ Optimized for low-cost and high-speed transactions
- 🛠️ Easily customizable token parameters (name, symbol, decimals, supply)

## Installation

```bash
# Clone the repository
git clone https://github.com/angelalopez1974326/create-fungible-token-on-aptos.git
cd create-fungible-token-on-aptos

# Install dependencies (if applicable)
npm install
# or
yarn install
```

## Usage

### Deploy Smart Contracts

```bash
# Compile the Move package
aptos move compile --package-dir move/

# Publish the Move modules to the Aptos network
aptos move publish --package-dir move/ --profile default
```

### Initialize the Token

```bash
# Call the initialize function to create a token
aptos move run-entry-function \
  --function-id "create_fungible_token_on_aptos::token::initialize" \
  --args "TokenName" "TokenSymbol" "Decimals" "InitialSupply"
```

### Transfer Tokens

```bash
# Transfer tokens between accounts
aptos move run-entry-function \
  --function-id "create_fungible_token_on_aptos::token::transfer" \
  --args "0xRecipientAddress" "Amount"
```

## Configuration

- Update token metadata (name, symbol, decimals) in the initialization function.
- Configure deployment profiles in `aptos.yaml` for devnet, testnet, or mainnet deployment.

## Testing

```bash
# Run Move unit tests
aptos move test --package-dir move/
```

## Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature-name`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add your message here'`)
5. Push to the branch (`git push origin feature/your-feature-name`)
6. Create a pull request

Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## License

This project is licensed under the [Apache 2.0 License](LICENSE).

## Links

- [Aptos Documentation](https://aptos.dev/)
- [Move Language Documentation](https://move-language.github.io/move/)
- [Aptos GitHub](https://github.com/aptos-labs)
