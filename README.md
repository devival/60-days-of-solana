# 60-days-of-solana

My attempt at learning [Solana](https://solana.com/) [program (smart contract)](https://solana.com/docs/core/programs) development through [RareSkill's Solana course](https://www.rareskills.io/solana-tutorial).

> Originally, I was trying to create a single anchor project and add the daily exercises under `programs` (`programs/day_1`, `programs/day_2`, `programs/day_x`), but this made following along with the tutorial harder (longer running tests, Anchor not supporting deployment/testing of individual programs out of the box).

## Directory

- [Day 1: Hello World (and troubleshooting Solana installation)](day_01/README.md)
- [Day 2: Function arguments, math, and arithmetic overflow](day_02/README.md)
- [Day 3: Anchor function magic and the Interface Definition Language](day_03/README.md)
- [Day 4: Solana reverts, errors, and basic access control](day_04/README.md)
- [Day 5: Where is the constructor? About anchor deploy](day_05/README.md)
- [Day 6: Solidity Translations to Rust and Solana](day_06/README.md)
- [Day 7: The unusual syntax of Rust](day_07/README.md)
- [Day 8: Understanding function-like macros in Rust](day_08/README.md)
- [Day 9: Rust Structs and Attribute-like and Custom Derive Macros](day_09/README.md)
- [Day 10: Translating Solidity function visibility and contract inheritance to Solana](day_10/README.md)
- [Day 11: Block variables in Solana: block.timestamp and block.number and others](day_11/README.md)
- [Day 12: Beyond the block: Sysvars](day_12/README.md)
- [Day 13: Native Programs: Sysvars](day_13/README.md)
- [Day 14: tx.origin, msg.sender, and onlyOwner in Solana](day_14/README.md)
- [Day 15: Transaction fees and compute units](day_15/README.md)
- [Day 16: Accounts in Solana](day_16/README.md)
- [Day 17: Writing to storage](day_17/README.md)
- [Day 18: Reading Accounts from Typescript — an alternative to public variables and view functions](day_18/README.md)

## Setup

For the initial setup of dependencies required for Solana program development, follow the [day 1 tutorial](day_1/README.md).

Then for creating a new Anchor project:

1. Initialize a project: `anchor init day_x`
2. Go to folder: `cd day_x`
3. Remove git repository: `rm -rf .git` (since `60-days-of-solana` is the main git repository)
4. Follow the tutorial for each day

## Troubleshooting

Here is a list of common issues that I've encountered while going through the tutorials and how to resolve them.

- `Error: Deploying program failed: RPC response error -32002: Transaction simulation failed: Error processing Instruction 0: account data too small for instruction`

  - [StackOverflow](https://stackoverflow.com/questions/71267943/solana-deploy-account-data-too-small-for-instruction)

  To resolve this:

  1.  Delete `day_x/target/deploy`
  2.  Build Anchor program: `anchor build`
  3.  Sync keys: `anchor keys sync`
  4.  Redeploy or retest: `anchor deploy` or `anchor test`

## References

- [RareSkill's Solana course](https://www.rareskills.io/solana-tutorial)
- [Solana](https://solana.com/)
- [What are Solana Programs?](https://solana.com/docs/core/programs)
- [Anchor](https://www.anchor-lang.com/)
