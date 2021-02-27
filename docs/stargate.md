# Microtick Stargate Features

The upcoming Stargate release brings the highly anticipated IBC capabilities to the Microtick chain, and some exciting new features as well.

## IBC Deposits and Withdrawals

With the new Stargate SDK release Microtick now supports token deposits and withdrawals from other chains that also support IBC. Multiple relayers
can relay packets between chains. Gone are the days where a trusted bridge was necessary to transfer backing tokens on- or off-chain.  In addition,
there is no KYC requirement for IBC transfers, or any limitation on the size of deposits or withdrawals.

In addition to backing token transfers over IBC, any Microtick account can now transfer TICK tokens off chain to trade on an Automated Market Maker
or DEX.

## New Governance Features

The chain adds two new governance proposals specific to the x/microtick module: **Backing Denomination** and **Add Markets**.

### Backing Denomination Proposal

IBC tokens have a naming mechanism based on the port / channel and their denomination on the originating chain. This results in token denominations
on the receiving chains that look like:

ibc/ED2456914E48C1E17B7BD922177291EF8B7F553EDF1B1F66B6FC1A076524B22F

This mechanism is described in more detail here: https://docs.cosmos.network/master/architecture/adr-001-coin-source-tracing.html

Once a channel has been set up between a source chain and Microtick, the Microtick governance community can switch to a new backing token denomination by 
proposing and passing a **Backing Denom** change proposal. Upon successful passage, the following changes take effect immediately:

- All existing quotes and trades using the previous denomination are closed and removed from the markets.
  - Quote backing is refunded to the quote provider
  - Trade backing is refunded to the short counterparty. No credit is given for an in-the-money consensus.
  - Premium paid is not refunded to the long counterparty (this was paid at trade initiation).
- The new backing denomination is stored in the parameter set and must be used for all quotes, trades and settlements after the backing change.

### Add Markets Proposal

The community can now dynamically add new markets without having to stop and restart the chain. With a successful vote, the new markets become available 
automatically for trading upon proposal passage. Each market must have a **name** and **description**. No structure or naming convention is enforced by the
governance mechanism itself; proposal curation is assumed to have been provided by the community through the proposal process.

## Option Bids



Quote weights are now computed backing / average premium, where average premium is bid + ask / 2

## Synthetic Long / Short Positions

## Dynamic Commissions

## Dynamic TICK Reward
