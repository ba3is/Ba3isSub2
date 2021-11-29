# What is SubQuery?

SubQuery powers the next generation of Polkadot dApps by allowing developers to extract, transform and query blockchain data in real time using GraphQL. In addition to this, SubQuery provides production quality hosting infrastructure to run these projects in.

# SubQuery Example - Account balance

This subquery example indexes the deposit balance of each account and it is an example of an EventHandler. By processing substrate events with the use of the "balances/Deposit" mapping filter, we can obtain account and the DOT balance of the account.

# Getting Started

### 1. Clone the entire subql-example repository

```shell
git clone https://github.com/subquery/tutorials-account-balances.git

```

### 2. Install dependencies

```shell
cd tutorials-account-balance
yarn
```

### 3. Generate types

```shell
yarn codegen
```

### 4. Build the project

```shell
yarn build
```

### 5. Start Docker

```shell
docker-compose pull & docker-compose up
```

### 6. Run locally

Open http://localhost:3000/ on your browser

### 7. Example query to run

```shell
query {
   accounts(first:10 orderBy:BALANCE_DESC){
    nodes{
      account
      balance
    }
  }
}
```