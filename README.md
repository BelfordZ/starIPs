# \*IPs - Star Improvement Proposals
*by Zachary Belford, Shane Jonas, Donald McIntyre, Yaz Khoury, Anthony Lusardi, Tomaz Kariz*

Star Improvement Proposals is an extension of the BIP/EIP/ECIP process, with some changes to allow for decentralization of the process. Its fundamental change involves determinism of proposal numbers and content-based versioning. 

![pristine badge](https://img.shields.io/badge/pristine-%20reference-informational.svg?style=flat?link=http://left&link=http://github.com/etclabscore/pristine)

The Star is meant to be replaced with the prefix/acronym of the users choice, though the prefix MUST be the same for all participants of the particular protocol specification.

For example, All forks of the Star Improvement Proposal relating to the bitcoin network MUST be called `BIP`. The differentiator being the location/domain/github organization to which the \*IP belongs.

# Changes to BIP/EIP/ECIP
## Version
Star Improvement Proposals are versioned by the content of their name. First we create a hash of the preamble, then we use a portion of it to create the version hash.

### Preamble hash
SHA-3-512 of the proposal [preamble](https://github.com/ethereumclassic/ECIPs/blob/master/ECIP-1.sample.md#what-is-an-ecip) encoded with BASE58.

### Version Hash
MUST be derived by the last 8 characters of the [Preamble Hash](#preamble-hash). This `version` naming scheme is deterministic in that groups or individuals may choose to include another's proposal without any numbering conflicts.

## Proposal Number
Star improvement proposals will retain a human friendly proposal number. However, this number will be derived from the hash such that it remains deterministic. The proposal number will be derived as the trailing 4 integers from the [Preamble Hash](#preamble-hash).

## Creating a proposal
Once you have your \*ip repo up, people submit proposals to it via pull requests, adding a file named {networkName}IP-{[proposal number](#proposal-number)}. Once the proposal is implemented by your team / group, you may signal your readyness by merging the pull request.

Example:

- Proposed Preamble:
```
Title: Byzantium on block 696969
Author: Santa Clause <a@b.c>
Discussions-To: a@b.c
Status: Draft
Type: Standards Track
Created: 2020-05-25
Replaces: FSEgfyewqYNvTLsCZeKFTv7k7NCjBM6jkWMHp2pCXYnmfwtLKptWMqQreXqMKg3B5KEA4TAcEwZ3doMTkVhjyC5TPpffszJkwhdAqVerCL4RsxBC7mBVY6gyvQeELTcbLYGjm1ndTGHYhPMYGKqAv1wXMdYcDiiKnL5sjyNKBVFgDmh8bHDnpK41NYfT5atxfm5qRPcG6KR6ZEvmrmeb5T9bXEhSEg5pQmRtz4P3RiYMRi8
Superseded-By: 6em822CkxkjZZW12fN2kc6PhEniwKcptMLgw1gbMGZvtCoRcstrBP6vCFGesqEGp4NcjLQ1CJxA1JDRkJZyoKdp7Qoc2i4aDVAAy9Lm9i7qHYqN2fLWwtvzD6Zprze7hDzqjRHCWQTPhWw4dbr89Fgqdtf59mk1nCQ9UGGRiYQE9ZF8
```
- Base-58 Hash: `ATMBgrfrx3XMNhG8WSxoayLCAtL8vHxykBSQWozTYh5GfJQ8EaiBR7rZRv2BYz9gQ8Sxn3yMYTd9S9mjVTX2wi4LziRpAixB7zCoqyJKRmPZdCgaY12B2ETs86bijRHunMTogLoQSPGThnMiaowKZLpKF7caBXZEyDZhSWRY4hfsJzmDESwJTMrvj5LXyN`
- Resulting \*IP Name: `ECIP-Byzantium-rvj5LXyN`
- Resulting Human-Friendly version number: `LXyN`


### Start using this
1. Fork _this_ repository.
2. Change the name to your network prefix/ accronym.
3. Create the first {your network accronym}IP to determine the standards and procedures for your StarIP repo.
4. Take old proposals and move them in with new version hashes

### Contributing

How to contribute, build and release are outlined in [CONTRIBUTING.md](CONTRIBUTING.md), [BUILDING.md](BUILDING.md) and [RELEASING.md](RELEASING.md) respectively. Commits in this repository follow the [CONVENTIONAL_COMMITS.md](CONVENTIONAL_COMMITS.md) specification.
