# Notary Project Meeting Notes from January 2023 to June 2023

## Jun 29, 2023

### Attendees

- Nagarajan Jayabal
- Pritesh
- Roseline Bassey
- Sajay
- Samir Kakkar
- ToddySM
- Zach

### Agenda Items

- We need to create and publish the blog post of security audit report announcement on July 5 or July 6 per discussion with Adam in Slack (Feynman)
- Review the new [Notary documentation directory structure](https://docs.google.com/document/d/15y_U7Yyqlysw-rJDolZct5wjhlZHpoLeBvqVod6OTcs/edit) (Roseline/Feynman)
- Request to review the [maintainer nomination](https://github.com/notaryproject/.github/issues/34) for Zach (Feynman)
- Lack of feedback from `notary` repo maintainers - https://github.com/notaryproject/notary/pull/1685

### Notes
- Ada Logics is requesting the Notary Project community to create the blog post. Samir will check with Pritesh whether he can take ownership of the creation of the blog post
    - The blog post should summarize the comletion and the findings
    - Blocking issues may be: thread model completion  and the the secure deployment documentation (https://github.com/notaryproject/notaryproject.dev/pull/228)
- Next steps on the outline the ask is to leave feedback in the Google doc. 
    - We need to have a broader discussion about the high level information structure whether Notation content should be in the subdirectory? (Zach)
    - Roseline will discuss with Feynman and Yi and will review the feedback on Monday
- Zach's nomination - Pritesh to talk with Niaz, Toddy to ping Steve and Justin from Docker
- `notary` repo - Pritesh to talk with Niaz, Toddy to ping Steve and Justin from Docker
- (Sajay) Do we have anything in the Governance about maintainers participation? Toddy will review the governance documents and send an update.

## Jun 26, 2023

### Attendees

- Yi Zha
- Shiwei Zhang
- Junjie Gao
- Toddy SM
- Samir Kakkar
- Roy Williams
- Pritesh
- Miran
- Sajay
- Patrick Zheng

### Agenda Items
- Status update on Notation naming issue
    - `notary` [readme.md](https://github.com/notaryproject/notary/pull/1685) -> `.github` [issue#35](https://github.com/notaryproject/.github/issues/35) -> `.github` [readme.md](https://github.com/notaryproject/.github/pull/32) -> update readme file for each repo
- Confirm the date to publish security audit report
- Set up GitHub Actions repo per [issue](https://github.com/notaryproject/.github/issues/30)
- [Notation v1.0.0 release blog](https://hackmd.io/St0P06gGQxK_pbeVrVfqaw?view) is ready for review. We have booked a slot to publish it on cncf.io (Feynman)
- [VMware Bitnami team](https://hub.docker.com/u/bitnami) was failed to use Notation with Docker Hub last week. Considering Bitnami is a large publisher, any suggestions to unblock them? (Feynman)

### Notes
- Sajay walked through the `notary` [PR 1685](https://github.com/notaryproject/notary/pull/1685), Samir shared some comments that are nice to have
    - Borrowing some feedback from [Emily's proposal](https://github.com/notaryproject/.github/pull/32#pullrequestreview-1488153711)
- This [PR 1685](https://github.com/notaryproject/notary/pull/1685) requires org maintainers to approve.
- Toddy will create an issue for new repository related to spec and folder structure.
- Feynman will continiously follow up with security audit team on security audit report.
- Toddy will create a new repo for GitHub actions per [issue](https://github.com/notaryproject/.github/issues/30)
- Request maintainers to review Notation v1.0.0 release blog
- Feynman called out broken links under notaryproject repo, see [issue](https://github.com/notaryproject/notaryproject/issues/266). We can take a look at https://shreeshail.medium.com/how-to-checks-all-markdown-files-in-your-repository-for-broken-links-474c106eec87 to see whether it helps, we can continously explore other options.

### Recording
https://www.youtube.com/watch?v=XdFcAnajpik

## Jun 22, 2023

### Attendees
- Sajay Antony
- Samir Kakkar
- Josh Duffney
- Miran Kurukulasuriya
- Roseline Bassey 
- Toddy SM
- Zach

### Agenda Items
- Renaming the "notaryproject" repo

### Notes
- Samir and Miram are saying that the repo names are confusing and a cleaner specification name will help
    - Challange with the proposed name "notation-spec" is that other communities are using the specification without using Notation CLI or even its libraries
    - From discussions the convergence is to name the repository with more generic name like `specifications`
    - Need to go through the process to agree among maintainers though
- Next steps
    - Update the README.md for the https://github.com/notaryproject/notary/ repository to clearly state that this is the TUF implementation for a client and a server. 
    - Associate this with the term `notary`
    - Agree with maintainers to merge the updates for that README.md
    - After this is done, proceed with proposal in https://github.com/notaryproject/.github/issues/35
    - Consider finailizing a specs repo with a preifx like signature-specs or notation-specs. 
        - Given that notary project is more than notation which is CLI and refence implementation consider notation-specs might be over-constraining [sajay]
        - Current specs repo has notation plugin specs that are scoped to the CLI only and potentially should be moved to notation. [sajay]

## Jun 19, 2023

### Attendees
- Sajay Antony
- Yi Zha
- Samir
- Toddy SM
- Pritesh Bandi
- Feynman Zhou
- Fan Du
- Miran Kurukulasuriya
- Shiwei Zhang
- Patrick Zheng
- Junjie Gao


### Agenda Items

- Disuss the [proposal](https://github.com/notaryproject/.github/issues/35) and align way forward
- Walk through other documentation status

### Note

Next steps for fixing the naming issues:
- Samir to work with Millind and Niaz to get super-majority of approval for [PR #32](https://github.com/notaryproject/.github/pull/32/files) and [proposal issue #35](https://github.com/notaryproject/.github/issues/35)
- @Maintainers to review [PR #32](https://github.com/notaryproject/.github/pull/32/files) and [proposal issue #35](https://github.com/notaryproject/.github/issues/35), and provide comments
- @toddysm will update [PR #32](https://github.com/notaryproject/.github/pull/32/files) according to [proposal issue #35](https://github.com/notaryproject/.github/issues/35)
- @Feynman and @yizha1 Update the README.md in each repository to resolve Toddy's issue raised in each repo, see [#715](https://github.com/notaryproject/notation/issues/715) as an example

Next steps for archiving `notaryproject` repo and creating new repo named `specifications`
- Review and amend the process if needed about how to archive the repository in governance.md, there was an [issue](https://github.com/notaryproject/.github/issues/36) created to address it. @Feynman will take actions on this issue.
- Create an issue based on the process to vote for archiving `notaryproject` repo and creating new repo named `specifications`. Request super majority approvals.
- Need to merge all the necessary PRs in `notaryproject`, and clean up history PRs (no activities for more than 6 months). Require @Maintainers to actively review it.

Security audit:
- @Maintainers to review the security report, and align the publishment date with the security audit team

We also discussed that if it is possible to release Notation v1 first, and then cut the specifications release later, since notation is an implementation reference based on the spec. Pritesh and Samir mentioned that it's better that specification can be released together with Notation, so that Notation can refer to it. Feynman and Toddy also shared the asking from different users on when Notation v1 is released.

### Recording

https://www.youtube.com/live/sOBnpl5ysh0

## Jun 15, 2023

### Attendees
- Roseline Bassey (LFX Mentee for documentation)
- Roy Williams
- Samir Kakkar
- ToddySM

### Agenda Items

- Notaton v1 PR status. We made progress these days, see [board](https://github.com/orgs/notaryproject/projects/10/views/28), The following PRs are pending, need further actions:
    - Two security doc PRs need Toddy and Samir to re-review to remove `request changes` if LGTM: [219](https://github.com/notaryproject/notaryproject.dev/pull/219), [228](https://github.com/notaryproject/notaryproject.dev/pull/228)
    - Review release checklist and management doc
- Confirm to create new repo for `setup_notation` Github actions, https://github.com/notaryproject/.github/issues/30, we have 6 out 9 maintainers LGTM now.
- [Nominate Zach to be a maintainer for the notaryproject.dev repo](https://github.com/notaryproject/.github/issues/34)
- Notation naming PRs, how to proceed?

### Note
- The remaining items for the release are mostly governance and documentation. The only code related item (https://github.com/notaryproject/notation/issues/696) is complete.
- For the GitHub Action repository, proposed to hold on the creation until after 1.0.0 release. 
    - We need to update the docs with information about the Hashicorp repo as well as the repo README
- Samir will ping Pritesh, Nyaz, and Milind for Zach's nomination
- Proposal
    - Archive the `notaryproject` repository and create `specification` repository (ToddySM)
        - (Samir) Samir asked whether this repo will be used for the specifications/design for the actual implementation
        - We will create an issue for discussion and we need maintainers agreement.
        - (Roy) Proposal is to create separate folders and have README in each folder for what specifications it contains (currently we have OCI but in the future we will have signing of non-OCI artifacts - Samir)
        - (Samir) We need to close the current PRs in the `notaryproject` repo before the move to the new repository
    - For the security reports and threat models the proposal is to have them in folder under `.github` (ToddySM)
        - (Samir) Samir asked how users who are interested in a particular implementation will find the reports. We will continue the discussion on this.
        - We will create an issue for discussion and we need maintainers agreement.
    - (Samir) We need an acknowledgement of the names we used in the past and the terminology we will continue to use going forward.
    - (ToddySM) We need to update each individual repository before the 1.0.0 release (Samir is in agreement)
    - (Samir) Let's put our intent in the https://github.com/notaryproject/notaryproject/issues/244 so that everyone who provided feedback can see it
- (Roy) Did we ever document the policy that we took for COSE
    - Samir believes that this is formalized in the signature specification
    - (Roy) What is the policy from a governance point of view to take a dependency on implementation from other OSS projcets (ex. if there is a project with a single maintainer)
- (ToddySM) Process for archiving repositories and moving maintainers to emeritus status
    - Archiving repos is needed for the 1.0.0 release
    - Maintainers process is not blocking for 1.0.0 release but 

## Jun 12, 2023

### Attendees

### Agenda Items

- Notation v1 release [status check-in](https://github.com/orgs/notaryproject/projects/10/views/28)
- Status update: [vote for creating a repository for Notation GitHub Action](https://github.com/notaryproject/.github/issues/30)
- [The subpage design for the list of Notary security audit report](https://www.figma.com/file/rj5BvQDNPon4mipgajOlr5/Notary-website-landing-page-(Redesign)?type=design&node-id=0-1&t=eS58rXDFFdv3wrHb-0)
- [Nominate Zach to be a maintainer for the notaryproject.dev repo](https://github.com/notaryproject/.github/issues/34) (Feynman)
- Request review: Created a draft doc to demonstrate e2e signing and verification scenario on K8s - [Sign and verify an image with Notaion, Ratify, and Gatekeeper](https://hackmd.io/51bUjLFtRxqMutv2XYt-AQ?view)

### Notes

- @Samir review the [PR](https://github.com/notaryproject/.github/pull/32), and then we align the terms to be used
- @pritesh take a look at [release management issue](https://github.com/notaryproject/.github/issues/19)
- @Feynman to summarize the [Github actions vote issue](https://github.com/notaryproject/.github/issues/30), so that we can proceed.
- @Feynman to sent out the [namination issue](https://github.com/notaryproject/.github/issues/34) in slack
- Review [PR](https://github.com/notaryproject/notation/pull/559) by Byron

## Jun 8, 2023

### Attendees
- Pritesh
- Samir
- ToddySM
- Zach

### Agenda Items
- Ad-hoc

### Notes
- PR for AWS Signer plugin documentation. Pritesh will send PRs for review and approval
- Two items from the 1.0.0 board should be moved to "immediatelly post 1.0.0"
    - Homebrew https://github.com/notaryproject/notation/issues/571
    - Winget https://github.com/notaryproject/notation/issues/570
- Missing items from 1.0.0 release
    - Publishing the Security Audit (linking from the web site)
    - New item to update the banner on the website
    - New item to generate the CLI documentation 
- Release criteria - update the release criteria to make sure that all activities are included
    - The sequence is binaries -> Security Audit publishing -> web site changes -> announcement
    - Note: Zach doesn't have merge rights 
    - Samir is concerned that we are not complete with the governance work items before 1.0.0 release
        - We need to have a release document for the release - https://github.com/orgs/notaryproject/projects/10/views/32?pane=issue&itemId=23572624. 
            - We need to also need a release branch. We need to add work item for that. Required for 1.0.0.
            - We should also call out that RCs are not supported. We need doc work item. Not required for 1.0.0. We need to document this shortly after the release.
    - Notation naming needs to be complete before 1.0.0 release https://github.com/notaryproject/notaryproject/issues/244
    - Bug report templates also need to be added as 1.0.0 - PRs are ready
    - We need to update the https://github.com/notaryproject/notaryproject/blob/main/README.md as part of 1.0.0 release (Yi Zha) https://github.com/notaryproject/notaryproject/issues/260
    - We need to release the spec too as part of 1.0.0 (Yi Zha) https://github.com/notaryproject/notaryproject/issues/261
- Plan for release
    - We cannot release until the notaryproject work items are complete. We should start PRs ASAP and target to complete by Monday evening PDT
    - Target for release date is Wed June 14th

### Recording

## Jun 5, 2023

### Attendees
- Samir Kakkar
- Pritesh Bandi
- Shiwei Zhang
- Yi Zha
- Toddy Mladenov
- Jinjie Gao
- Miran Kurukulasuriya
- Patrick Zheng
- Josh Duffney
- Fan Du
- Sajay Antony
- Feyman Zhou

### Agenda Items

- Notation v1 status check-in
    - Suggest adding credentials store issue in v1 scope, [issue 696](https://github.com/notaryproject/notation/issues/696)
    - New issues reported, and suggest fixing it by v1 release
        - https://github.com/notaryproject/notation/issues/699
        - https://github.com/notaryproject/notation/issues/700
        - https://github.com/notaryproject/notation/issues/701
    - Walk though the [board](https://github.com/orgs/notaryproject/projects/10/views/28)
    - Publish security advisories
    - v1 blog outline: https://hackmd.io/St0P06gGQxK_pbeVrVfqaw?view
- [Vote](https://github.com/notaryproject/.github/issues/30) for Create a repository for Notation GitHub Action
- [Check the license header for Notation and its dependencies](https://github.com/notaryproject/notation/issues/706)
- Can we merge RC-7 release notes/blog today

### Notes
- Document [Notation general configuration for credential store](https://notaryproject.dev/docs/concepts/directory-structure/#general-configuration)
- create PRs for 4 issues discussed, if no big risk identified from the review, we can consider including it for v1 release.
- Josh will prepare a PoC for notation actions
- Publish security advisories and merge RC-7 blog today
- Move topic "Check the license header for Notation and its dependencies" to next meeting

### Recording

https://www.youtube.com/watch?v=Q3XCHQcfIxM

## Jun 1, 2023

### Attendees
- Miran Kurukulasuriya
- Pritesh
- Samir Kakkar
- ToddySM
- Zach

### Agenda Items
- Ad-hoc

### Notes
- Miran suggested that plugin use cases should be more prominent on the web site. Link to the issue https://github.com/notaryproject/notaryproject.dev/issues/268
    - How to use available plugins
    - What plugins are available
    - etc.
- Miran is working with Setup Notation GitHub action. He is currently running into some issues that he is discussing with Joshua.
- Miran is interested in how to sign releases on GitHub. 
    - Link to the local OCI layout may also help in certain situations https://notaryproject.dev/docs/how-to/oci-image-layout/
- Zach has open PR for the publishing the CLI reference. He would like to have that merged before 1.0.0. Link to the PR https://github.com/notaryproject/notation/pull/687
    - We need to look at the dependencies and make sure that there are no license violations
    - We should document the process for adding dependencies in the Contributor guide @Feynman and @yizha1
- Miran was also asking if there is any requirement to use TUF with the latest implementation of Notary
    - Would be good to document how the latest implementation of Notary and TUF relate


## May 30, 2023

### Attendees:
- Fan Du
- Feynman Zhou
- Jinjie Gao
- Miran Kurukulasuriya
- Patrick Zheng
- Pritesh
- Sahil
- Sajay Antony
- Samir Kakkar
- Shiwei Zhang
- Toddy Mladenov
- Yi Zha

### Agenda Items:
- Align v1 scope, see [board](https://github.com/orgs/notaryproject/projects/10/views/28)
- Align way forward for issue [227](https://github.com/notaryproject/notaryproject.dev/issues/227).
- Final review and publish security advisories
- Request to add [Notation interactive tutorial](https://killercoda.com/sahil/scenario/notation)(contributed by Sahil) to the website as an online demo environment
- We have two mentees are selected for two LFX mentorship projects
    - [Design and implement the new Notary website](https://mentorship.lfx.linuxfoundation.org/project/06774504-da91-469e-89f9-14fb18b6e0d8)
    - [Develop content for Notary documentation and blogs](https://mentorship.lfx.linuxfoundation.org/project/007ca3e9-c121-4428-8e63-57bc0418e98a)

### Notes:

- Aligned v1 scope, see [board](https://github.com/orgs/notaryproject/projects/10/views/28)
- Follow up the issue https://github.com/notaryproject/notation/issues/696, which could be in v1 scope.
- Callout for spec and documentation PR reviewing 
- AP on Yi to add next steps for issue #227
    - create a document on website for security best practies covering metadata contract, and releasing plugin securely. This document will be developed overtime.
- Toddy may report some issues for plugin spec
- AP on Feynman to create issue for adding `notation demo` on website.
- AP on Feynman to create a hackmd document for v1 blog.

### Recording
https://www.youtube.com/live/FppqJFHmUTo

## May 25, 2023

### Attendees:
- Lata
- Miran
- Pritesh Bandi (AWS)
- Pranit Patil
- Samir Kakkar (AWS)
- ToddySM

### Agenda Items:
- Release of Notation RC.6 by Friday 2023-05-26
- Release timelines
- Miran questions
- Lata and Pranit - LFX mentoriship

### Notes:
- All tracking issues for RC.6
    - @Pritesh will open an issue and PR for the release and get maintainers' votes
- Monday 2023-05-29 is a holiday in US. Can we vote on time to meet on Tuesday or Thursday ealy morning so folks from China.
- @Samir wants to take a little bit more cautious approach for the release
    - Can we have @Feynman and @yizha1 identify the governance and security and put all the work items for 1.0.0 release on the board
    - Final review on next week's meeting (TBD)
    - Targeting tentative date of 2023-06-12 for the 1.0.0 release
- Miran questions
    - Status of the Github Action for Notation - goal to release it as part of the 1.0.0 release
    - Follow up on signing installers and other artifacts - files like ZIP files can be pushed to an OCI registry and signed there as OCI artifacts
- Lata found several areas on the web site that can be improved
    - She can file issues if she wants to
- Pranit is also interested in the LFX 

### Recording
https://www.youtube.com/live/TzLctkaFxc8?feature=share

## May 22, 2023

### Attendees:
- _add yourself_

### Agenda Items:
- notation delete funtionality; Support deletion of signature.(Pritesh)
    - Created [issue](https://github.com/notaryproject/notaryproject.dev/issues/248) to document how to delete signature using ORAS. Yi will followup on adding documentation.
- PRs for Patrick Zheng account issue (Yi)
    - https://github.com/notaryproject/notation/pull/672
    - https://github.com/notaryproject/notation-go/pull/310
    - https://github.com/notaryproject/notation-core-go/pull/145
- Proposed steps towards Notation v1 release (Yi)
    1. Release `v1.0.0 RC-6` for fixing security advisories, and all other issues see [Planning board](https://github.com/orgs/notaryproject/projects/10/views/28)
    2. Merge documents required for security audit
    3. Publish security audit report by audit team
    4. Release Notation v1.0.0 (including only bug fixes), and release blog
- [added notation cert cleanup-test command](https://github.com/notaryproject/notation/pull/673)
- FYI: [Zoom to Youtube livestream guideline](https://lists.cncf.io/g/cncf-notary-maintainers/topic/how_to_enable_the/98852881?p=,,,20,0,0,0::recentpostdate/sticky,,,20,2,0,98852881,previd%3D1684428780599082518,nextid%3D1674576350188481552&previd=1684428780599082518&nextid=1674576350188481552)
- PR review: [add initial CODEOWNERS and MAINTAINERS to notation-hashicorp-vault repo](https://github.com/notaryproject/notation-hashicorp-vault/pull/2)

### Notes:
- Create a document issue for `how to delete signatures`. Yi will follow up on adding documentation.
- Plan notation RC-6 release on May 26 including the fixes for security advisories, bug fixes and improvements list in the notation board
- `notation cert cleanup-test` will be moved out of v1 scope.
- Notation v1 release will be planned on Jun 9, only critical bug fixes since RC-6 will be included.

### Recording
https://www.youtube.com/watch?v=PM43od6UUXQ

## May 18, 2023
### Attendees:
- Lata
- Miran Kurukulasuriya
- Precious Enyi
- Pritesh
- Sumit Maithany
- Toddy Mladenov
- Vani Rao

### Agenda

- Discuss the way forward, should we cut another release including all the v1 issues especially the following two: (Yi)
    - Change the flag name from `--plain-http` to `--insecure-registry` is a breaking change [issue#623](https://github.com/notaryproject/notation/issues/623)
    - Should this command `notation cert generate-test` behind experimental flag, see [issue#647 comment](https://github.com/notaryproject/notation/issues/647#issuecomment-1552741372)
- Notation v1.0.0-RC.5 release blog is ready for review, see [PR](https://github.com/notaryproject/notaryproject.dev/pull/218) (Feynman)

### Notes
- Yi's question about release for the below two - opinion is that we don't need new RC release for them
    - From last Monday's discussion we decided to use an alias for `--plain-http` which will make it backwards compatible and we don't need new release for that. This is a small change and can include in the final release 
    - For the secong issue we are not sure why it needs to be behind `EXPERIMENTAL` flag. This is only for thest purposes and should not be used in production. This needs more discussion.
    - In general we don't think we need a new release for those two. The first can be included in the release. For the second one, we need discussion and decide on Monday.
    - Vani asked question about which security issues will be fixed before release. We deferred the discussion to tomorrow's call with the security auditors and finalize on Monday's call
    - Toddy asked whether should we target a date for the final release. Work is finalized and the scope is defined except the security issues (Vani). Yi and Vani can work on updating the board https://github.com/orgs/notaryproject/projects/10/views/28. Please update the Slack channel when it is finalized.
- Goal is to get the blog finalized by Monday and publish on Tuesday
- Lata and Precious Enyi were new to the call and introduced themselves. They are part of the LFX mentorship program.
- Some questions from Miran
    - Asked about the release - date will be determined on Monday's meeting
    - When will DockerHub support Notary Project signatures
    - They are interested in signing the images as well as the installers of their Ballerina language https://ballerina.io/

## May 15, 2023

### Attendees:
- ToddySM
- Fan Du
- Miran Kurukulasuriya
- Sanjay
- Yi Zha
- Feynman Zhou
- Toddy SM
- Shiwei Zhang
- Patrick Zheng
- Junjie Gao
- Sajay Antony

### Agenda
- RC-5 release status checkin (Yi)
- Notation CLI [PR Review](https://github.com/notaryproject/notation/pulls)
- Notary project in [CNCF LFX mentorship](https://github.com/cncf/mentoring/tree/main/programs/lfx-mentorship/2023/02-Jun-Aug)
    - [New: Design and implement the new Notary website](https://mentorship.lfx.linuxfoundation.org/project/06774504-da91-469e-89f9-14fb18b6e0d8)
    - [New: Develop content for Notary documentation and blogs](https://mentorship.lfx.linuxfoundation.org/project/007ca3e9-c121-4428-8e63-57bc0418e98a)
    - [WIP: Notary: HashiCorp Vault plugin for Notary](https://mentorship.lfx.linuxfoundation.org/project/9710c834-913d-487d-9ebf-8205cdf48ab4) and created a [notation-hashicorp-vault repo](https://github.com/notaryproject/notation-hashicorp-vault)

### Notes
    
- Welcome new participants: Sanjay, Miran and Fan
- Addressed comments for several PRs
- @patrickzheng200 to create an issue for account issues

## May 11, 2023

### Attendees:
- Pritesh Bandi
- Sumit Maithani
- ToddySM

### Agenda
- Ad-hoc

### Notes
- Sumit asked about feedback on the code copy functionality PR. Discussed the option to make it more accessible. Sumit will follow up with options
- Sumit has feedback on the Contributor Guide that it doesn't cover details about signing commits and signing off on commits. He will file issue to update the Contributor Guide
- Pritesh brought up the topic for RC.5. He will discuss the approach for implementation and come up with agreement offline. We will target release of RC.5 for Wed, May 17th 2023 evening PDT.

### Meeting Recording
- [link-goes-here]


## May 8, 2023

### Attendees:
- Yi Zha
- Feynman Zhou
- Toddy SM
- Shiwei Zhang
- Patrick Zheng
- Vani Rao
- Junjie Gao
- Bingqi Shang
- Samir Kakkar
- Sajay Antony
- _add yourself_

### Agenda Items:
- Impact of OCI 1.1.0-rc3 image spec changes on Notary. Will this impact the release? How about the dependencies on ORAS? Plan/work items (ToddySM)
- Notation v1 release status check-in, see [board](https://github.com/orgs/notaryproject/projects/10/views/28) (Yi)
- Will create a new repo `notation-hashicorp-vault` with 4 initial maintainers, see [proposal](https://github.com/notaryproject/.github/issues/26) (Feynman)
- Will cut the first release for [oras-credential-go](https://github.com/oras-project/oras-credentials-go) this week and integrate it into Notation to improve authentication experience (Feynman)
- Remind: [CNCF LFX Mentorship program](https://github.com/cncf/mentoring/tree/main/programs/lfx-mentorship/2023/02-Jun-Aug) application will be closed on May 9 (Feynman): 

### Notes:

- AP: Yi to create an issue to elaborate on the changes for Referrers API
- AP: Feynman to create an issue to propose deprecating the flag `--signature-format` OCI artifact manifest 
- Continue the offline discussion on the [issue](https://github.com/notaryproject/notation/issues/623) 

### Meeting Recording

View the meeting video at [youtube](https://www.youtube.com/watch?v=YckD5v8ZC9I)

## May 4, 2023

### Attendees:
- Vani
- Samir
- Toddy

### Agenda Items:

### Notes:
- Add guidance for migration from Docker Content Trust (old Notary) to Notation as part of the release (blog - check with Feynman and Yi)
- Security audit draft report will be available and shared by Adam by the end of the week.
- For the release https://github.com/orgs/notaryproject/projects/10/views/28 there are few items that still need discussion. We should close those in Monday's meeting
- Still targeting the release for 5/17. Blocking items are the disclosured filed as part of the security audit. 

### Meeting Recording

View the meeting video at [TBD]

## May 1, 2023

### Attendees:
- Vani Rao
- Pritesh
- Toddy

### Agenda Items:

### Notes:
- Relese checklist for Notation general availability (ToddySM)
    - Target 5/17 (tentative)
    - Vani will go over the board (see below) and add comments what should be included in the release and what we can move out
- Security audit newly discovered issues (ToddySM)
    - Toddy to ask Adam to schedule meeting for 8 AM PDT on Thrusday
- [Notation v1.0.0 issues in planning board](https://github.com/orgs/notaryproject/projects/10/views/28) (Feynman)
- Vote: proposal to create a new subproject in the Notary org for the HashiCorp Vault KMS plugin https://github.com/notaryproject/.github/issues/26
    - Vani will discuss with Samir and Pritesh and they will cast their votes for the subproject
- Toddy to talk with Patrick to link the design to the issues
    - https://github.com/notaryproject/notation/issues/623
    - https://github.com/notaryproject/notation/issues/633

- CNCF LFX Mentorship program application will be closed on May 9, we can submit project proposals to LFX before May 9 (Feynman): https://github.com/cncf/mentoring/tree/main/programs/lfx-mentorship/2023/02-Jun-Aug

### Meeting Recording

View the meeting video at [TBD]

## Apr 24, 2023

### Attendees:
- _add yourself_
- Patrick Zheng

### Agenda Items:
- RC.4 release official announcement (Yi)
    - blog [PR](https://github.com/notaryproject/notaryproject.dev/pull/175)
    - quickstart [PR](https://github.com/notaryproject/notaryproject.dev/pull/155)
- [Revocation support: using revocationDate/invalidityDate](https://cloud-native.slack.com/archives/CQUH8U287/p1681778707365059) (Pritesh)
- Align [1.0.0 scope](https://hackmd.io/qEQfes82Rb2VuzN6whzfUw) (Yi)
- Chores (Yi)
    - Updating contributing guide [PR](https://github.com/notaryproject/.github/pull/25)
    - Remove milestones "Discuss" and "Future"
    - Define what label we needed and remove useless labels
- [HashiCorp Vault KMS plugin](https://github.com/notaryproject/notation/issues/521) has the prototype and doc. The next step is to request to create a subproject and iterate (Feynman, Patrick, Bingqi)
    
### Notes:
- Revocation leftover issue need to be addressed by 1.0 release, @yizha1 will ping Shiwei for comments
- Agree on defining labels for managing issues first, and remove `discuss` and `future` milestone after labels are aligned. A proposal will be prepared by @yizha1 
- Shared overview of HashiCorp Vault KMS plugin, and plan a demo on May 8, @Feynman to check the demo plan with Bingqi
- Notary maintainers to vote for 

### Meeting Recording

View the meeting video at https://youtube.com/live/ND3p9ax4qE8

## Apr 17, 2023

### Attendees

- Yi Zha
- Feynman Zhou
- Vani Rao
- Shiwei Zhang
- Patrick Zheng
- Billy 
- Kody-kimberl
- Pritesh
- Bingqi Shang

### Agenda Items
- Notation rc.4 release (Yi)
- Governance update, see [here](https://github.com/notaryproject/notaryproject/issues/244#issuecomment-1511468461) (Yi)
- Path forward for RC-4 and GA from the OSTIF meeting
- [The Notation intro video](https://drive.google.com/file/d/1bp6C3T9MHht5qEIYSamQS-1JJ-7IN-jX/view) recorded by Sai is available for internal preview. It will be published before KubeCon (Feynman)
- [CNCF LFX Mentorship program](https://github.com/cncf/mentoring/tree/main/programs/lfx-mentorship/2023/02-Jun-Aug) is open for application (Feynman)

### Meeting Notes
- RC.4: targeting Apr 20, still several PRs to go
    - Certificate revocation (2 PRs)
    - sign oci layout (2 PRs)
    - Fix vulnerabilities
- Governance update
    - Fix Naming issues `notation-go` and `notation-core-go` by v1 release
    - Release first version of threat model by v1 release.
    - Submit CNCF annual review after RC-4 release @Feynman 
- Prepare work items for v1 release, no feature will be planned. @yizha1 @vani
- Create an issue to vote for hashicorp plugin repository @Feynman 

### Meeting recording 

View the meeting video at https://youtu.be/ru8wCt-o510

## Apr 10, 2023

### Attendees
- Yi Zha
- Feynman Zhou
- Vani Rao
- Priteh
- Billy Zha
- Shiwei Zhang
- Patrick Zheng
- Sajay Antony

### Agenda Items
- RC-4 PRs status (Yi)
    - certificate revocation
    - sign/verify images in oci-layout directory
- Other items (Yi, Feynman)
    - INFO: The 2nd Notation security audit meeting
        -  Thursday, April 13, 4:00 – 5:00pm, UTC+1
    - Reduce to 2 PR approvals for `notation`, `notation-go`, `notaryproject.dev` repo. See the comments in the issues below:
        - https://github.com/notaryproject/notation-go/issues/296
        - https://github.com/notaryproject/notation/issues/616
        - https://github.com/notaryproject/notaryproject.dev/issues/169
    - Plan for CLI UX issues
    - Follow-up on "plugin or direct integration with build tools like docker"
        - There was a PoC of notation docker plugin in alpha.1 release, and it was not continued based on this [discussion](https://github.com/notaryproject/notation/discussions/251) 
- Adding ECR to the compatible registry list https://github.com/notaryproject/notaryproject.dev/pull/145#issuecomment-1502489649 (Samir, Feynman)


### Meeting Notes
- Split the [PR](https://github.com/notaryproject/notation/pull/613) into two: one for experimental flag, another for `notation policy` command. It was also agreed that `notation policy` command will not be marked as experimental.
- Feature of "Sign/verify oci-layout" will be the experimental feature.
- Yi suggest prioritizing UX issue with Vani after RC-4 release
- Further discussion required on "plugin or direct integration with build tools like docker" after kubecon.
- Need to follow up on fixing the youtube video (it's progressing but not fixed yet)

### Recording 

View the meeting video at https://youtu.be/aEyU5ihfJeg

## Apr 6, 2023

### Attendees 
- Sajay Antony
- ToddySM
- Samir Kakkar
- Michael Brown
- Roy Williams

### Agenda Items
- Clarifications on the local signing and verification needs 

### Meeting Notes
 - Should SBOMs be the only thing that is signed since the SBOM has the hash of the continer already. [Roy]
     - This might be the direction forward and it might be good for notary to provide guidance on these 
     - Current tooling and users don't yet have this workflow of producing or consuming SBOMS for the immediate needs we can continue focusing on the container signing scenario
     - [@toddysm] Signing non-container images is a valid user scenario since notation will be used to sign SBOMs. 
         - Having a way to specify a blob/manifest to sign in notation is important. 
 - OCI layout signing is hard since most tools don't produce OCI layouts, should we consider a plugin or direct integration with build tools like docker [Michael Brown]
     - The OCI layout implementation is currently a tool agnostic implementation and common denominator
     - We generally agree that a proper integration with build tools is the better user experience. 
     - As a follow up @toddysm  will reach out to Docker and what options we have
     - The group will have to decide on a user scenario before and that might be either in a plugin in notation or sample or docs. 

## Apr 3, 2023

### Attendees 
- kody-kimberl
- Sajay Antony
- Yi Zha
- Feynman Zhou
- Billy Zha
- Junjie cheng
- Shiwei Zhang
- Vani Rao
- ToddySM
- Samir Kakkar

### Agenda Items
- Notation RC.4 release status check-in (Yi/Vani)
    - PR waiting for approval from maintainers
    - Date for rc-4 release to be 04/10.
- Any pending clarifications on the local signing and verification https://hackmd.io/5CoAU-yvST-wtABtwR1XTA?view (Vani/Samir)
- Call-out: Triage and close old issues.(Yi)
- Governance issue status sync-up (Feynman)
    - CNCF has sent invitation of CNCF-related platforms to new Notary maintainers
    - The draft Notary Project Annual Review will be prepared this week
- Fixing any known issues to improve security (Samir)

### Meeting Notes
- There are still PRs not merged yet, so the new date proposed for RC-4 release is 4/10
- The experience and flag name of signing local artifacts was discussed. The decision is this feature will be marked as experimental, and an env variable like `XXX_EXPERIMENTAL=1` will be introduced in RC-4.
- Vani and Yi will start triaging and old issues
- Futher discussion on some known security issues on this Thursday community meeting

## Mar 27, 2023

### Attendees
- kody-kimberl
- Sajay Antony
- Yi Zha
- Feynman Zhou
- Billy Zha
- Patrick Zheng
- Pritesh 
- Shiwei Zhang
- Vani Rao
- ToddySM

### Agenda Items

- Call-out: Speed up PRs review for notation RC-4.
    - [documentation PRs](https://github.com/notaryproject/notaryproject.dev/pulls?q=is%3Apr+is%3Aopen+label%3Areview)
- Vote for flag name, PR https://github.com/notaryproject/notation/pull/601 (Yi)
- Open discussion: Two-factor auth for everyone in the Notary project org
- Possibility to grant `triage` access to "notation-roadmap-maintainers" in the Notation repo (Feynman)
- Notary security audit meeting will be started at 8:00 AM PST Mar 28 according to the Poll (Feynman)

### Meeting notes

- Let's speed up the PR review for RC-4 release.
- We had a discussion on the names, and the next step is to add naming options in PR https://github.com/notaryproject/notation/pull/601, then we will vote for the name later. Some options discussed during the meeting:
    - `--path`, `file://./`, `--oci-dir`, `--use-oci-layout`, `--target-path`, `--offline`, `-- dirpath`
- No objections to enabling two-factor auth for everyone in the notary project org
- We will see in the future whether there is a need to grant `triage` access to Notation related code repositories for other contributors.

## Mar 20, 2023

### Attendees
- Yi Zha
- Feynman Zhou
- Pritesh
- Samir Kakkar
- Patrick Zheng 
- Shiwei Zhang
- Sajay Antony

### Agenda Items

- Governance issues (Yi)
    - Governance doc: https://github.com/notaryproject/.github/issues/7
    - GitHub teams: https://github.com/notaryproject/.github/issues/14
    - CNCF maintainers list: https://github.com/notaryproject/.github/issues/3
    - Fix Notary v2 references: https://github.com/notaryproject/roadmap/issues/89
- Recommended changes to Adam and Feynman on the [Fuzz Security Audit Blog](https://github.com/notaryproject/notaryproject.dev/pull/152) (Vani)
- Healthcheck on the RC-4 release milestone (Vani)
- Request review on the [Notary doc and blog PRs](https://github.com/notaryproject/notaryproject.dev/pulls?q=is%3Apr+is%3Aopen+label%3Adocumentation) (Feynman)

### Meeting Notes
- Governance doc: https://github.com/notaryproject/.github/issues/7
    - We reached consensus on [comment](https://github.com/notaryproject/.github/issues/7#issuecomment-1476143560), and the next steps:
        - Create a PR to copy governance docs from `notary` repo to `.github` repo
        - Create another PR to amend the governance doc based on the needs if any
        - Align with `notary` repo maintainers about removing those gov docs in `notary` repo
- GitHub teams
    - We reached consensus on [comment](https://github.com/notaryproject/.github/issues/14#issuecomment-1473032128), and the next step is to take actions accordingly
- CNCF maintainers list
    - We reached consensus on [comment](https://github.com/notaryproject/.github/issues/3#issuecomment-1477138473), and the next step is to take actions accordingly
- Fix Notary v2 references
    - We reached consensus as [comment](https://github.com/notaryproject/roadmap/issues/89#issuecomment-1477157871), we will start working on the following issues first:
        - notation#586, notation-go#287, notation-core-go#127, meeting-notes#15
- Fuzz Security Audit Blog
    - Follow up with Vani when she is online
- Update RC-4 release status
    - Features in the scope are still WIP.
- Call-out for the review of Notary doc and blog PRs, the fuzz security audit blog need to be reviewed ASAP.

## Mar 13, 2023

### Attendees:

- Yi Zha
- Feynman Zhou
- Toddy SM 
- Patrick Zheng 
- Shiwei Zhang
- Vani Rao
- Pritesh 
- Sajay Antony

### Agenda Items:
- CNCF Annual Review
    https://github.com/cncf/toc/issues/1018 (Toddy)
- Update references from Notary v2 to Notation, see aggregated issues https://github.com/notaryproject/roadmap/issues/89 (Yi)
- Timing for the Notary meeting after the time change as of 03/12/2023 (Vani)
- Before investing too much time, approve the PR https://github.com/notaryproject/notation-core-go/pull/128 to ensure we agree on the approach (Vani)
- Heads-up: 3 weeks left for notation RC-4 releases, see [RC-4 board](https://github.com/orgs/notaryproject/projects/10/views/29) (Yi)
- Notary fuzzing test blog and report are in reviewing and will be released this Thursday (Feynman)
-  Governance work items (Toddy)
    -  https://github.com/notaryproject/.github/issues/3
    -  https://github.com/notaryproject/.github/pull/5
    -  https://github.com/notaryproject/roadmap/pull/85
    -  Branch naming conventions
    
### Meeting Notes:

- CNCF Annual Review
    - Feynman will help to drive the content preparation
    - Lachie will help to confirm the timeline.
- The notary meeting Monday series start from 5 pm to 6 pm pacific time since Mar 12
- Yi shared there will be more issues to be submitted to address other governance issues including project review cadence, branch strategies and etc.
- The license of https://pkg.go.dev/github.com/cloudflare/cfssl/revoke is good per 
foundation/allowed-third-party-license-policy.md at main · cncf/foundation (github.com)
- Lachie will help to follow up the go-cose license. We may need to file an exception 
https://github.com/cncf/foundation/blob/main/license-exceptions/cncf-exceptions-2019-11-01.json
- Fuzzing testing Report and blog 
    - Review the reports and blogs
    - Recommend to store the reports under Notary project repo with this folder structure: `security/reports/fuzzing-test`
- Still waiting for comments from current org maintainers, suggest waiting until Mar 16, and then take actions on https://github.com/notaryproject/.github/issues/3 on Thursday.
- Agreed to merge PR with enough approvals and no unresolved comments: https://github.com/notaryproject/.github/pull/5

## Mar 6, 2023

### Attendees:
- ToddySM 
- Vani Rao 
- Yi Zha
- Feynman Zhow 
- Agam Dua
- Byron Chien
- Pritesh Bandi
- Patrick Zheng

### Agenda Items:
- CNCF TOC Issues (ToddySM)
    - https://github.com/notaryproject/notaryproject/issues/245
    - https://github.com/notaryproject/notaryproject/issues/244
- Vote for [Notation CLI v1.0.0-rc.3 release](https://github.com/notaryproject/notation/issues/582) (Yi)
    - Not recommended new releases for `notation-go` and `notation-core-go`, since the recent changes were trivial.
- Feature demo: sign and verify local artifacts (Patrick Zhang)
    - See [demo steps and asking for feedback](https://github.com/notaryproject/notation/discussions/581)

### Meeting Notes:
- Open discussion on CNCF TOC Issues (ToddySM)
    - https://github.com/notaryproject/notaryproject/issues/245
    - https://github.com/notaryproject/notaryproject/issues/244
- Agreed on only releasing Notation CLI v1.0.0-rc.3, and try the best including [PR579](https://github.com/notaryproject/notation/pull/579)
- Hot discussions on the demo, some notes taken, we will continue working on the scenarios, and polishing the solution
    - The output message need to be improved to show useful information to users, and also considering JSON output that can be parsed easily
    - How to ceate OCI layout?
    - If the image was already built using `docker build` locally, can user sign it directly? Probably not, because it's not possilbe to get the descriptor. OCI layout is a standard format. 
    - Consider using `docker buildx --metadata-file` as input 
    - Local verification is not important for K8S
- Fuzzing test blog post includes report is started and will be available next week (Feynman)## Mar 2, 2023

### Attendees:

### Agenda Items:

### Meeting Notes:

## Feb 27, 2023

### Attendees:
 - ToddySM 
 - Vani Rao 
 - Yi Zha
 - Feynman Zhow
 - Agam Dua
 - Byron
 - Derek McGowan
 - Junjie Gao
 - Lachlan Evenson 
 - Manas Sivakumar
 - Patrick Zheng
 - Pritesh
 - Samir Kakkar
 - Shiwei Zhang
 - Sajay Antony

### Agenda Items:
- Walk through rc-3 work items based on proposal https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ?view, any clarifications or blockers. (Vani) 
- Revocation Spec review between Pritesh and Shiwei, if any pending work needed. (Vani)
- Will existing tools/mechanisms that customers use today to move images from development-> Staging -> Production repositories. What are our thoughts from Notation community ? (Vani/Samir)
- OCI changes on standardazing on Image Manfiest to support artifact scnearios [Yi]
   - [manifest: provide guidance on SCRATCH config descriptor](https://github.com/opencontainers/image-spec/pull/1023)
   - [manifest: clarify that layers is technically OPTIONAL](https://github.com/opencontainers/image-spec/pull/1016)
   - [Remove artifact manifest](https://github.com/opencontainers/image-spec/pull/999)
- Finalize the RC.2 release notes [PR](https://github.com/notaryproject/roadmap/pull/87) and announcement blog [PR](https://github.com/notaryproject/notaryproject.dev/pull/141) (Feynman)
- Homebrew installation for macOS will be deferred to v1.0.0, see [#431](https://github.com/notaryproject/notation/issues/431), [#571](https://github.com/notaryproject/notation/issues/571) (Feynman)


### Meeting Notes:
- Welcome Manas joining the meeting
- Certificate Revocation
    - AP: Pritesh to provide an update version for review on Mar 14
    - AP: Prtiesh to create issues for implementation (Pritesh: [issues](https://github.com/notaryproject/roadmap/issues/60#issuecomment-1447369802))
- Left works for governance work
    - Branch policies
    - GitHub Teams
    - Security policy: create one under .github, and referred by other sub-repos
    - AP on Feynman to create the issue for submitting Maintainers to CNCF maintainer list
- Discussed the tools used for move images and associated signatures between registries.
    - oras is the tool to copy images across registries, oras also support recursive copy that signatures associated with images can be copied at the same time.
- Discussed signature deletion
    - ORAS can be used to delete signatures. ORAS also provides option that when deleting images, the artifacts subject to images can be deleted at the same time.
    - Should Notation support deleting signatures without asking users to use ORAS? 
- AP on Samir to clarify the scenarios for signature deletion and image copy, create issues in ORAS project if needed.
- Discussed signature filtering, need to clarify what filtering is about
    - Pritesh: we also talked about filtering artifact in oras move command. 
- Agree on changing the default behavior to use image manifest storing signatures, AP on Yi to create an issue for it
- Need to re-visit the release goal for rc.3, AP on Vani and Yi
- Discussed Mac OS installation experience

## Feb 20, 2023

### Attendees:
- Yi Zha (MSFT)
- Feynman Zhou (MSFT)
- Agam Dua (containerd)
- Junjie Gao (MSFT)
- Patrick Zheng (MSFT)
- Pritesh Bandi (AWS)
- Vani Rao (AWS)
- Byron Chien (AWS)
- Shiwei Zhang (MSFT)

### Agenda Items:
- Gratitude: BIG THANK to all of you for the contribution to RC-2 Release (Yi)
- Kick off RC-3 development (Yi)
    - Chore: Clean up the project board
    - Missing issues or some issues requires break-down
- Apply for approvals on merging the [new website PR](https://github.com/notaryproject/notaryproject.dev/pull/110) and push it to production, see [preview](https://deploy-preview-110--notarydev.netlify.app/) (Feynman)

### Meeting Notes:
- Welcome and show gratitude on rc-2 release
- Walk through rc-3 work items based on [proposal](https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ?both#RC-3-Release-Items---April-10th-2023-Can-be-called-GA-----Gives-5-weeks-after-rc-2-release), ACTIONS required for below items and reflecting them in project board.
    - missing issues for what to be done in rc.3
        - Improve Error Message for Notation CLI
        - Support TSA (TimeStamp Authority) trust stores in trust policy
        - Removing unwanted signature from signed images
        - configuration improvement
        - installation improvement
        - Sign/verify offline artifacts
    - issues need to break-down to fit into rc.3 timeline
        - Security (besides security poliy, more issues could come up after security audit)
        - [Multiple Signature verification](https://github.com/notaryproject/roadmap/issues/22)
    - More issues to be added
        - [Improve Notation authentication experience](https://github.com/notaryproject/notation/issues/503)
        - Documentation work, see [board](https://github.com/orgs/notaryproject/projects/10/views/30)
            - Could reference CLI spec, but missing document for E2E user guides
- Showed a [preview](https://deploy-preview-110--notarydev.netlify.app/) of new website, confirmed the logo and looking for LGTM to [website PR](https://github.com/notaryproject/notaryproject.dev/pull/110)

## Feb 16, 2023

### Attendees:

### Agenda Items:
- Conclude if RC-2 is a good release to consider for Notation GA and decide on RC.3 release items  status check. (Vani)
    - Refer to the following link - https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ?both
- Yi to provide what is the progress on the draft version of Threat model and start the review process.(Vani)
- Feynman to see if any open item for Security Audit Introductory Meeting  (Yi) 

## Feb 13, 2023

### Attendees:
- Samir Kakkar
- Vani Rao

### Agenda Items:
- RC.2 release status check-in. (Vani)
- Status of the request for the Notary website. (Vani)
- Feynman to share the latest status on the potential issues when integrating to Docker Hub and Ratify.(Vani)


### Meeting Notes:
- Website: requests final review on Notary website, Vani mentioned the logo of AWS is approved conditionally based on the verbiage used above the logo.
- rc.2: rc.2 release will be announced as of 02.16.
- rc.2: Pritesh/Vani shared test results for notation rc.2 dev build. There are potential issues when itegrating to Docker Hub and Ratify, need to follow it up.

## Feb 13, 2023

### Attendees:
- Yi Zha
- Vani Rao
- Agam Dua
- Pritesh 
- Derek McGowan
- Patrik Zheng
- Shiwei Zhang
- Lachlan Evenson 
- Feynman Zhou
- Junjie Gao
- Ziwen Ning 
- Ramkumar Chinchani
- Sajay Antony

### Agenda Items:
- RC.2 release status check-in
- Fuzz testing: This kind of issue (issue [#276](https://github.com/notaryproject/notation-go/issues/276)) and fix (PR [#275](https://github.com/notaryproject/notation-go/pull/275) and [PR#550](https://github.com/notaryproject/notation/pull/550)) should go through the [GitHub Security Advisories](https://docs.github.com/en/code-security/security-advisories/repository-security-advisories/about-repository-security-advisories) feature (Shiwei)
    - Define impact scope
    - Give credit to the reporters
    - Discuss, fix, and publish **privately**
    - Examples:
        - oras-project/oras: [Tarballs with links can escape working directory upon extraction ("zip slip")](https://github.com/oras-project/oras/security/advisories/GHSA-g5v4-5x39-vwhx)
        - moby/moby (a.k.a. docker/docker): [Ambiguous OCI manifest parsing](https://github.com/moby/moby/security/advisories/GHSA-xmmx-7jpf-fx42)
- Looking for explicit approval or LGTM (Yi)
    - Maintainers PRs, see [list](https://cloud-native.slack.com/archives/CQUH8U287/p1675899029597369)
    - Branch policies issues, see [list](https://cloud-native.slack.com/archives/CQUH8U287/p1675900129338429)
- Info: Work items organizaztion and clean-up by Vani and Yi (Yi)
    - Track status easily in project board
    - Use Roadmap repo for roadmap features and breakdown in the individual repositories accordingly
- A draft version of Threat model is under preparation using the tool [OWASP Threat Dragon](https://threatdragon.github.io/home). Any comments? Suggest to create a directory named `threatmodels` under notaryproject folder to store related files.(json files for models, and pdf for report) (Yi)
- Final review on the new [Notary website](https://) and confirm the release 
- Collaborating on Notation v1.0.0-RC.2 blog post
- Short introduction to the CNCF LFX mentoring program 
- OCI changes on standardazing on Image Manfiest to support artifact scnearios [@sajay]
   - [manifest: provide guidance on SCRATCH config descriptor](https://github.com/opencontainers/image-spec/pull/1023)
   - [manifest: clarify that layers is technically OPTIONAL](https://github.com/opencontainers/image-spec/pull/1016)
   - [Remove artifact manifest](https://github.com/opencontainers/image-spec/pull/999)
     
### Meeting Notes:
- Welcome new participant Ziwen Ning
- JSON output: Need to create spec for JSON output. Pritesh to create a PR to remove misaligned code for merged PR
- Document: To create user guides for new notation commands
- rc.2: Feynman shared test results for notation rc.2 dev build. There are potential issues when itegrating to Docker Hub and Ratify, need to follow it up.
- rc.2: Based on current PR status, rc.2 will be delayed to 2/15/2023.
- Fuzzing test: fix the bugs in rc.2 and document on both notary website and Github. The security policy will be fixed after maintainer goverance issues are taken cared of.
- Goverance: We are ready to merge once we have 2/3 of the Notary org maintainer +1
- threatmodel: Yi is working on a draft version of threat model for review and further discussion.
- Security Audit: Feynman to update the security aduit meeting since next Monday is holiday in US.
- Website: requests final review on Notary website, Vani mentioned the logo of AWS is wrong, which should be fixed.
- OCI changes: move this topic to 2/27/2023

## Feb 9, 2023

### Attendees:
- Agam Dua (containerd)
- Derek McGowan (containerd)
- Toddy Mladenov (msft)
- Vani Rao (aws)

### Agenda Items:
- GitHub Action for Notary (ToddySM)
- Maintainers PRs (ToddySM)
- Branch policies work items (ToddySM)
- rc.2 release status (VaniRao)
    - Merge and close all the open PRs by EOD.
    - Do the basic sign and verify functions prior to the release.
    - Release date to be moved from 02/09 to 02/13.
- Need to plan to cut a DEV build by EOD on 02/09 or latest by 02/10 morning. (VaniRao)

### Meeting Notes:
- RC.2 there are some PRs remaining to be closed today but we agreed to move the RC.2 release to 2/13/2023 (Monday)
    - Get DEV build by EOD today 2/9 to give to Jimmy for Ratify
    - Agreed to move the RC.2 release to 2/13
    - As a result of this we may need to shuffle some of the RC.3/release items. Targeted RC.3 April 3rd 2023
    - Need to cleanup the RC.2 board
    - For the release milestone we should only do security fixes 
- For the GitHub Action for Notation the proposal is to create a separate repository and give Joshua access to it. Will need to go over the process for adding CODEOWNERS and MAINTAINES. Toddy to comment on the issue https://github.com/notaryproject/notation/issues/544 with the proposal and tag Joshua. 
- ContainerD may be interested in using the Notation CLI. They are trying to learn about Notary
- Ask from Toddy - organize and clean up the work items and use the roadmap one for uber-items and breakdown in the individual repositories. Else it is hard to find items

## Feb 6, 2023

### Attendees:

- Vani Rao (AWS)
- Pritesh Bandi(AWS)
- Toddy Mladenov (Microsoft)
- Patrick Zheng (Microsoft)
- Feynman Zhou (Microsoft)
- Shiwei Zhang (Microsoft)
- Yi Zha (Microsoft)
- Byron Chien (AWS)
- Junjie Gao (Microsoft)
- Derek McGowan (ContainerD)
- Agam Dua (ContainerD)


### Agenda Items:

- rc.2 release status check-in, see [summary](https://github.com/notaryproject/notaryproject/discussions/238) (Yi)
- Finalize rc.3 [scope](https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ#RC-3-Release-Items---MAR-13th-2023-Call-be-called-GA---Gives-5-weeks-after-rc-2-release) (Yi)
    - New work items: Fuzzing test and security audit support 
- `.github` repo PRs and work (ToddySM)
    - https://github.com/notaryproject/.github/pull/1
    - https://github.com/notaryproject/.github/issues/2
- Repo maintainers PRs (ToddySM)
- Submitted a [ticket](https://cncfservicedesk.atlassian.net/servicedesk/customer/portal/1/CNCFSD-1580) on CNCF Service Desk for requesting a Security Audit (Feynman) 
- Idea for improving the Notation KMS plugin ecosystem and experience (Feynman)

### Meeting Notes:

- Notation rc.2 release will be delayed to Feb 9, 2023
- It is decided to use flag name `--signature-manifest` with two options WRT to flag name for support OCI image manifest
Current votes for maintainers:
As of 3:30 PM Feb 6th, 2023
	• https://github.com/notaryproject/notation
		○ Jinjie Gao (MSFT) - 5 approvals (1 AWS, 1 Independent, 3 MSFT)
		○ Patrick Zheng (MSFT) - 6 approvals (1AWS, 1 independent, 4 MSFT)
		○ Shiwei Zhang (MSFT) - 7 approvals (2 AWS, 1 independent, 4 MSFT)
		○ Pritesh Bandi (AWS) - 8 approvals (1 independent, 7 MSFT)
		○ Milind Gokarn (AWS) - 8 approvals (1 AWS, 1 independent, 6 MSFT)
		○ Rakesh Gariganti (AWS) - 8 approvals (1 AWS, 1 independent, 6 MSFT)
		○ Yi Zha (MSFT) - 9 approvals (2 AWS, 1 independent, 6 MSFT)

Not balanced 4 MSFT, 3 AWS

	• https://github.com/notaryproject/notation-core-go
		○ Jinjie Gao (MSFT) - 4 approvals (1 AWS, 3 MSFT)
		○ Patrick Zheng (MSFT) - 4 approvals (1 AWS, 3 MSFT)
		○ Shiwei Zhang (MSFT) - 6 approvals (2 AWS, 4 MSFT)
		○ Pritesh Bandi (AWS) - 5 approvals (5 MSFT)
		○ Milind Gokarn (AWS) - 5 approvals (5 MSFT)
		○ Rakesh Gariganti (AWS) - 5 approvals (5 MSFT)
	• https://github.com/notaryproject/notation-go
		○ Jinjie Gao (MSFT) - 4 approvals (1 AWS, 3 MSFT)
		○ Patrick Zheng (MSFT) - 5 approvals (1 AWS, 4 MSFT)
		○ Shiwei Zhang (MSFT) - 6 approvals (2 AWS, 4 MSFT)
		○ Rakesh Gariganti (AWS) - 8 approvals (2AWS, 6 MSFT)
		○ Milind Gokarn (AWS) - 9 approvals (2 AWS, 7 MSFT)
		○ Pritesh Bandi (AWS) - 7 approvals (1 AWS, 6 MSFT)
	• https://github.com/notaryproject/notaryproject
		○ Yi Zha (MSFT) - 0 approvals
		○ Toddy Mladenov (MSFT) - 0 approvals
		○ Feynman Zhou (MSFT) - 4 approvals (2AWS, 1 independent, 1 MSFT)
		○ Shiwei Zhang (MSFT) - 4 approvals (1 AWS, 1 independent, 2 MSFT)
		○ Vani Rao (AWS) - 5 approvals (1 AWS, 1 independent, 3 MSFT)
		○ Milind Gokarn (AWS) - 6 approvals (2 AWS, 1 independent, 3 MSFT)
		○ Pritesh Bandi (AWS) - 4 approvals (1 AWS, 1 independent, 2 MSFT)

Not balanced 4 MSFT, 3 AWS

	• https://github.com/notaryproject/notaryproject.dev
		○ Yi Zha (MSFT) - 0 approvals
		○ Toddy Mladenov (MSFT) - 0 approvals
		○ Feynman Zhou (MSFT) - 1 approvals (1 MSFT)
		○ Vani Rao (AWS) - 3 approvals (1 AWS, 2 MSFT)
		○ Samir Kakkar (AWS) - 3 approvals (1 AWS, 2 MSFT)
		○ Pritesh Bandi (AWS) - 2 approvals (2 MSFT)
	• https://github.com/notaryproject/roadmap
		○ Yi Zha (MSFT) - 0 approvals
		○ Toddy Mladenov (MSFT) - 1 approvals (1 MSFT)
		○ Feynman Zhou (MSFT) - 1 approvals (1 MSFT)
		○ Vani Rao (AWS) - 2 approvals (2 MSFT)
		○ Samir Kakkar (AWS) - 2 approvals (2 MSFT)
		○ Pritesh Bandi (AWS) - 2 approvals (2 MSFT)
	• https://github.com/notaryproject/meeting-notes
		○ Yi Zha (MSFT) - 0 approvals
		○ Toddy Mladenov (MSFT) - 0 approvals
		○ Feynman Zhou (MSFT) - 1 approvals (1 MSFT)
		○ Vani Rao (AWS) - 3 approvals (1 AWS, 2 MSFT)
		○ Samir Kakkar (AWS) - 3 approvals (1AWS, 2 MSFT)
		○ Pritesh Bandi (AWS) - 2 approvals (2 MSFT)


## Jan 30, 2023

### Attendees:
- Vani Rao (AWS)
- Byron Chien (AWS)
- Samir Kakkar ( AWS)
- Pritesh Bandi(AWS)
- Sajay Antony (Microsoft)
- Toddy Mladenov (Microsoft)
- Patrick Zheng (Microsoft)
- Feynman Zhou (Microsoft)
- Junjie Gao (Microsoft)
- Shiwei Zhang (Microsoft)


### Agenda Items:
- Confirm the RC.3 scope based on available engineering resources and [implementation cost](https://github.com/notaryproject/notaryproject/discussions/218#discussioncomment-4820383) - Feynman
- Sync up the development status of the new Notary website landing page, see [PR](https://github.com/notaryproject/notaryproject.dev/pull/110) and [preview link](https://deploy-preview-110--notarydev.netlify.app/). Jesse will help us to create a demo video - Feynman
- Gather project proposals for [CNCF LFX Mentorship program](https://github.com/cncf/mentoring/tree/main/lfx-mentorship/2023/01-Mar-May). Potential proposals include but not limited to HashiCopr Vault plugin, Notary Documentation - Feynman
- RC.2 status check-in
- Governance work items - Toddy
    - Creation of `.github` repo
    - CODEOWNERS and MAINTAINERS files
    - Branch policies
- Streaming the recordings to YouTube - Toddy
- PRs pending review
    -  [fix: Appends annotations returned by plugin to signature manifest's annotations #253](https://github.com/notaryproject/notation-go/pull/253)
    -  [Adds example of remote key in signingkeys.json & Rewords verify notation checksum section #126](https://github.com/notaryproject/notaryproject.dev/pull/126)
    -  [Adds signingkeys.json validation check #246](https://github.com/notaryproject/notation-go/pull/246)
    -  [ chore: improve warning message when signing or verifying with tag #497 ](https://github.com/notaryproject/notation/pull/497) (Good to have)

### Meeting notes

- Confirmed Feb 1 as the date for code freezing and cut a dev build release for testing
- Walked through the RC.3 scope at [Vanin's proposal](https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ#RC-3-Release-Items---MAR-13th-2023-Call-be-called-GA---Gives-5-weeks-after-rc-2-release)
- Samir will discuss the [Multiple signature verification](https://github.com/notaryproject/roadmap/issues/22)
- Sajay will check the Ratify RC.1 status
- Toddy will create `.github` repo and migrate the governance guide to a central place
- Feynman and Patrick will review the RC.2 PRs

## Jan 26, 2023

### Attendees:
- Vani Rao (AWS)
- Toddy Mladenov (Microsoft)

### Agenda Items:
- Release goals
- Governance items (may need to move to next meeting if not enough quorum)
    - Creation of `.github` repo
      https://github.com/notaryproject/roadmap/issues/77
    - Updating CODEOWNERS and MAINTAINERS files in each repo
      https://github.com/notaryproject/notation/issues/514
      https://github.com/notaryproject/notaryproject.dev/issues/127
      https://github.com/notaryproject/notation-core-go/issues/106
      https://github.com/notaryproject/notation-go/issues/249
      https://github.com/notaryproject/notaryproject/issues/224
      https://github.com/notaryproject/notary/issues/1665
      https://github.com/notaryproject/roadmap/issues/78
      https://github.com/notaryproject/tuf/issues/34
      https://github.com/notaryproject/meeting-notes/issues/5

### Notes:
- We need to have a build on 1/31 so we can give to Jimmy to do the testing for Ratify. 
    - We want to make sure that there are no surprises for the fallback
    - We need to start the PR reviews ASAP so that we can 
- For the release goals
    - By March first week we need to have V1 to have the release to get feedback from customer

## Jan 23, 2023

### Attendees:
- Vani Rao (AWS)
- Pritesh Bandi (AWS)
- Toddy Mladenov (Microsoft)
- Sajay Antony (Microsoft)
- Feynman Zhou (Microsoft)

### Agenda Items:
- Followup governance improvements (https://hackmd.io/@toddysm/S19ygj2qs)
    - Where are we? can we have something for short term like restrict permissions and provision for security issue?
- Notation roadmap review
    - https://github.com/notaryproject/notaryproject/discussions/218
    - https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ
- Notation release manager and meeting chair rotation 
- Notation documentation delivery plan

### Notes:
- Followup governance improvements agreement is to:
    - Start with PRs for the governance documents and make them more visible - @toddysm and @pritesh to collaborate on those and tag the maintainers
    - We need to create a security policy to describe the process for filing and handling the security issues with the project - @toddysm to drive that
    - We need to file issues for nominating the maintainers. The process we will follow is: 1. File issues with nominations 2. Community votes on the nominations/discusses the nominations 3. Current maintainers need to vote on the nominations 4. Nominations are accepted by super majority vote from the maintainers (as per current governance)
- RC.2 readiness
    - Reviews of the PRs will happen after folks in China come back from vacation. Once those are reviewed, we are ready for RC.2 release
    - Also working with Ratify on testing Ratify with the latest RC.2 release
    - Ratify question: What is the impact on Ratify if Notation supports using OCI image manifest to store signatures in registries that partially implement the OCI Image specification v1.1. Notation Sign command will have a new flag --image-spec v1.1-image to force Notation to store the signatures using OCI image manifest.
        - If there is a impact for Ratify what is the plan to make the changes and how are we going to prioritize that in Ratify community. Can it be ready by Feb 6th ?  
- Notation release schedule
    - To be able to do the prioritization we agreed that we need to confirm the available engineering resources for RC.3 and have a high-level (T-shirt sizing) for each item in the RC.3 items (https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ)
    - We need to add Security Review in the list of items before release (RC.3, RC.4, or GA)
    - We should align the goals for RC.3 before selecting the RC.3 items


## Jan 17, 2023

### Attendees
- Vani Rao (AWS)
- Samir Kakkar ( AWS)
- Pritesh Bandi(AWS)
- Jesse Butler (AWS)
- Sajay Antony (Microsoft)
- Toddy Mladenov (Microsoft)
- Patrick Zheng (Microsoft)
- Feynman Zhou (Microsoft)
- Junjie Gao (Microsoft)



### Agenda Items
- Go through the Notation automatic fallback solution
- Notation RC.2 status check-in, see [first section](https://github.com/notaryproject/notaryproject/discussions/218) and confirm an ETA date
- Notation roadmap review
    - https://github.com/notaryproject/notaryproject/discussions/218
    - https://hackmd.io/WVFhrhvYSFutJpnY6JTDuQ
- Notation release manager and meeting chair rotation 
- Notation documentation delivery plan

### Meeting notes

- Based on the development and PR review status, RC.2 will be deferred to Feb 6. Vani and Samir will drive this release
- "OCI manifest fallback solution" will be split into two phases:
    - Using a flag to specify the manifest pushing behavior. It will not support the "hybrid situation" like Docker Hub. It requires to change the CLI spec to define the CLI UX (RC.2)
    - Using manual configuration file per registry, need to raise an issue to track and design the configuration options (RC.3)
- Opened issue based on discussion
  - [[RC2] Fallback updates for Sign operation](https://github.com/notaryproject/notaryproject/issues/219)
  - [[RC2] Fallback updates for Verify operation](https://github.com/notaryproject/notaryproject/issues/220)
  - [Define scenarios for movement/replication of signatures between registries](https://github.com/notaryproject/notaryproject/issues/221)

## Jan 12, 2023

### Attendees
- Ivan Wallis (Venafi)
- Pritesh (AWS)
- Sajay Antony (Microsoft)
- Toddy Mladenov (Microsoft) - chairing

### Ageda Items
- Notary project governance improvements (proposal pre-read https://hackmd.io/@toddysm/S19ygj2qs)
    - Discussed comments from Pritesh (Toddy to add clarifications)
    - Need more feedback from the community (Toddy to solicit feedback offline and bring agian for discussion in a week)
- Release timelines
    - Postponed to next week's meeting due to the lack of quorum
- Ivan wanted feedback on https://github.com/notaryproject/notation-go/issues/220
    - Pritesh provided some suggestions. Please add suggestions to the issue

## Jan 9, 2023

### Attendees
- Toddy Mladenov
- Yi Zha
- Shiwei Zhang
- Patrick Zheng
- Pritesh 
- Feynman Zhou
- Vani Rao
- Junjie Gao
- Nima Talebi
- Sajay Antony
- Samir Kakkar
- Byron

### Agenda Items
- Notation v1.0.0-rc.2 release status check-in (Yi)
    - OCI image support
    - Notation inspect
    - Metadata support
    - sematic versioning
    - E2E testing (framework+sign/verify+TP) -- PR reviewing
    - debug logs for all CLI commands -- done 
    - spec for CLI to manage trust policy
- Automatic fallback support logic in ORAS CLI to be considered in Notation CLI (why and why not) (Vani)
- Notation Inspect
    - Can Inspect inspect a specific signature. No as of now (Vani)
    - Any use case scenario for executing the LIST command and retriveing one of the signature to perform the Inspect ? (Vani) 
-  Here are 3 options so far for inspect output to decide on: (Vani)
    - -o, --output json
    - `--display {tree, json) by default tree
    - --json (an example in https://clig.dev/#output)
- notation inspect prints a tree view by default, which usually requires a wide screen. The screen size of a typical TTY is 80 x 24. How can the tree view fit the width of 80? (Vani)
- In inspect to describe the "media type", "digest" and "size", do we need to use the term 'payload' or 'target artifact' ? (Vani) 
- Revisit the date for rc-2 based on the discussion / changes and status today considering the rc-2 items. (Vani)

### Meeting Notes

- Vani and Samir will drive the solution of "Backward Compatibility" for Notation and will submit a doc for review
- Vani will create an issue to track the `notation inspect` to inspect a single signature.
- Use `--output` for `notation inspect` output
- The implementation of `notation inspect` will be moved to post-rc.2 release

## Jan 3, 2023

### Attendees
- Toddy Mladenov
- Yi Zha
- Shiwei Zhang
- Patrick Zheng
- Pritesh 
- Feynman Zhou
- Vani Rao
- Junjie Gao
- Nima Talebi
- Sajay Antony
- Byron


### Agenda Items
- Project status sync-up, see [project board](https://github.com/orgs/notaryproject/projects/10/views/22) (Yi)
- Status review for rc-2 dated for Jan 16th (Vani Rao)
- To do task list for the Fallback Support (Nima)
    - client-side code for setting the relationship between the artifact and the subject.  That’s handled by the oras-go library already.  
    - All notary needs to do is 
        - a) on failure after trying to push an artifact, to then try again, but this time create the manifest equivalent of the artifact manifest.  And 
        - b) comprehend that the referrers API is a thing, and then fall back to querying for the image manifest list/index instead.
- Update notation sign and verify spec for metadata - [notation/pull/498](https://github.com/notaryproject/notation/pull/498) (Byron)
- Collaborate on the Notary new year blog (Feynman)


### Meeting Notes
- Nima and Pritesh will update Notary v2 spec to support fallback solution and CLI spec
- We have less resources on the documentation. Vanin will confirm if she can find one maintainer for Notary documentation
- `Notation Inspect` is risky in RC.2. We need to review the status next Monday and determine if we could imlement it in RC.2
- Feynman will draft new year blog for Notary, the content structure will be similar to [this one](https://github.com/oras-project/oras-www/pull/75/files)
- Review a PR from Byron: Update notation sign and verify spec for metadata - [notation/pull/498](https://github.com/notaryproject/notation/pull/498)

