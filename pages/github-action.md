- ## Limit
- Official runner not support `m1` cpu, (Oct 23rd, 2022)
- Self host runner
	- Support `m1` (ARM64)
	- All software needs to be installed by yourself ( [official runner image](https://github.com/actions/runner-images/blob/main/images/macos/macos-12-Readme.md) )
- Price ( [ref](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions#minute-multipliers) )
	- Minute multipliers
		- macos * 10 Minute
	- Per-minute rates is most **expensive**
		- | Operating system | Cores | Per-minute rate (USD) |
		  | ---- | ---- | ---- |
		  | macOS | 3 | $0.08 (0.63 hkd)|
-