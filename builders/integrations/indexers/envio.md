---
title: Index Data with Envio & GraphQL
description: Learn how to use Envio HyperIndex to index Moonbeam and Moonriver smart contract events and query the data using a GraphQL API.
categories: Indexers and Queries
---

# Indexing Moonbeam with Envio

## Introduction {: #introduction }

[Envio](https://envio.dev/?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank} is the data layer for blockchain apps. It gives Moonbeam developers the fastest, most flexible way to get real-time and historical onchain data, from a single GraphQL API to raw high-speed access, with managed hosting on Envio Cloud. Envio's HyperIndex natively supports indexing any EVM chain out of the box, so you can index Moonbeam and Moonriver contract data through your own RPC endpoint and serve it to your application over GraphQL.

With HyperIndex you can auto-generate an indexer from any verified contract, write event handlers in TypeScript, JavaScript, or ReScript, and get reorg support, real-time and historical data, and multichain data aggregation across EVM and non-EVM networks. You can deploy your indexer to Envio Cloud with git-based deploys, monitoring, zero-downtime, and backups, or self-host.

--8<-- 'text/_disclaimers/third-party-content-intro.md'

## Create a Project {: #create-a-project }

To get started, generate a new indexer using the Envio CLI. Auto-generate an indexer from any verified contract with the following command and follow the prompts:

```bash
pnpx envio init
```

The initializer scaffolds a project that includes a configuration file, a GraphQL schema, and event handlers. For a full walkthrough, see the [HyperIndex quickstart](https://docs.envio.dev/docs/HyperIndex/quickstart?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank}.

## Configure the Network {: #configure-the-network }

Point your indexer at a Moonbeam network by setting the network id and an RPC endpoint in the configuration file, then list the contracts and events you want to index. Use the chain id for the network you are targeting:

=== "Moonbeam"

    |  Parameter   |                  Value                  |
    |:------------:|:---------------------------------------:|
    | `id`         |   `{{ networks.moonbeam.chain_id }}`    |

=== "Moonriver"

    |  Parameter   |                   Value                   |
    |:------------:|:-----------------------------------------:|
    | `id`         |   `{{ networks.moonriver.chain_id }}`     |

For details on configuring an RPC data source, see the [RPC sync guide](https://docs.envio.dev/docs/HyperIndex/rpc-sync?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank} and the [configuration file reference](https://docs.envio.dev/docs/HyperIndex/configuration-file?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank}.

## Query the Data {: #query-the-data }

Once your indexer is running, HyperIndex exposes the indexed data as a GraphQL API that you can query from your application. Write event handlers to shape the entities in your schema, then query those entities over GraphQL.

## Deploy {: #deploy }

You can run your indexer locally, self-host it, or deploy it to [Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank} for fully managed hosting with git-based deploys, monitoring, zero-downtime, and backups.

## Additional Resources {: #additional-resources }

- [Envio documentation](https://docs.envio.dev/?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank}
- [HyperIndex overview](https://docs.envio.dev/docs/HyperIndex/overview?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank}
- [HyperIndex quickstart](https://docs.envio.dev/docs/HyperIndex/quickstart?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank}
- [Supported networks](https://docs.envio.dev/docs/HyperIndex/supported-networks?utm_source=moonbeam&utm_medium=partner-docs){target=\_blank}

--8<-- 'text/_disclaimers/third-party-content.md'
