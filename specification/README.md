# Maintaining the OSS SSC Framework Specification

> ⭐: **Click
> _[here](Open_Source_Software_(OSS)_Secure_Supply_Chain_(SSC)_Framework.pdf)_ for the PDF of the specification**

## Updates to the specification

The OSS SSC Framework specification is intended to be a living document
created and maintained for the community by its members.

Updates to the whitepaper, suggestions for updates, or discussion for updates
should initiate with an [issue](https://github.com/microsoft/oss-ssc-framework/issues)
submitted to the repo and labeled with "discussion" and "specification".

### Markdown

The living OSS SSC Framework is captured in [markdown](framework.md) and is where all updates will take place.

### Contributing updates

All members of the community are welcome to contribute updates to the OSS SSC Framework specification. We
ask potential contributors to refer to the original design decisions, listed
below, as guidance when determining the content of their updates.

It is highly recommended that you seek peer review for your updates beyond that
of the Technical Leads of the working group.

After the issue has been triaged in the community call, and has been tagged with "Spec Change", the next step is to submit a PR to the [markdown](framework.md) with the proposed changes. Once the PR is submitted, please link the PR to the issue to request a review.

### Versioning and publishing

It is expected that many minor updates will occur, corrections to grammar,
spelling, clarification in language, translations, etc.  When these occur they
are considered minor changes to the overall content and will not warrant the
regeneration of the PDF.

When significant changes to the intent, content, or numerous minor changes
occur, the OSS SSC Framework working group will assess and determine if a new major version
of the PDF needs to be published.  When this decision is made, the markdown content
will be converted to text document and sent to the OSS SSC Framework technical writers to
create the PDF.  The PDF will then be published back into the repository
annotating the new version, updating the links in the README.md accordingly.

Minor updates to the markdown shall receive a minor version bump indicated in
the Metadata table of the document and recorded as WIP.  When enough significant
changes have been recorded, the markdown will be placed "In Review" (via PR) and
solicited to the OSS SSC Framework mailing list for review, at a
minimum.

Upon completion of review, the OSS SSC Framework technical writer shall provide final
approval on the PR.  At which point the markdown state will be changed to
"Approved" and merged.

## Original design decisions

The OSS SSC Framework creation occurred using the below general design decisions which
should be considered when updating the content.

* Consider if the content already exists elsewhere.  Provide references to
  comprehensive information on a topic rather than re-writing the content.  This
  not only allows us to provide summarization of complex topics, but also
  exposes the audience to other avenues of information for which they may be
  unaware.
* Determine if the content is better suited as it's own document, such as a
  how-to, blog, or whitepaper of itself.
* Determine if your suggestion belongs in the high-level solution-agnostic set of Practices - which can be used in any scenario - or if your suggestion is more of a detailed implementation-level requirement.
* Identify if the proposed requirement is realistic or aspirational. Suggest a level of maturity that fits with the themes for each maturity level.
