# \*IPs - `star improvement proposals`
*Written by Zachary Belford & Shane Jonas*

Star Improvement Proposals are an open standard for contributors to propose changes, additions, on deprecations of core protocol specifications.

The Star is meant to be replaced with the prefix/accronym of the users choice, though the prefix MUST be the same for all participants of the particular protocol specification.

For example, All forks of the Star Improvement Proposal relating to the bitcoin network MUST be called `BIP`. The differentiator being the location/domain/github organization to which the \*IP belongs.

Star Improvement Proposals are versioned by the content of their name. That is, in the case of making a proposal, the `version` identifier of the proposal MUST be derrived by the last 8 characters of the SHA-3-512 of the proposal name. This `version` naming scheme is deterministic in that groups or individuals may chose to include another's proposal without any numbering conflicts.

Once you have your \*ip repo up, people submit proposals to it via pull requests, adding a file named {networkName}IP-{version}. Once the proposal is implemented by your team / group, you may signal your readyness by merging the pull request.

Example:

- Proposal Name: `Byzantium Upgrades on block 123123`
- Resulting \*IP Name: `ECIP-cebf0a05`
