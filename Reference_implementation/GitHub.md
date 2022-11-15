# Suggested Reference Implementation for GitHub open source projects

The goal of this document is to show how far a GitHub project can get using as much native tooling as possible toward achieving up to maturity level 3 for the Secure Supply Chain Consumption Framework (S2C2F).

The community helps maintain these suggested methods of implementing the requirements, and will be updated over time.

| Requirement ID | Requirement Title | Maturity Level | Reference Implementation in GitHub |
| --- | --- | --- | --- |
| ING-1 | Use public package managers trusted by your organization | L1 | Ex. npmjs.org, DockerHub |
| ING-2 | Use an OSS binary repository manager solution | L1 | GitHub Packages |
| ING-3 | Have a Deny List capability to block known malicious OSS from being consumed | L3 | a Deny list can be achieved through [Dependency Review action](https://josh-ops.com/posts/dependency-review-action/). You must create a branch protection rule for your default branch, and select "Require status checks to pass before merging" box. If a component has vulnerabilities, this part of the build will fail. And GitHub now auto-creates CVEs for malicious components, so this is in-effect your Deny List. |
| ING-4 | Mirror a copy of all OSS source code to an internal location |  L3 | [Duplicate a repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/duplicating-a-repository) |
| SCA-1 | Scan OSS for known vulnerabilities | L1 | Recommend using [GitHub dependency graph](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph) for your repo for scanning vulns |
| SCA-2 | Scan OSS for licenses | L1 | Recommend configuring [Dependency Review](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/configuring-dependency-review#configuring-the-dependency-review-github-action) for license management |
| SCA-3 | Scan OSS to determine if its end-of-life | L2 | [OpenSSF Scorecard](https://github.com/ossf/scorecard) - actively maintained (inactivity for X years). Security Insights (Luigi) |
| SCA-4 | Scan OSS for malware | L3 | [OpenSSF Package Analysis](https://github.com/ossf/package-analysis) |
| SCA-5 | Perform proactive security review of OSS | L3 | Proactive security scans will be done out-of-band from a build. Usually it's an action that can be taken on cloned source |
| INV-1 | Maintain an automated inventory of all OSS used in development | L1 | [GitHub Dependency Graph](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph) |
| INV-2 | Have an OSS Incident Response Plan | L2 | Write one - be focused on how to roll back versions of OSS |
| UPD-1 | Update vulnerable OSS manually | L1 | |
| UPD-2 | Enable automated OSS updates | L2 | [Dependabot](https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts) |
| UPD-3 | Display OSS vulnerabilities as comments in Pull Requests (PRs) | L2 | [Dependency Review](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-dependency-review) via [GHAS](https://docs.github.com/en/enterprise-server@3.4/get-started/learning-about-github/about-github-advanced-security) |
| AUD-1 | Verify the provenance of your OSS | L3 | Repo it came from and commit hash from where it came. GitBOM? SBOM? |
| AUD-2 | Audit that developers are consuming OSS through the approved ingestion method | L2 | An index methodology to identify the OSS code undeclared. Searching for Copyright and != your company name |
| AUD-3 | Validate integrity of the OSS that you consume into your build | L2 | This is usually performed by the language package client |
| AUD-4 | Validate SBOMs of OSS that you consume into your build | L4 | |
| ENF-1 | Securely configure your package source files (i.e. nuget.config, .npmrc, pip.conf, pom.xml, etc.) | L2 | https://azure.microsoft.com/en-us/resources/3-ways-to-mitigate-risk-using-private-package-feeds/ |
| ENF-2 | Enforce usage of a curated OSS feed that enhances the trust of your OSS | L3 | Enforce a [branch protection rule](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests) to enforce that “OpenSSF Package Analysis” was run |
| REB-1 | Rebuild the OSS in a trusted build environment, or validate that it is reproducibly built | L4 |  |
| REB-2 | Digitally sign the OSS you rebuild | L4 | |
| REB-3 | Generate SBOMs for OSS that you rebuild | L4 | |
| REB-4 | Digitally sign the SBOMs you produce | L4 | |
| FIX-1 | Implement a change in the code to address a zero-day vulnerability, rebuild, deploy to your organization, and confidentially contribute the fix to the upstream maintainer | L4 | | 
