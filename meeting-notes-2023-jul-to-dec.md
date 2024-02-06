# Notary Project Meeting Notes from Jul 2023 to Dec 2023

## Dec 26 2023

Cancelled due to lack of topics and participants


## Dec 18 2023

### Attendees:

- Yi Zha (Microsoft)
- Junjie Gao (Microsoft)
- Shiwei Zhang (Microsoft)
- Feynman Zhou (Microsoft)
- Patrick Zheng (Microsoft)
- Rakesh Gariganti (AWS)
- Vani Rao (AWS)
- Rishab Semlani (AWS)
- Milind Gokarn (AWS)

### Agenda Items:

- Revising trust policies for blob signatures (Rakesh)

### Meeting Notes:
- The [proposal](https://hackmd.io/@-KPyDkW6QfGA-pldFa13pA/ByuHffALa) of revising trust policies was reviewed. In general, we are aligned to separate the trust policy file for blob and OCI image. We will have further discussion next week.

### Recording
- https://www.youtube.com/watch?v=9vHJccK2CJ4

## Dec 14 2023

### Attendees:
- ToddySM (Microsoft)

### Agenda Items:
- Meeting got cancelled due to lack of agenda and attendance

### Meeting Notes:

### Recording:


## Dec 11 2023

### Attendees:

- Yi Zha (Microsoft)
- David Dooling (Docker)
- Feynman Zhou (Microsoft)
- Toddy Mladenov (Microsoft)
- Junjie Gao (Microsoft)
- Patrick Zheng (Microsoft)
- Shiwei Zhang (Microsoft)

### Agenda Items:
- Notary Project org maintainers - open questions and proposals (ToddySM)
    - What is the total number of org maintainers we will have?
    - What is the agreed upon diversity of maintainers?
    - For the results of the voting, can we have a split: votes from current org maintainers and votes from current sub-project maintainers?
    - Proposal: Reach the total number of maintainers before making any other changes in the governance.
    - Proposal: Set a deadline by when the election should be done.

- Optional topic: [Notary Project issues and PRs status](https://hackmd.io/LkKAC-5hROeEwMOPNc_D3w) (Yi)

### Meeting Notes

- Due to lack of maintainers from different organizations, we did not discuss the topics in the agenda. These topics will be planned for discussion in Jan, 2024.
- We discussed Notation v1.1.0 release. Currently no features are ready. @yizha1 will follow it up to see whether we can have v1.1.0 release before end of 2023.

### Recording

https://www.youtube.com/watch?v=CJP9Zba3LxM

## Dec 7 2023

### Attendees:
- John Kjell
- Toddy Mladenov

### Agenda Items:
- Ad-hoc discussion

### Meeting Notes
- John was interested in the details of the signatures and the envelopes

### Recording
https://www.youtube.com/live/FtsYksy4J-Q?si=_NEDkoK3_iOqwipb 

## Dec 4 2023

### Attendees
- David Dooling (Docker)
- Feynman Zhou (Microsoft)
- Ivan Wallis (Venafi)
- Junjie Gao (Microsoft)
- Milind Gokarn (AWS)
- Niaz Khan (AWS)
- Patrick Zheng (Microsoft)
- Pritesh (AWS)
- Rakesh Gariganti (AWS)
- Sajay Antony (Microsoft)
- Samir Kakkar (AWS)
- Shiwei Zhang (Microsoft)
- ToddySM (Microsoft)
- Yi Zha (Microsoft)

### Agenda

- Notary Project review
    - Project health check
        - Adoption status, see [link](https://notaryproject.dev/docs/adopters/)
        - Maintainer and PR/issue status, see [link](https://hackmd.io/@yizha1/notaryproject-review)
    - Roadmap (This will be discussed at the community meeting next Monday, 12/11/2023) 

### Notes

- We shared current adoptors of Notary Project, and one improvement could be done is to add contact information to give more credits. @Feynman will help to create a PR
- The community has agreed to add new org maintainers. According to the [governance guide](https://github.com/notaryproject/.github/blob/main/GOVERNANCE.md), subproject maintainers are eligible for org maintainership. @yizha1 will create an issue and list data for all subproject maintainers to kick off the nomination process. Subproject maintainers can nominate themselves or be nominated by other maintainers. As per the governance document and alingment in the meeting, 2 out of 3 approvals from current org maintainers are required for new org maintainers. We will review the subproject maintainers’ status and nominations at the next Monday meeting.
- In the meeting, we also discussed some required updates on current governance document and other criterias to measure maintainer activities, @niazfk will create an issue to address updates on governance document. 

### Recording

- https://www.youtube.com/watch?v=a8DGHuu1Te8


## Nov 30 2023

### Attendees
- David Dooling
- ToddySM

### Agenda
- Ad-hoc

### Notes
- David and Toddy discussed Docker's plan to re-engage with the project.
- David and Toddy discussed the PR for adding Jonny as a maintainer to the `notary` sub-project and the challenges to merge that.
- Toddy encouraged David to attend Monday's meeting where the discussion of the Org Maintainers and the Governance will happen.

### Recording
https://www.youtube.com/live/pFODfdgJI1o?si=sOfXY2cmxRNKdJ6p

## Nov 26 2023

### Attendees:

- Yi Zha
- Feynman
- Samir
- Pritesh
- Toddy
- Patrick
- Junjie

### Agenda Items:

- Notary Project review meeting 12/4/2023 (Yi)
    - Participants
    - Proposal of Agenda
        - Project health check
            - Adoptions
            - Metrics for Project/Repos/issues/PRs
            - Maintainer status review
        - Roadmap and long term investiments

- Clean up issues and PRs (Yi)
    - https://github.com/orgs/notaryproject/projects/10/views/7

- Info: cooperation with Tanzu Application Catalog on Notation integration (Feynman)

### Notes

- Yi will send out a message in slack channel to invite maintainers to join the Notary Project review meeting
- Yi will create GitHub actions for `notation`, `notation-go` and `notation-core-go` repo to clean up stale issues and PRs automatcially.
- Feynman will document the scenarios of Tanzu integration with Notation, then we can review and plan features if needed

### Recording

https://www.youtube.com/watch?v=3xA4aflCGD8

## Nov 20 2023

### Attendees:
- Yi Zha
- Pritesh
- Feynman
- Shiwei
- Junjie
- Patrick

### Agenda Items:
- Should we continue Thursday's meeting there has been low attendence lately. (Pritesh)
- Noatoin v1.1.0 new date (Yi)
    - Sign arbitrary data
    - Plugin management
    - Error message improvements
    - Sign local container images (document containerd experience)
    - Improvements on trust store and trust policy management (move to v1.2.0)
- Plan for Notary Project retro and outlook meeting (Yi)
    - Date: 12/4/2024 community meeting
    - Topics:
        - Project health check: adoption, maintainer status, governance etc.
        - Upcoming releases and long term investiment

### Notes:
- [5 PRs](https://github.com/notaryproject/notaryproject.dev/pulls?q=is%3Apr+is%3Aopen+label%3Areview) on the website repo need review
- Pritesh will create a Poll in discussion of repo `.github` https://github.com/notaryproject/.github/discussions/new?category=polls to discuss whether we should cancel Thursday's meeting or not.
- New date for Notation v1.1.0 is 12/20/2023, and we will review the status on 12/11/2023

### Recording
https://www.youtube.com/watch?v=NQObc-C6keA

## Nov 16 2023

### Attendees:
- John Kjell
- Toddy Mladenov

### Agenda Items:
- Ad-hoc discussion how Notary Project and in-toto collaborate on attestations and signing

### Recording
https://www.youtube.com/live/ELHUnkA5k3M?si=0334GTxXDK4mzmxZ  

## Nov 13 2023

### Attendees:
- Yi Zha
- Feynman Zhou
- Shiwei Zhang
- Patrick Zheng
- Sajay Antony
- Pritesh
- Rakesh Gariganti
- Junjie Gao 
- Samir Kakkar
- _add yourself_

### Agenda Items:

- Status of major feature in Notation v1.1.0 (Yi)
    - Sign arbitrary data 
        - [Notation PR #811](https://github.com/notaryproject/notation/pull/811)
        - [Specification](https://github.com/notaryproject/specifications/pull/283)
    - Notation plugin management [PR #809](https://github.com/notaryproject/notation/pull/809)
    - Prioritize [Error message improvements](https://github.com/notaryproject/notation/issues/824) over "Simplify trust store and trust policy setup"
- Discuss how to effectively gather adopter information from the community based on CNCF TOC's [suggestion](https://github.com/cncf/toc/pull/1187). [Adding an adopter list](https://github.com/notaryproject/notaryproject.dev/pull/124) might be one of the appropriate options (Feynman)
- Preparation for Notary Project retrospective meeting (Yi)
    - Time: Proposal is community meeting on Dec 4 or Dec 11
    - Topics:
        - Project adoption, health, and maintainer satus
            - One input [Annual review summary and recommendations](https://github.com/cncf/toc/pull/1187)
        - Project charter and long term investiments

### Notes:
- Regarding "Sign arbitrary data"
    - We aligned on the flag name `--force` for overwritting existing signatures. 
    - The implementation is ready to go, @rakeshgariganti will come back with an ETA
- Yi will create an issue to track the CLI guideline
- Regarding "plugin management"
    - We aligned on `plugin install/uninstall` command, for `upgrade` since it requires spec changes and also there are some security concerns, it can be done in the 2nd itegration.
    - There are comments from Pritesh on install from url/file. @Feynman will drive further discussions to finalize the spec asap.
- We didn't have time to discuss other two topics

### Recording

https://www.youtube.com/live/nkRu1RGRfBI?si=LFclYA4f4P98KiMO


## Nov 6 2023

### Attendees
- Shiwei Zhang 
- Feynman Zhou
- Patrick Zheng
- Yi Zha
- _add_yourself_

### Agenda

- [Vote for Notation v1.0.1 release](https://github.com/notaryproject/notation/pull/820) (Yi)
- Notation v1.1.0 Feature status
    - Sign arbitrary data
    - plugin management
- Retrospective meeting (Yi)
    - Project Adoption and health
    - Project charter and long term investiments
    - [Annual review summary and recommendations](https://github.com/cncf/toc/pull/1187)
    - Governance related: 
- Governance PRs have been open for long time:
    - [Contributing guide](https://github.com/notaryproject/.github/pull/25)
    - [Repo lifecycle](https://github.com/notaryproject/.github/pull/37)
    - [Notation-go readme](https://github.com/notaryproject/notation-go/pull/343)
    - [Notation-core-go readme](https://github.com/notaryproject/notation-core-go/pull/158) 

### Notes
- Notation v1.0.1 release
    - update website banner and latest version to the installation guide
    - Update package manager, like Winget, brew
    - create a new PR to update release_management document for patch release workflow
- sign arbitrary data
    - Notation control the signature file name, for example, the name of the blob file
    - provide an option for users to specify the signature directory
    - if users sign the blob for the 2nd time, overwrite the existing signature by asking whether users is ok with it.
    - consider `cp` behavior for output file path resolution. 
        - Should notation create a fully nested path or not? 
        - If its directory then should we outupt {dir}/{pattern}.{ext} 
            - if not should we output the file to the output path and consider that its a fully qualified filename.
        - `cp` does not create nested paths so maybe to keep this consistent with other tools and avoid surprises notation could follow the same pattern of not creating nested paths. 
     -  Why do need to use the extension? 
         -  There are options like BOM, PE but this creates a perf issue 
         -  other tools might not interpret these signature files natively since those tools also need the same way to interpret this header https://github.com/microsoft/CoseSignTool
    - Notation plugin needs review from @samir/Pritesh. 
- Plugin management
    - We will not support plugin installers, which could be .exe, .msi binaries.
    - We can support installing a plugin binary itself
    - The checksum to verify is sha256
- Preparation for Notary Project retrospective meeting
    - Time:
        - Decemember (Samir)
    - Topics: 
        - Pritesh/Samir to suggest topics for this meeting
- Pritsh/Samir to review the governance related PRs

### Recording

https://www.youtube.com/watch?v=lcJ56sCTzqA

## Oct 30 2023

### Attendees
- Yi Zha
- Feynman
- Pritesh
- Junjie
- Patrick
- Rakesh
- Pritesh
- Sajay
- Toddy

### Agenda Items

- Notation v1.0.1 patch release (Yi)
    - `notation-core-go` v1.0.1 was released based on the vote.
    - Actions: 
        - [Vote for `notation-go`](https://github.com/notaryproject/notation-go/issues/360)
        - Review and merge [Notation CLI error message PR](https://github.com/notaryproject/notation/pull/810)
        - Create a new PR to update dependencies for Notation CLI
        - vote for Notation CLI release
- Blob Signing [PR comments](https://github.com/notaryproject/notation/pull/811#discussion_r1375853652) - Rakesh Gariganti
- Plan for retrospective meeting
    - Project Adoption and health
    - Project charter and long term investiments
    - [Annual review summary and recommendations](https://github.com/cncf/toc/pull/1187)
    - Governance basic: retro, contributing guide and so on
- Feature updates (Feynman)
    - Sign images before pushing to remote registries
    - Improvements on Plugin management
- Use dependabot to clean up stale PRs or issues on Notary Project Website.

### Notes

- @pritesh will review the noation PR and suggested to create updating deps PR in parallel
- @pritesh said maybe we can have a dedicated meeting for retro
- @pritesh / @rakeshgariganti will bring the repospective meeting plan to @Samir
- Blob signing, the decision is to use the file extension for different signature formats
- @rakeshgariganti will update/add the signature specification
- For signing local images, it is aligned that we document the new expericence for using experimental feature with containerd, no code changes for Notation 1.1.0
- Request further review on open questions for Notation plugin management

### Recording

https://www.youtube.com/watch?v=UEpNeJM--dk

## Oct 26 2023

### Attendees
- Sajay
- Samir
- Toddy

### Agenda Items

- Notation v1.0.1 patch release started, please maintainers click [this link](https://github.com/notaryproject/notation-core-go/issues/168) to Vote for `notation-core-go` v1.0.1 patch release first, later will start the vote for `notation-go`, then `notation` (Yi)
- Do we have any further questions on the [Notation plugin management (proposal)](https://hackmd.io/1nQa69DeROyqrO_IB5yGZQ?view)? Feynman will send a PR to update plugin spec this Friday.
- Question: will it be good to create a `Feature Design/Prototype Proposal` folder under the Specification repo and archive all proposals in a central place? Now they are under different maintainers' personal hackmd (Feynman)
- Info: Notary Project CNCF annual review 2023 has been merged by CNCF TOC. CNCF also provided valuable recommendations to us: https://github.com/cncf/toc/pull/1187. We need to discuss our actions based on their recommendations. (Feynman)
- 

### Notes
- Samir will work with Pritesh and Rakesh to get two more approvals for the patch release.
- For the [Notation plugin management (proposal)](https://hackmd.io/1nQa69DeROyqrO_IB5yGZQ?view) 
    - Samir will look at the MD and add comments
    - Sajay brought up the containerized scenario and the lack of diagnostics in the spec to troubleshoot issues in unattended runs (like in containers that are spawned automatically)
    - We can move to a PR to make sure that we can comment
- Samir, Sajay, Toddy don't have a good suggestion how to handle those.
    - Docs proposal folder may be a solution for that. For example for the CLI folder, we may have a docs folder and have all those specs there. @Feynman and @toddysm to come up with proposal by mid Nov 2023.
- Samir brought up the question about how to enable end users to attest for their usage/how is the end user adoptioin measured. For the next annual review, we should have a better way to report on end-user adoption (not only vendors).
    - Uber question: How the CNCF evaluate that end users are using the project? @Feynman to follow up with the TOC for suggestions.
- Overall discussion about project health
    - Regular retrospectives was brought up by @toddysm 
    - Bringing up the use cases up front would be helpful - Samir

### Recording
https://www.youtube.com/watch?v=pLjb6aJ0qoo

## Oct 23 2023

### Attendees:
- Yi Zha
- Feynman
- Toddy
- Sajay
- Rakesh
- Pritesh
- Shiwei
- Junjie
- Patrick
- Pablo

### Agenda Items:
- Request maintainers to review [Notation plugin management (proposal/spec)](https://hackmd.io/1nQa69DeROyqrO_IB5yGZQ?view) (Feynman)
- Question: will it be good to create a `Feature Design/Prototype Proposal` folder under the Spec repo and archive all proposals in a central place? Now they are placed in maintainers' personal hackmd (Feynman)
- Review the [Notation 1.0.1 patch release plan](https://github.com/notaryproject/notation/issues/804) (Yi)
- Status update on the [Notary Project Annual review](https://github.com/cncf/toc/pull/1187#pullrequestreview-1690530333) and next step (Yi)
- Sign Arbitrary Data, new flag vs command (Rakesh)
    - Disambiguate trust policy for oci vs arbitrary data.

### Notes

- Regarding reviewing spec of notaiton plugin management, we only covered reviewing the background and major scenarios. Request maintainers to continously offline review the specification. Questions from Toddy: how to upgrade Notation with existing plugins, how to use plugins from a different folder, how to brew install plugins
- Yi presented the Notation 1.0.1 patch release plan, and requested maintainers to review the scope and provide more comments by tomorrow.
- Rakesh presented the two proposals:
    - Use separated commands like sign-blob, verify-blob for signing arbirary data
        - Rakesh will investigate more and get back on whether other notaton commands also need a simliar blob command for example, inspect-blob.
        - Shiwei has a proposal of using a new command blob with different sub-commands, like notation blob sign,verify
    - Use a pattern in scope to differenticate oci registry and blob
        - Shiwei mentioned we should step up the version of trust policy
        - Notation should be backward compatibility to consume both old and new version of trustpolicies

### Recording

https://www.youtube.com/watch?v=pmUAnv1zQ3Q&t=7s

## Oct 19 2023

Cancelled

## Oct 16 2023

### Attendees
- Yi Zha
- Feynman
- Sajay
- Shiwei
- Patrick
- Junjie
- Pablo
- Toddy
- Pritesh

### Agenda

- Review spec for feature [sign images before pushing them to registries](https://hackmd.io/065j6_1HSM6K-lrTJeQyDg?view) (Feynman)
- Make contributions to promote Notary Project term and new experience, for example [Notation venafi-csp plugin](https://github.com/Venafi/notation-venafi-csp) (Yi)
    - [Use notation policy import command to import trust policies](https://github.com/Venafi/notation-venafi-csp/issues/10)
    - [Remove Notary v2 term used in the doc and code](https://github.com/Venafi/notation-venafi-csp/issues/9)
- Versioning of the documentation - proposal by Zach (ToddySM)
- Status check-in on the [v1.1.0 release](https://github.com/orgs/notaryproject/projects/10/views/7), if we have time (Yi)


### Notes
- Actions on spec for feature [sign images before pushing them to registries](https://hackmd.io/065j6_1HSM6K-lrTJeQyDg?view)
    - Feynman to update feasible solution based on the discussion during the meeting
    - The feasible solution has adoption issues since it requires customer to make other changes on build system besides using Notation, this need further discussion.

- @Feynman provide Zach the necessary permissions so that Zach can trying out the versioned documentation proposal.

### Recording
https://www.youtube.com/watch?v=a4suSC3KmYM

## Oct 12 2023
- Roseline Bassey
- Sajay Antony
- ToddySM
- Zach

### Agenda
- @Zach has a PR for a blog post that he wrote and linked the Tanzu
    - Blog PR https://github.com/notaryproject/notaryproject.dev/pull/356
        Asking for approval on this one so we can publish
    - Discussion for adding information to the docs https://github.com/notaryproject/notaryproject.dev/issues/342
        No PR available yet. Zach will start working on PR. We should break down on smaller PRs.
- @Zach raising the question about versioning of the docs when we have subsequent release of the Notary Project
    - Last time the conclusion was to have system releases (that consist of the following versions of the CLI, libraries, tools, etc.)
    - We have two options
        - Copy content in a new folder - easier but not so clean approach
        - Handle the content via branching - all work happens in the main branch and we cut a release branch and we publish version of the site for the release branch; this will require more work on the github and redirection on the site. 
            - We can cut a release for 1.0.0
            - We can create redirects
            - One issue is the blog posts - Zach will investigate how to overcome this one
            - @Zach will do the investigation by next Thu and we will bring to the Monday meeting after that
- @toddysm There is a maintainers meeting to approve the response for the security advisory today evening PT

### Recording
https://www.youtube.com/watch?v=NWvi_t2zPHM

## Oct 9 2023

### Attendees:
- Yi Zha
- Feynman Zhou
- Pritesh
- Toddy
- Sajay
- Shiwei
- Patrick
- Junjie

### Agenda Items:
- Review [Notary Project CNCF annual review document](https://hackmd.io/4TflOq8iSxqApi6Kx4WZjQ?view) (Feynman)
    - [PR](https://github.com/notaryproject/.github/pull/53) to update term in governance doc
- Review [spec](https://hackmd.io/ewbJr2ZnT4a8U1ObDVXcSw?view) of feature signing arbitrary  (Pritesh)
- Request community to review on updated [v1.1.0 milestone](https://github.com/orgs/notaryproject/projects/10) with priorities, status and assignees. (Yi)
- Protect the community meeting against Zoom bombing. Require only signed users participation. (ToddySM)

### Notes
- Maintainers to review https://github.com/notaryproject/notaryproject.dev/pull/357 which removed Docker adoption document, and added Harbor adoption
- Maintainers to review https://github.com/notaryproject/.github/pull/53, which update term in governance doc before 10/10/2023
- @pritesh and Samir to review the updated [v1.1.0 milestone planning board](https://github.com/orgs/notaryproject/projects/10).
- CNCF annual review document, @Feynman to resolve comments 
    - Overall comments on CNCF annual review: rework the background to focus on current Notary Project goals and activities.
    - Sajay suggested linking to the notary project overview is good enough instead of repeating the background info
    - Pritesh will add more comments after the meeting.
- Spec for signing arbitrary data
    - We are aligned on signature payload: "digest", "size" and "mediatype" (optional), @pritesh can start writing PR for signature payload spec
    - @yizha1 to update scenarios to make it clear especially on scenario "users distribute file and signatures via registry"
    - @pritesh to write PR for CLI spec for command line expereince, based on the discussoin, we perfer adding flags for sign and verify commands.
    - We discussed a bit of trust policy, and the proposal is to rename "registryScopes" to "Scopes". @yizha1 is good with the proposal, waiting for others' comments.
    - @pritesh requested further review on the specification.

### Recording

https://www.youtube.com/watch?v=Y2dWBjNId7w

## Oct 5 2023
- Meeting is cancelled as there was no else and no agenda items 

- sajay
- Zach
 
## Oct 2 2023

### Attendees:
- Pablo
- Pritesh
- Sajay Antony
- Samir Kakkar
- ToddySM

### Agenda Items:
- Notary Project annual review https://github.com/cncf/toc/issues/1018#issuecomment-1682556150 (Toddy)
- Security advisory - this should be discussed privately in the Slack channel among maintainers
    - Shiwei is important to the conversation, we need to wait for his presence
- Any blockers for the 1.1.0 relese in November
    - Signing arbitrary artifacts is running a bit late
        - Pritesh is targeting to have the spec ready for discussion for next week's (10/9) meeting
    - List of items is available at https://github.com/orgs/notaryproject/projects/10/views/7
        - Items assigned to folks to be confirmed (@Toddysm and @pritesh)
        - @shizh to follow up with the team if they can take those items
        - Adding priorities to the items will help with scheduling (@Yi and @Feynman)
- Random
    - @Feynman and @yizha1 can you speak about the adoption of DockerHub on this page https://notaryproject.dev/?
    - How do we measure adoption (Samir)
        - We need to define the way we measure adoption (Toddy)
        - Possible metrics (Samir)
            - Number of visitors to our web page
            - Number of visitors to the release page/number of downloads
    - Doing retrospecives (Toddy)
        - Somebody to post question before we do the retrospective (Samir)
        - How often? (Toddy)
            - After major release (Samir). Proposal is to do it after the 1.1.0 release
            - At least twice a year (Sajay)
        - @toddysm can work on a proposal for retros
    - Looking at the long term investments (Toddy)
        - We can repurpose one of the Thursday meetings for that (Sajay)
        - We also need to have somebody write a strategy to be useful (Sajay)
        - Urge the community to create a wish list (Sajay)
            - @pritesh and @Samir to eventually styart a list

### Notes:
- _meeting minutes_

Agenda items must identify the (owner) of the item

### Recording
https://www.youtube.com/watch?v=FzrwC5y1HOQ

## Sept 28 2023
CANCELLED due to no agenda and people unable to attend

## Sept 25 2023

### Attendees:
- Yi Zha
- Pritesh 
- Toddy SM
- Shiwei Zhang
- Feynman Zhou
- Jungie Gao
- Patrick Zheng
- Pablo
- Sajay Antony

### Agenda

- Discussion of PRs (Pritesh)
    - https://github.com/notaryproject/notation/pull/771#issuecomment-1731705600
    - https://github.com/notaryproject/notation-go/pull/345
- Review and discuss feature "Sign Arbitrary Data" https://hackmd.io/ewbJr2ZnT4a8U1ObDVXcSw?view (Pritesh)
- [KubeCon China](https://www.lfasiallc.com/kubecon-cloudnativecon-open-source-summit-china/) (9/26 - 9/28)
- Public holidays in China Mainland (9/29 - 10/6)

### Meeting Notes:

- Pritesh can help to create an issue for a optimized verification workflow: https://github.com/notaryproject/notation/issues/790
- Continously discuss the experience of multiple signature verifcation failures, should we print out all the failure by default or leverage the verbose flag @yizha1 
- We walked through the comments for "Sign Arbitrary Data" hackmd, Pritesh will update the spec accordingly, we need to continoue the review later.

### Recording

https://www.youtube.com/watch?v=S_bXMvI1y4o

## Sept 18 2023

### Attendees:
Yi Zha
Feynman Zhou
Shiwei
Patrick
Junjie
Pritesh
Samir
Toddy
Sajay

### Agenda Items:

- Release Notation GitHub Actions and submit it to GitHub Marketplace (Feynman)
- Triage other issues marked in [1.1.0 milestone](https://github.com/notaryproject/notation/milestone/17) (Yi)
- INFO: KubeCon China from Sep 26 to Sep 28
    - [Kicking Security Chain Attacks to the Curb with Kyverno and Notary Project in GitOps](https://www.lfasiallc.com/kubecon-cloudnativecon-open-source-summit-china/program/schedule/) - Feynman
    - [Securing Container Supply Chain in CICD with Notary Project, ORAS and Harbor](https://www.lfasiallc.com/kubecon-cloudnativecon-open-source-summit-china/program/schedule/) - Yi wo Harbor maintainer
- Additional guidance for difference with TUF based update?


### Notes
- We didn't complete all the topics today.
- Notation GitHub action will be submitted to GitHub marketplace on 9/20/2023
- We can continiously iterate GitHub actions by adding new enhancements and user guides.
- Pritesh will try the actions and provide feedback
- We triaged several issues in [1.1.0 milestone](https://github.com/notaryproject/notation/milestone/17), but didn't complete. Suggest reviewing the issues offline first, then we finalize it during the community meeting.

### Recording

https://www.youtube.com/watch?v=rrg1_xxQgh0


## Sept 14 2023

### Attendees:
- Sajay Antony
- Samir Kakkar
- ToddySM 

### Agenda Items:
- Ad-hoc agenda today

### Notes:
- Samir and Toddy discussed the KubeCon maintainers track
    - Samir will follow up with Milind on that
- Samir completed the PR reviews marked as action items from the last meeting

### Recording
https://www.youtube.com/watch?v=rxfqqKw1kcM

## Sep 11, 2023

### Attendees:
- Yi Zha
- ToddySM 
- Sajay Antony
- Feynman Zhou 
- Shiwei Zhang
- Patrick Zheng
- Junjie Gao
- Fan Du 
- Samir Kakkar
_add yourself_

### Agenda Items:

- Follow up actions from previous meeting
- Notary Project v1.1.0 release planning
    - [Feature](https://github.com/notaryproject/notation/issues/768) assginments
    - Documentation [v1.1.0](https://github.com/notaryproject/notaryproject.dev/milestone/8)
    - Specification [v1.1.0](https://github.com/notaryproject/specifications/milestone/22)
- PR Review
    - [Release schedule and support policy](https://github.com/notaryproject/notaryproject.dev/pull/348)
    - [archive process](https://github.com/notaryproject/.github/pull/37)
    - [contributing guide](https://github.com/notaryproject/.github/pull/25)

### Notes

- Request review on [TOC](https://github.com/notaryproject/notaryproject.dev/pull/312), Samir and Zach to review this PR.
- Request review on [contributing PR](https://github.com/notaryproject/.github/pull/25), @pritesh and other maintainers
- Once we align with the criteria for stale issues or PRs, we can start to practice automation workflow on website repo to clean up stale issues and PRs.
- Requet broader review on archiving process, @Toddy, and Samir

### Recording

- https://www.youtube.com/watch?v=H96aPvjb7b0

## Sep 7, 2023

### Attendees:
- Sajay Antony
- ToddySM
- Zach

### Agenda Items:
- Ad-hoc agenda

### Notes:
- Discussed documentation items (@Feynman and @yizha1 please work with @Roseline and @Sanjay to complete the important PRs below)
    - The TOC https://github.com/notaryproject/notaryproject.dev/pull/312 is blocking a lot of other stuff. We need to prioritize this one - @Roseline if you can take action and resolve the conflicts so we can merge
    - We agreed on closing items that are older than Jan 2023 and ask the submitters to reopen if they deem the update important
    - Next, let's prioritize the Landing page https://github.com/notaryproject/notaryproject.dev/pull/335 and this will unblock some site-wide issues
    - Net new content (@Zach)
        - GitHub Actions documentation
        - Update the installs with the Brew instructions for MacOS and other updates to the installs
        - Eventually get some nuggets from the Tanzu podcast https://tanzu.vmware.com/content/videos/enlightning-ensuring-software-authenticity-introduction-to-notary-project
            - How Notary Project differs from Sigstore
            - One-page summary of what Notary Project is
        - Add links to cloud providers and other project and vendors that integrated with Notary Project tooling. Integration partners page.
            - AWS
            - Azure
            - Hashicorp
            - containerd
            - Harbor
            - Kyverno
- (@Sajay) We need to have a page describing the release schedule and the support policy for Notary Project tools - @Feynman and @yizha1 to kick off this work
- (@Zach) Versioning of the content is becoming important topic. We need to make decisions on the git structure, branching, etc. Issue with proposal to be filed in the documentation repo for documenting, discussion and formal approval. @Zach to file. 

### Recording link
https://www.youtube.com/live/q1Kx856MXAw?si=oiGo6dgfzcf8HCZ5

## Sep 5, 2023

### Attendees
 - Yi Zha
 - Sajay Antony
 - Toddy SM
 - Pritesh
 - Patrick Zheng
 - Feynman Zhou
 - Fan Du
 - Shiwei Zhang 
 - 
_add yourself_

### Agenda Item:

- [Discuss user stories and target date for Notation v1.1](https://github.com/notaryproject/notation/issues/768) (Yi)
- [PR Bump apache/skywalking-eyes from 0.4.0 to 0.5.0](https://github.com/notaryproject/notation-core-go/pull/161) (Yi/Shiwei)
- We onboarded Notation to Homebrew (for macOS/Linux) and Winget (for Windows). Users can install Notation with just one command. Request maintainers to review the [doc PR](https://github.com/notaryproject/notaryproject.dev/pull/338). (Feynman)
    - Homebrew: `brew install notation`
    - Winget: `winget install notation -s winget`

### Notes
- We agreed that using date based release approach. We will have at least one release per quarter. It could be patch release, minor release or major rlease. For next release, Nov 15 will be the code freezing date, release date will be Nov 22, given one week after code freezing. The worst case is that we don't have any features ready by target date, but we will still cut a patch release for small enhancements and bug fixing.
- Pritesh, Toddy, Sajay to take a look at the proposal of issue https://github.com/notaryproject/notation/issues/777, we can discuss it offline
- Feynman/Yi to consult skywalking-eyes/CNCF to find the root cause, like whether Apache license can depend on dependencies with MPL2.0
    - https://github.com/apache/skywalking-eyes/blob/main/assets/compatibility/Apache-2.0.yaml
- Shiwei will help to create two issues to address the improvements mentioned by him.
    - `brew`: https://github.com/notaryproject/notation/issues/778
    - `winget`: Binary is directly obtained from the github releases. Therefore, no change / issue on this.

### Recording
- https://www.youtube.com/watch?v=4W_MXHy9VTw


## Aug 31, 2023

### Attendees:
- _add yourself_

### Agenda Items:
- [Discuss user stories and target date for 1.1](https://github.com/notaryproject/notation/issues/768) (Samir)
- Proposal to move meeting on Sep 4 to Sep 5 due to US holidays (Yi)
- Action from previous meeting: any feedback from Pritesh on `mediatype` usage in signature payload? Yi is adding a spec to cover non-oci signature payload and storage, ETA Sep 5 for review. (Yi)
- Request Pritesh and Samir to re-review governance PRs (Yi)
    - [Notation-go readme.md](https://github.com/notaryproject/notation-go/pull/343)
    - [notation-core-go readme.md](https://github.com/notaryproject/notation-core-go/pull/158)
    - [Achive process](https://github.com/notaryproject/.github/pull/37)
    - [Contributing guide](https://github.com/notaryproject/.github/pull/25)
- We onboarded Notation to Homebrew (for macOS/Linux) and Winget (for Windows). Users can install Notation with just one command. Request maintainers to review the [doc PR](https://github.com/notaryproject/notaryproject.dev/pull/338). (Feynman)
    - Homebrew: `brew install notation`
    - Winget: `winget install notation -s winget`
    
### Notes:
- _meeting minutes_


## Aug 28, 2023

### Attendees:
- Yi Zha
- Fyenman Zhou
- Pritesh
- Patrick Zheng
- Shiwei Zhang
- Samir Kakkar
- ToddySM
- Sajay Antony
- _add yourself_

### Agenda Items:
- [When is 1.1 release and what to include in it.](https://github.com/notaryproject/notation/issues/768) (Pritesh)
- [For siginng non-oci(arbitrary) artifact, Signature Payload format should include mediatype or not.](https://github.com/notaryproject/notation/discussions/767) (Pritesh)
- Information sharing on KubeCon China 2023 (Sep 26 ~ Sep 28), and public holidays (Sep 29 ~ Oct 6) (Yi)

### Notes:

- Clarify the purpose of Major/Minor/patch release in [Release Management](https://github.com/notaryproject/notation/blob/main/RELEASE_MANAGEMENT.md)
    - @yizha1 create an issue for tracking
    - We will differ discussion of supporting n and n-1 major minor release to 1.1 release.
- Need continous discussions on release cadence for patch releases and feature releases
- @yizha1 Prepare a prioritized feature list and add it in [issue](https://github.com/notaryproject/notation/issues/768) for discussion on Thursday Community Meeting.
- We discussed that mediatype is important for declaring the purpose of the content to avoid potential security risk. Sajay suggests using default mediatype `application/octet-stream` for arbitrary content, and users can specific their own mediatype based on the needs. @pritesh will consider these comments and a follow-up discussion is required.

### Recording






## Aug 24, 2023

### Attendess
- Roseline
- Samir
- ToddySM
- Zach

### Agenda

- Request PR review (Yi)
    1. [Notation v1 blog](https://github.com/notaryproject/notaryproject.dev/pull/300)
    2. [Contributing guide](https://github.com/notaryproject/.github/pull/25), which includes the planning improvements discussed in previous meeting. We can start practicing while reviewing this guide.

### Notes
- Samir, Toddy, and Pritesh will take a look at the changes in [Notation v1 blog](https://github.com/notaryproject/notaryproject.dev/pull/300) and approve the PR
- Homework for the contributors to look at the [Contributor's guide](https://github.com/notaryproject/.github/pull/25) and provide feedback
    - Open question is whether any subproject specific guidelines will be covered by this guide
    - We also need to link the guide from each individual subproject README
- Ask for @Feynman and @yizha1 - can we update the icon on YouTube channel to remove the V2 part in the lower right corner
![YouTube screenshot](https://hackmd.io/_uploads/r1VCbZH63.png)
- @Samir will check with Pritesh and Milind about KubeCon NA 2023
- Appeal to the community is to start planning for next set of features (signing local images, signing arbitrary files, timestamping, plugins, etc.). We should have discussion in the next community meeting
    - Should we include plugins by default
    - We should plan for smaller releases instead of bigger ones


### Recording
https://www.youtube.com/watch?v=WB8F3595grA

## Aug 20, 2023

### Attendees

- Yi Zha
- Toddy SM
- Junjie Gao 
- Pablo
- Samir Kakkar
- Patrick Zheng
- Sajay Antony
- Feynman Zhou
- Fan Du

### Agenda

- [Improvements for Notary Project Planning](https://hackmd.io/efzM7JIeTPCkND5VJKdY7w?view) (Yi)

### Notes

- Notary Project maintainers to review the [PR of the system release announcement blog](https://github.com/notaryproject/notaryproject.dev/pull/300) by 8/22/2023.
- The decision is to use a hybrid model to triage issues regularly. Samir suggested reserving 15 min in community meeting to triage new issues, especially issues for new features. Bugs can be triaged offline. We can start the practice next week and continoulsy improve the practice over time.
- Label `triage` or `question` may not be required for PRs, @yizha1 will consider the comments and update the PR.
- Pritesh and Feynman suggested moving the milestone management content to the PR and make the dicision with other maintainers offline, @yizha1 will create a PR to update the milestone management, and send out contributing PR for review.

### Recording

https://www.youtube.com/watch?v=dK_C5I0shPg

## Aug 17, 2023

### Attendees
- Samir Kakkar
- Sajay Antony 
- Daniel (CNCF)

### Agenda

- Request reviewing the remaining PRs for issue [Proposal for bringing clarity to the Notary Project branding](https://github.com/notaryproject/.github/issues/35). Here is the [prioritized PR list](https://github.com/notaryproject/.github/issues/35#issuecomment-1682016530) (Yi)
- Review of the notaryproject.dev open PR - In progress (Samir)

### Notese
- Samir to ping reviewers for the open PRs above
- Sajay suggestion for https://deploy-preview-312--notarydev.netlify.app/community/ is to get the must have changes now and create seprate tracking items for nits/enhancements.

## Aug 14, 2023

### Attendees

- Yi Zha
- Toddy SM
- Junjie Gao 
- Pablo
- Feynman Zhou
- Samir Kakkar
- Shiwei Zhang
- Patrick Zheng
- Sajay Antony

### Agenda

- Notation CLI v1.0.0 release process (Yi)
    1. Walk through and finalize [release note](https://hackmd.io/@shizh/rJ6A-zQ32)
    2. Release [Notation CLI v1.0.0](https://github.com/notaryproject/notation/issues/749)
    3. Slack channel to announce Notation CLI v1.0.0 release
- Notation CLI post-v1.0.0 release (Yi)
    - Review and merge [update website banner](https://github.com/notaryproject/notaryproject.dev/pull/281)
    - Review and Merge [Notation v1 blog](https://github.com/notaryproject/notaryproject.dev/pull/300) for system release announcement
    - Merge [release management PR](https://github.com/notaryproject/notation/pull/714)
    - Review and Merge [Release checklist PR](https://github.com/notaryproject/notation/pull/713)
    - Review and merge website PRs [update website meta](https://github.com/notaryproject/notaryproject.dev/pull/331), [overview](https://github.com/notaryproject/notaryproject.dev/pull/334), [naming update](https://github.com/notaryproject/notaryproject.dev/pull/327)
    - Add [Mac](https://github.com/notaryproject/notation/issues/571) and [Windows](https://github.com/notaryproject/notation/issues/570) installer for Notation CLI v1.0.0.


### Notes

- @shi to release Notation CLI v1.0.0 after community meeting 8/14/2023
- Announce Notary Project system release
    - @feynman to update the [blog post](https://github.com/notaryproject/notaryproject.dev/pull/300) for Notary Project system release, and @samir to review it by Aug 15
- Complete the review on other PRs after merging the blog PR
    - [release management PR](https://github.com/notaryproject/notation/pull/714), merge it after Notation v1 release
    - [Release checklist PR](https://github.com/notaryproject/notation/pull/713), need @Pritesh or @Milind to review it
    - Need @samir to review website PRs
        - [update website banner](https://github.com/notaryproject/notaryproject.dev/pull/281)
        - [update website meta](https://github.com/notaryproject/notaryproject.dev/pull/331)
        - [overview](https://github.com/notaryproject/notaryproject.dev/pull/334)
        - [naming update](https://github.com/notaryproject/notaryproject.dev/pull/327)
- Considering using brew for linux installer, @yizha1 to create an issue for tracking it.
        

### Recording

- https://www.youtube.com/watch?v=xktLZjupEow

## Aug 10, 2023

### Attendees
- Roseline Bassey
- Sajay Antony
- Samir Kakkar
- Toddy SM
    
### Agenda

- Notary Project release blockers (TSM)
    - FAQs for terminology and names https://github.com/notaryproject/notaryproject.dev/pull/328 (major)
    - Changing references to `notaryproject` repo to `specifications` https://github.com/notaryproject/.github/pull/50 (minor)
    - Notary Project meta tag https://github.com/notaryproject/notaryproject.dev/pull/331 (minor)
- Need @Samir to help review [Notation v1.0.0 release blog](https://github.com/notaryproject/notaryproject.dev/pull/300). Feynman has resolved his suggested changes. It will be submitted to cncf.io after the v1 release (Feynman) 
    
### Notes
- Notary Project release blockers
    - ToddySM, Samir will review https://github.com/notaryproject/notaryproject.dev/pull/328 and approve
    - Samir, Pritesh to look at the minor PRs and review
    - (Sajay) Release notes review and communication
        - (Samir) Notation release announcement are already reviewed
        - We are talking about the release notes on the GitHub release
        - Shiwei will share a HackMD with the proposed release notes and we will review
- (Roseline) is requesting feedback on her https://github.com/notaryproject/notaryproject.dev/issues/107
- (Roseline) asking for review of the web-site docs structure https://github.com/notaryproject/notaryproject.dev/pull/312
- (Samir) Raised the question that there is no system release annoncement. We have individual Notation and Spec announcement but nothing for the system release. Example: https://github.com/notaryproject/roadmap/tree/main/RELEASENOTES (@FeynmanZhou and @yizha1 can we follow up and prepare those?)
    
### Recording
https://www.youtube.com/watch?v=zDzcuz8xMUA

## Aug 7, 2023

### Attendees

- Feynman Zhou
- Shiwei Zhang
- ToddySM
- Sajay Antony
- Pritesh
- Samir Kakkar
- Miran Kurukulasuriya
- Patrick Zheng
- Yi Zha

### Agenda

- Notation CLI v1 release status check-in (Yi)
    - [Release Notation CLI v1.0.0](https://github.com/notaryproject/notation/issues/749) 

- PR for post Notation CLI v1 release (Yi)
    - Notation v1 release announcement [blog](https://github.com/notaryproject/notaryproject.dev/pull/300)
    - Documentation updates for website
        - https://github.com/notaryproject/notaryproject.dev/pull/327
    - `README.md` updates for Notary Project Overview
        - https://github.com/notaryproject/notation-go/pull/343
        - https://github.com/notaryproject/notation-core-go/pull/158
        - https://github.com/notaryproject/notation-action/pull/18
        - https://github.com/notaryproject/notaryproject.dev/pull/295
        - https://github.com/notaryproject/notation-hashicorp-vault/pull/9
        - https://github.com/notaryproject/tuf/pull/45
        - https://github.com/notaryproject/meeting-notes/pull/18
        - https://github.com/notaryproject/roadmap/pull/92
    - Proposal of archiving process
        - https://github.com/notaryproject/.github/pull/37
- Vote for `notation v1.0.0` release (Shiwei)
    - Vote link: https://github.com/notaryproject/notation/pull/748


### Notes

- [x] Regarding [RELEASE CHECKLIST #PR713](https://github.com/notaryproject/notation/pull/713), the decision is to remove [RELEASE CHECKLIST #PR713](https://github.com/notaryproject/notation/pull/713) from the blocking issues of v1 release
- It is decided that [FAQ PR](https://github.com/notaryproject/notaryproject.dev/pull/328) need to be completed before Notation CLI v1 release
- [ ] Regarding ETA of Notation CLI v1 release, the decision is to finalize all blocking issues and release Notation CLI v1 by Aug 11
- [ ] Notary Project maintainers to review PRs for post v1 as listed in [issue #35](https://github.com/notaryproject/.github/issues/35#issuecomment-1653281321)


### Recording

- https://www.youtube.com/watch?v=AGS-S-pMx-A

## Aug 3, 2023

### Attendees
- Roy Williams
- Sajay Antony
- Samir Kakkar
- ToddySM
- Zach Rhoads

### Agenda

- Info: Repo `notaryproject/notaryproject` was renamed to `notaryproject/specifications` after reaching 2/3 supermajority, and the relevant [issue](https://github.com/notaryproject/.github/issues/38) was closed (Yi)
- Call-out: PRs review and merge for Notation v1 releases (Yi)
    - [specifications#256](https://github.com/notaryproject/specifications/pull/256)
        - Need Toddy approval, since changes were requested by Toddy
    - [specifications#263](https://github.com/notaryproject/specifications/pull/263)
        - Need one more approval from Milind or Pritesh
    - [.github#32](https://github.com/notaryproject/.github/pull/32)
        - Need Milind approval, since changes were requested by Milind
        - Need Toddy to fix the DCO error
    - [notaryproject.dev#326](https://github.com/notaryproject/notaryproject.dev/pull/326)
        - Need both Samir and Zach approvals, since changes were requested by them
- Release [specifications](https://github.com/notaryproject/specifications) v1.0.0 after above two PRs [specifications#256](https://github.com/notaryproject/specifications/pull/256) and [specifications#263](https://github.com/notaryproject/specifications/pull/263) are merged (Yi)

### Notes
- Call-out: PRs review and merge for Notation v1 releases (Yi)
    - [specifications#256](https://github.com/notaryproject/specifications/pull/256)
        - Need Toddy approval, since changes were requested by Toddy
            Samir will ping Pritesh, Milind, and Niaz for approvals. Toddy will review today and approve.
    - [specifications#263](https://github.com/notaryproject/specifications/pull/263)
        - Need one more approval from Milind or Pritesh
            Samir will ping Pritesh, Milind, and Niaz for approvals. Toddy will review today and approve.
    - [.github#32](https://github.com/notaryproject/.github/pull/32)
        - Need Milind approval, since changes were requested by Milind
        - Need Toddy to fix the DCO error
            Samir will ping Pritesh, Milind, and Niaz for approvals. Toddy will address the DCO errors.
    - [notaryproject.dev#326](https://github.com/notaryproject/notaryproject.dev/pull/326)
        - Need both Samir and Zach approvals, since changes were requested by them
            This should be in the `.github` repo and we should refer to it. This is not blocking for release. We can add after the release.
    - Specification PR needs approvals https://github.com/notaryproject/specifications/pull/256 by maintainers. This can be done in parallel with the other PRs
- [Zach] Discussion related to the following comment https://github.com/notaryproject/notaryproject.dev/pull/312#issuecomment-1661051838. Zach needs feedback from the maintainers and the community
- [Samir] Is the "the" important to the branding. Should we capitalize it always or just when it is grammatically required. We decided that "the" is insignificant and it is not part of the brand "Notary Project".
- [Samir] Feedback on renaming "notary" repo to "notary-tuf". There was a feedback from two maintainers. We believe that the decision to keep the name is made and we can move on from that proposal.

### Recording
https://www.youtube.com/watch?v=FIEkkduYCDA

## July 31, 2023

### Attendees
 - Yi Zha
 - Feynman Zhou 
 - Toddy SM 
 - Shiwei Zhang 
 - Patrick Zheng
 - Zach
 - Pritesh
 - Junjie Gao
 - Sajay Antony
 - Pablo Rincon

### Agenda

- [New directory structure and version control](https://github.com/notaryproject/notaryproject.dev/pull/312) (Feynman)
- [[Arbitary data signing]](https://hackmd.io/QteHaBQTS-6h-AsU04U1cQ?both) [[notation/issues/741]](https://github.com/notaryproject/notation/issues/741): Support signing of already calculated hash. (Pritesh)
- Notation v1 release (Yi)
    -  Merge branding related PRs
    -  Rename `notaryproject` to `specifications`
    -  Review v1 blog, and merge it for official announcement
    -  See complete [list](https://cloud-native.slack.com/archives/CQUH8U287/p1690507615334939)
- Review Other branding issues in parallel with Notation v1 release, see [Issues and PRs NOT blocking Notation v1.0.0 release:](https://github.com/notaryproject/.github/issues/35#issuecomment-1653281321) (Yi)
- Wondering if we want to use "The Notary Project" or "the Notary Project" everywhere in our docs? (Samir)


### Notes

- Keep current documentation structure for Notation v1 release, and further discussion on versioning and structures are required for future releases.
- Need further discussion on [notation/issues/741](https://github.com/notaryproject/notation/issues/741)
- Agreed on [complete the list of PRs and issues](https://cloud-native.slack.com/archives/CQUH8U287/p1690507615334939) for Notation v1 release by mid of this week, and decision on Thursday community call for Notation v1 release.
- The last topic "Wondering if we want to use "The Notary Project" or "the Notary Project" everywhere in our docs?" was not discussed, @yizha1 posted this qustion [here](https://github.com/notaryproject/.github/issues/35#issuecomment-1659443419) for further discussion 

### Recording

https://youtu.be/7_pORhoAMzM



## Jul 27, 2023

### Attendees
- Sajay Antony
- Pritesh Bandi
- Sanjay
- Roseline

### Agenda

- Call-out: Review branding related issues and PRs (~`20` in total), see [complete list under .github issues#35](https://github.com/notaryproject/.github/issues/35#issuecomment-1653281321) 
- Review v1 blog https://github.com/notaryproject/notaryproject.dev/pull/300
- Review of the new landing page UI for the Notary Project website https://github.com/notaryproject/notaryproject.dev/pull/320

### Notes

- Discussed the issues to unblock notation relase. 
- Pritesh will follow up with Milind and Niaz. 
- Doc PRs require help from Zach for Rosaline and Sanjay. How can we proceed with the restructing?

## July 24, 2023

### Attendees
- ToddySM 
- Feynman Zhou
- Yi Zha
- Pritesh
- Shiwei Zhang
- Patrick Zheng
- Junjie Gao
- Sajay Antony

### Agenda

- Follow-up on [naming proposals](https://github.com/notaryproject/.github/issues/35) (Yi)
  - Archiving process https://github.com/notaryproject/.github/pull/37
  - Update readme to align with TUF
  https://github.com/notaryproject/notary/pull/1685
  - Proposal for the creation of a specifications repository https://github.com/notaryproject/.github/issues/38
- Notation CLI and libraries v1 release status (Yi)
    - [Notation Core Go Library](https://github.com/notaryproject/notation-core-go) v1.0.0 was approved and [released](https://github.com/notaryproject/notation-core-go/releases/tag/v1.0.0)! 
    - Track for [releasing `notation` v1.0.0](https://github.com/notaryproject/notation/issues/749)
- [vote: A new repository for creating framework for notation plugin ](https://github.com/notaryproject/.github/issues/45) (Pritesh)


### Meeting Notes

- @pritesh to nominate Samir as maintainers for ``.github` repo and emeritus of Vani
- @yizha1 to create an issue to define a clear criteria for "supermajority" in the governance guide. In general, two-thirds supermajority means the criteria.
- Regarding renaming `notaryproject/notaryproject` repo as described in [issue 38](https://github.com/notaryproject/.github/issues/38), we need to get super-majority approval from Notary Project maintainers.
- @pritesh to comment on [issue 749](https://github.com/notaryproject/notation/issues/749). The decision is to cut the Notation CLI v1.0.0 and announce it after fixing the naming issue. --done
- @yizha1 to comment on [PR 1685](https://github.com/notaryproject/notary/pull/1685) with the conclusion that the decision is to merge this PR and bypass the CI checks
- Notary Project maintainers to finish the naming issues and send out PRs for review before July 27. We will use the Thursday's meeting as a check point
- @toddysm to resolve the comments and finalize [PR 32](https://github.com/notaryproject/.github/pull/32) by July 27

### Recording
https://www.youtube.com/live/a1f47VX-ssk

## July 20, 2023

### Attendees:
- Miran Kurukulasuriya
- Naga
- Roseline Bassey
- Sajay
- Samir Kakkar
- ToddySM
- Zach

### Agenda 
- Governance items (Samir)
    - Notary Project logo update
    - FAQ work item
    - Work item for nominating Samir
- Documentation items (Zach)
    - Get arpprovals for the PR from Roseline https://github.com/notaryproject/notaryproject.dev/pull/312
    - Versioning of the docs
- Sign arbitrary file (Miran)
- Kick off release discussion for notation-go notation-core-go and notation

### Notes
- Governance
    - For the logo @Feynman will create a ticket to request designer and work with them to update the logo. Work item is created by Feynman https://github.com/notaryproject/.github/issues/43
    - New work item will be created by Toddy and linked to the common work item https://github.com/notaryproject/.github/issues/35
    - @pritesh will create work item to nominate Samir as maintainer (and replace Vani)
- Documentation
    - As of today we have capability to publish the CLI auto-generated documentation but we don't have ability to publish API documentation and we don't have any other bespoke developer content except the secure development one
    - We need the following audiences: End users, Developers of plugins, Developers who use the spec, Developers who use the libraries for their tools and we need to address all their needs in the documentation
    - Evenrgreen content will be at the top level, spec related content will be under the Developer level
    - Discussion will continue offline
- Sign Arbitrary Files
    - Miran's scenario. He wants to sign installer file and publishe it as GitHub package (as GitHub release). If Notation can sign GitHub release it will make sense. The signature will be part of the release (as a signature file) but can be in some other way. He is interested to understand how to distribute the trust policy. 
    - We will document scenarios in https://github.com/notaryproject/notation/issues/741
- Kick off release
    - Starting the release of the three components - Notation-Core-Go, Notation-Go, Notation CLI. Agreed to start the process and queue everything. 

### Recording
https://www.youtube.com/live/6GYEQEGcmqw?feature=share

## July 17, 2023

### Attendees:
- ToddySM
- Sajay
- Shiwei Zhang
- Yi Zha
- Feynman Zhou
- Samir Kakkar
- Pritesh
- Patrick Zheng
- Junjie Gao

### Agenda Items:
- [Notation to sign and veify arbitrary data #741](https://github.com/notaryproject/notation/issues/741) (Pritesh)
- [Support go library based plugins](https://github.com/notaryproject/notation-go/issues/336) (Pritesh)
- Follow up action points from previous meeting (Yi)
- [Governance improvement plan](https://github.com/notaryproject/.github/discussions/42) (Feynman)
- PR still no update from maintainer on 'TUF notary CLI' https://github.com/notaryproject/notary/pull/1685
- Call for PR reviews: dependabot PRs

### Notes:
- Millind will provide updates on naming issue on Jul 18.
- Toddy will resolve the comments in the PR for notation-action repo govenernance today (Jun 17)
- Millind will work with Toddy on the podcast.
- Toddy submitted the document with Pritesh, Samir, Justin as co-speakers, we can decide the co-speaker in Aug.
- Notaiton issue #741 will be planned for Notation post-v1 release. Patrick will find the document related to this feature and share it to Pritesh for further discussion.
- Patrick will create two issues in notation-go repo:
    - Let signer.NewFromPlugin take a more relaxed plugin.SignPlugin instead of plugin.Plugin, targeting v1 release
    - Adding plugin examples for notation-go library
- Sajay will tag org maintainers on the PR https://github.com/notaryproject/notary/pull/1685
- Feynman will tranform the [discussion](https://github.com/notaryproject/.github/discussions/42) to issue and share the link in the slack channel to ask maintainers for review.

### Recording
see https://youtu.be/sbTL1AwZScA

## July 13, 2023
- Zach
- Pritesh
- Sanjay

### Agenda Items
- Sanjay wants feedback on redesign of website

### Notes
- Sanjay to share [ux design](https://www.figma.com/file/rj5BvQDNPon4mipgajOlr5/Notary-website-landing-page-(Redesign)?type=design&node-id=0-1&mode=design) on slack channel to solicit feedback from comunity. 

## July 10, 2023

### Attendees

- Fan Du
- Feynman Zhou
- Junjie Gao
- Miran Kurukulasuriya
- Patrick Zheng
- Pritesh
- Shiwei Zhang
- ToddySM
- Yi Zha

### Agenda Items

- Decision and next step on the [Notary Project naming/branding issue](https://github.com/notaryproject/.github/issues/35)
- Confirm Notation v1.0.0 release ETA
- Proposal to update MAINTAINERS and CODEOWNERS with the following:
    - Link org maintainers from .github repo
    - Considering active maintainers for CODEOWNERS. Active maintainers are maintainers who commit contributing or reviewing PRs timely for specific repo
- Notary Project at Enlightning podcast (see https://cloud-native.slack.com/archives/CQUH8U287/p1688733359614519) (ToddySM)
- Maintainer Track and/or Contribfest session for KubeCon + CloudNativeCon North America 2023 deadline is July 16th (ToddySM)

### Notes
- Decision and next step on the [Notary Project naming/branding issue](https://github.com/notaryproject/.github/issues/35)
    - Discussion between Milind, Niaz, Toddy agreed to resolve the naming/branding issue by end of this week
    - On Thursday's meeting hopefully we will have the issue unblocked
- Confirm Notation v1.0.0 release ETA
    - This is blocked on the first bullet point. Targeting three weeks from now (July 27th)
- Proposal to update MAINTAINERS and CODEOWNERS with the following:
    - Action on Toddy: use GitHub team name instead of listing all the org maintainers in CODEOWNERS file. Starting with notation-action repo to see whether it works as expected.
    - Action on Toddy: add a comment in MAINTAINERS that Org Maintainers are also considered repo owners and link to the Org Maintainers file in .github repo.
- Notary Project at Enlightning podcast (see https://cloud-native.slack.com/archives/CQUH8U287/p1688733359614519) (ToddySM)
    - Toddy will check with Whitney on the time changes to 2nd half of Aug
    - Pritesh will check with Niaz on the guideline to join the podcast event by Wed Jul 12.
- Maintainer Track and/or Contribfest session for KubeCon + CloudNativeCon North America 2023 2deadline is July 16th (ToddySM)
    - Pritesh will get back to Toddy on this joint activity by Wednesday Jul 12.
- Notation security audit report will be published at 8AM GMT, July 11th
  - Feynman will merge two PRs [302](https://github.com/notaryproject/notaryproject.dev/pull/302) and [303](https://github.com/notaryproject/notaryproject.dev/pull/303) by 8am GMT, July 11th
- Timestamping https://github.com/notaryproject/roadmap/issues/59
    - Shiwei will comment on this issue by Jul 12

### Recording
https://www.youtube.com/watch?v=QN5Ysoxb6_o


## July 6, 2023

### Attendees
- Ivan Wallis
- Sajay Antony
- ToddySM
- Zach Rhoads

### Agenda Items

- Notary Project maintainers to review and merge PRs for publishing the Notation security audit report and blog post on July 6
    - Security page: https://github.com/notaryproject/notaryproject.dev/pull/302/
    - Security audit report: https://github.com/notaryproject/notaryproject/pull/268
    - Blog post: https://github.com/notaryproject/notaryproject.dev/pull/303
    - Secure deployment guide: https://github.com/notaryproject/notaryproject.dev/pull/228
- Ivan questions about plugin development
- Zach's proposal for Notation section in the documentation (based on Roselin's proposal) - https://deploy-preview-304--notarydev.netlify.app/docs/
- How to move Sajay's PR forward https://github.com/notaryproject/notary/pull/1685
- Agree on the name for the GHA repo https://github.com/notaryproject/.github/issues/30

### Notes
- Ivan questions about plugin development
    - RFC 3161 timestamping
        - Planned but we need to have in a milestone (most probably in 1.1.0)
    - Technical question about plugin
        - Pass in vendor specific attributes - this should be supported
        - Add documentation how to implement those (@Zach)
    - Ivan will open issues in https://github.com/notaryproject/notaryproject.dev to keep track on those items
- Zach's proposal for Notation section in the documentation (based on Roselin's proposal) - https://deploy-preview-304--notarydev.netlify.app/docs/
    - Ivan had feedback on the spec and the implementation - it will be good to have Implementation Best Practices for Developers - not only about plugins but about signature types etc.
        - He is looking for references
        - He is refering to the spec
        - Example (any language) implementation of a plugin will be helpful
- Zach's nomination https://github.com/notaryproject/.github/issues/34
    - Toddy to create a PR in the `notaryproject.dev` repo for the maintainers and codeowners file
- Zach asked whether he can generate CLI reference and prep the docs for 1.0.0 release
    - We are in agreement that he can start with that
- Toddy will go ahead and create `notation-action` repository as Shiwei proposed in https://github.com/notaryproject/.github/issues/30
- How to move Sajay's PR forward https://github.com/notaryproject/notary/pull/1685
    - Maintainers are not active on this PR. Toddy tagged maintainers from Docker

## July 3, 2023

### Attendees
- Shiwei Zhang
- Patrick Zheng
- Junjie Gao
- Feynman Zhou
- Samir Kakkar
- Viktor Lu
- Pritesh

### Agenda Items

- Notation v1.0.0 status check-in
- Confirm the release date of the security audit report and blog post status
- Confirm the repository naming of notation github actions


### Notes

- The security audit report will be released on June 6. @Feynman will work with Samir to finish the blog post of the security audit announcement on July 5
- PRs need to be reviewed and merged by Notary Project maintainers before releasing Notation v1.0.0
    - https://github.com/notaryproject/notaryproject.dev/pull/228
    - https://github.com/notaryproject/notaryproject.dev/pull/300
    - https://github.com/notaryproject/notation/pull/730
- @toddysm to resolve the comments from Niaz in the [Notation branding issue](https://github.com/notaryproject/.github/issues/35#issuecomment-1613362300)
- Considering a general repository name since the Notation GitHub Actions might be evolved from a single action (setup) into multiple actions (setup, sign, verify) in the future

### Recording

https://www.youtube.com/live/k6O5ecaoBnA?feature=share
