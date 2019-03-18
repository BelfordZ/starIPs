# \*IPs - Star Improvement Proposals
*by Zachary Belford, Shane Jonas, Donald McIntyre, Yaz Khoury, Anthony Lusardi, Tomaz Kariz*

![pristine badge](https://img.shields.io/badge/pristine-%20reference-informational.svg?style=flat?link=http://left&link=http://github.com/etclabscore/pristine)

Star Improvement Proposals are an open standard for contributors to propose changes, additions, or deprecations of core protocol specifications.

The Star is meant to be replaced with the prefix/accronym of the users choice, though the prefix MUST be the same for all participants of the particular protocol specification.

For example, All forks of the Star Improvement Proposal relating to the bitcoin network MUST be called `BIP`. The differentiator being the location/domain/github organization to which the \*IP belongs.

Star Improvement Proposals are versioned by the content of their name. That is, in the case of making a proposal, the `version` identifier of the proposal MUST be derived by the last 8 characters of the SHA-3-512 of the proposal name. This `version` naming scheme is deterministic in that groups or individuals may choose to include another's proposal without any numbering conflicts.

Once you have your \*ip repo up, people submit proposals to it via pull requests, adding a file named {networkName}IP-{proposalName}-{version}. Once the proposal is implemented by your team / group, you may signal your readyness by merging the pull request.

Example:

- Proposal Name: `Byzantium`
- Resulting \*IP Name: `ECIP-Byzantium-cebf0a05`


### Start using this
1. Fork _this_ repository.
2. Change the name to your network prefix/ accronym.
3. Create the first {your network accronym}IP to determine the standards and procedures for your StarIP repo.
4. Take old proposals and move them in with new version hashes

### Contributing

How to contribute, build and release are outlined in [CONTRIBUTING.md](CONTRIBUTING.md), [BUILDING.md](BUILDING.md) and [RELEASING.md](RELEASING.md) respectively. Commits in this repository follow the [CONVENTIONAL_COMMITS.md](CONVENTIONAL_COMMITS.md) specification.
