# \*IPs - Star Improvement Proposals
*Written by Zachary Belford & Shane Jonas & Donald McIntyre & *

Star Improvement Proposals is an extension of the BIP/EIP/ECIP process, with some changes to allow for decentralization of the process. Its fundamental change involves determinism of proposal numbers and content-based versioning. 

The Star is meant to be replaced with the prefix/accronym of the users choice, though the prefix MUST be the same for all participants of the particular protocol specification.

For example, All forks of the Star Improvement Proposal relating to the bitcoin network MUST be called `BIP`. The differentiator being the location/domain/github organization to which the \*IP belongs.

# Changes to BIP/EIP/ECIP
## Version
Star Improvement Proposals are versioned by the content of their name. First we create a hash of the preamble, then we use a substring of it to create the version hash.

### Preable hash
SHA-3-512 of the proposal [preamble](https://github.com/ethereumclassic/ECIPs/blob/master/ECIP-1.sample.md#what-is-an-ecip).

### Version Hash
MUST be derived by the last 16 characters of the [Preamble Hash](#preamble-hash). This `version` naming scheme is deterministic in that groups or individuals may choose to include another's proposal without any numbering conflicts.

## Proposal Number
Star improvement proposals will retain a human friendly proposal number. However, this number will be derived from the hash such that it remains deterministic. The proposal number will be derived as the trailing 5 integers from the [Preamble Hash](#preamble-hash).

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
Replaces: e0c214e23b458ee5efeb53aebe632b70ae2d4ed3c682775e674eef5939f2d2d740c3b0199d40d08bb1b943862b27f0d8977fd43d0cde711d02d3a3b1b9616b8a
Superseded-By: 799c8bd30186f2dcfd7c8ef67d36a4b9f3c1ff73d3a7d4df4cf1808bde9d4cde3d19f441425782b3d1465757520af51ffa93eccb25f9074dc304226f81ebd96c
```
- Resulting \*IP Name: `ECIP-Byzantium-6be1872777f7a7f4`
- Resulting Human-Friendly version number: `77774`


To Start using this:
1. Fork it
2. change the name to your network accronym
3. Create the first {your network accronym}IP to determine the standards and procedures for your StarIP repo.
4. Take old proposals and move them in with new version hashes

### Contributing

How to contribute, build and release are outlined in [CONTRIBUTING.md](CONTRIBUTING.md), [BUILDING.md](BUILDING.md) and [RELEASING.md](RELEASING.md) respectively. Commits in this repository follow the [CONVENTIONAL_COMMITS.md](CONVENTIONAL_COMMITS.md) specification.
