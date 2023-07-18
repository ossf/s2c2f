# Frequently Asked Questions

Below are some frequently asked questions regarding the Framework. If you have further questions, feel free to start a discussion by opening an [Issue](https://github.com/ossf/s2c2f/issues).

- [What is the Secure Supply Chain Consumption Framework (S2C2F)?](#what-is-the-secure-supply-chain-consumption-framework-S2C2F)
- [What does this Framework focus on securing?](#what-does-this-framework-focus-on-securing)
- [How do you define OSS?](#how-do-you-define-OSS)
- [Why should I use the S2C2F?](#why-should-i-use-the-s2c2f)
- [What is this Framework not?](#what-is-this-framework-not)
- [Why is this Framework focused on open source?](#why-is-this-framework-focused-on-open-source)
- [How does this Framework relate to other supply chain security specifications like SLSA?](#how-does-this-framework-relate-to-other-supply-chain-security-specifications-like-slsa)
- [What is the difference between the SCA-5 and FIX-1 requirements?](#what-is-the-difference-between-the-SCA-5-and-FIX-1-requirements)

## About the framework

### What is the Secure Supply Chain Consumption Framework (S2C2F)?
The S2C2F is a combination of processes and tools for any organization to adopt to help establish a secure OSS ingestion process to protect developers from OSS Supply Chain threats and to help establish a governance program to manage your organization’s use of OSS. The framework is based on three core concepts: control all artifact inputs, continuous process improvement, and scale.

### What does this Framework focus on securing?
This framework focuses on securing OSS dependencies like PyPI, Maven, NuGet, npm, etc. The implementation guide does not apply to containers, but the 8 high level practices do. For further container guidance, please refer to the [Cloud Native Computing Foundation (CNCF) projects](https://www.cncf.io/projects/).

### How do you define OSS?
Open Source Software, as adopted from [The Free Software Definition](https://en.wikipedia.org/wiki/The_Free_Software_Definition), is software that ensures that the end users have freedom in using, studying, sharing and modifying that software. For more details about the definition of Open Source Software (OSS), see [The Open Source Definition](https://opensource.org/osd/).

### Why should I use the S2C2F?
Our framework provides the support and implementation guidance to protect your supply chains and prevent open source software threats from compromising your organization’s software and development environment. The framework includes solution-agonistic practices – suited for individuals like compliance/risk managers, security managers, engineering managers, and Chief Information Security Officers – plus an implementation guide with recommended tooling – suited for software developers, Continuous Integration and Continuous Development administrators, and security practitioners.

### What is this Framework not?
The S2C2F does not provide guidance on how to secure your DevOps workflows, how to secure your build infrastructure, how to secure the code you author, or how to secure your containers.

### Why is this Framework focused on open source?
Across the software industry today, developers are using and relying upon OSS components to expedite developer productivity and innovation – which makes OSS a critical piece of any software’s supply chain. However, cyberattacks that specifically target open source are growing at an exponential rate, as they are trying to abuse these package manager ecosystems to either distribute their own malicious components or to compromise existing OSS components. 

### How does this Framework relate to other supply chain security specifications like SLSA?
The S2C2F is focused on securely consuming OSS and makes an excellent bridge to other producer-focused supply chain security frameworks, such as SLSA.

## Requirements

### What is the difference between the SCA-5 and FIX-1 requirements?
`SCA-5: Perform proactive security review of OSS - Identify zero-day vulnerabilities and confidentially contribute fixes back to the upstream maintainer.`

SCA-5 requirement is simply that your organization is performing proactive security reviews of OSS and helping improve the security of the entire ecosystem by partnering with the upstream maintainer (confidentially - outside of public GitHub issues via [private security notifications](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/privately-reporting-a-security-vulnerability)) and suggesting a fix.

`FIX-1: Implement a change in the code to address a zero-day vulnerability, rebuild, deploy to your organization, and confidentially contribute the fix to the upstream maintainer - To be used only in extreme circumstances when the risk is too great and to be used temporarily until the upstream maintainer issues a fix.`

FIX-1 is when you come across a zero-day vulnerability that is so severe that your organization feels that they can't wait for the upstream maintainer to issue a public fix. The only other action would be to implement a private fix (just for your team/organization) while you continue trying to partner with the upstream maintainer on a public fix. A private fix should always be considered a temporary risk reduction measure for extreme circumstances, as your team/organization should plan to convert to the public fix once available.
