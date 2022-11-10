### Meeting Notes


## Oct 31, 2022
### Attendees:
- Vani Rao
- Patrick Zheng
- Samir Kakkar
- Rakesh Gariganti
- Sajay Antony
- Shiwei Zhang
- Yi Zha 
- Feynman Zhou
- Toddy Mladenov
- Junjie Gao
- David Tesar


### Agenda Items:
- Great team work on Notation project beta.1 release. KUDOS! (Yi)
- Review [refactoring proposal](https://hackmd.io/nAV5ipF1TKyxFdrO7_75Mg?view) -- important for rc.1 release, at least 30 min needed (Yi)
### Notes:


## Oct 27, 2022
### Attendees:

### Agenda Items:
- Speed up the PR review for beta.1 release (2 days left for release), currently there are total 10 PRs in the [queue](https://cloud-native.slack.com/archives/C0412355BRT/p1666795341893509) (Yi)
### Notes:


## Oct 24, 2022
### Attendees:
- Vani Rao
- Samir Kakkar
- Rakesh Gariganti
- Sajay Antony
- Shiwei Zhang
- Yi Zha 
- Feynman Zhou
- Toddy Mladenov
- Junjie Gao
- David Tesar

### Agenda Items:
- Walk through PRs (Yi)
    - https://github.com/notaryproject/notation-go/pull/173
    - https://github.com/notaryproject/notation-core-go/pull/89
    - https://github.com/notaryproject/notation/pull/405
    - https://github.com/notaryproject/notation/pull/400
    - https://github.com/notaryproject/notation/pull/343
- Which team will do the implentation per the changes in [plugin spec](https://github.com/notaryproject/notaryproject/pull/194) (Yi)
- rc.1 call-out: (Yi)
    - Should we add "Notation supports OCI artifact" in rc.1?       ORAS-go v2.0.0-rc.4 release on Oct 31 will support OCI artifact.
    - Support of "--debug" option requires refactoring in notation-go (Proposal is under prepration)
    - Signing workflow is not fully compliant with spec, which was found during notation-go code review. Need to be fixed
    - Next step for issue [Using Verifier without a repository](https://github.com/notaryproject/notation-go/issues/143)
- Mark issues and PRs for beta.1 release based on the scope "verify using TS/TP + new CLI specs" (Yi)
- Finalize the [Alpha.4 Release Notes](https://github.com/notaryproject/roadmap/pull/65) and migrate all release notes to the website (Feynman)
- Work with Ratify on next steps and priortizing of https://github.com/deislabs/ratify/issues/274 after Notation beta-1 is available.

### Notes:
- Rakesh will help to review PRs 
- Bring OCI artifact support from ORAS-go v2.0.0-RC.4 post Notation v1.0.0-beta.1
- Create a GitHub issue to track the `--debug` option (there is an existing issue, I can add it later here.)
- Shiwei's team will share refactoring proposal by this week
- Create a GitHub issue to fix the problem of signing workflow is not fully compliant with spec
- Provide a proposal against Rakesh's comment to [Using Verifier without a repository](https://github.com/deislabs/ratify/issues/274)
- Samir will resolve the comments in [Alpha.4 Release Notes](https://github.com/notaryproject/roadmap/pull/65) and publish it on the Notary Website
- Good to consider nested verification when considering notation-go refactoring.  See [related ratify issue](https://github.com/deislabs/ratify/issues/351)
- Review the proposal of [pagination solution](https://github.com/notaryproject/notation/issues/403)

## Oct 20, 2022
### Attendees:
- David Tesar
- Smir Kakkar
- Vani Rao
 
### Agenda Items:
- Alpha4 testing Status - Any blockers or call out ? - Ratify consumes notation as code(depends on notation-go) not via cli. As per ratify’s go,mod they are using alpha1 of notation. For trust-store/trust-policy Ratify should use this function which will default trust store and trust policy location to notation’s location but we should test this with next release of Ratify.
- Define Beta1 Milestone - Based on the initial discussion as of 10/10/2022, this release will  include "verify using TS/TP" + new CLI specs - Tentatively end of this month.
- https://github.com/notaryproject/notation-go/pull/137 - Close pending discussions.
- Way forward for RC-1 release. We need to align on the issues list from GITHUB. Fill estimates for task assigned [notaryproject/projects/10/views/8](https://github.com/orgs/notaryproject/projects/10/views/8)
  - Working with Yi on the estimates - Vani / Pritesh
  - Discuss in the community call for all the “-1” which is yet to be estimated. Target RC-1 for 11/15 and call out if any blockers or concerns.
- [“COSE Spec” status]( https://github.com/notaryproject/notaryproject/pull/148) - ETA ?
- Offline/Local Signing experience Finalize next steps and rough estimation.
    - Discussion and alignment on support for “signing with local keys” https://github.com/notaryproject/roadmap/issues/15.
    - Separate the two issues “Content being local” vs “Key being local”. Content being local is not a blocker but key being local is a blocker. https://github.com/notaryproject/roadmap/issues/44 (edited) 
 
### Notes:
- Data versus Developer compatibility
- Ratify and discussion on do we want people to take dependency on notation-go
- We will release beta 1 at end of month, not call it alpha 5
- Try to target getting this PR merged before next dev release on Sunday. https://github.com/notaryproject/notation/pull/343

## Oct 17, 2022
### Attendees:

### Agenda Items:
- Issue: [Using Verifier without a repository](https://github.com/notaryproject/notation-go/issues/143)
- Issue: [System vs User file/directory precedence](https://github.com/notaryproject/notation/issues/203)
- Next release timeline?
- Offline signing UX proposal - https://hackmd.io/bwQx3LxHQHOrBpR-RRM8Qg?view
### Notes:


## Oct 13, 2022
### Attendees:
- Vani Rao
- David Tesar
- Pritesh Bandi

### Agenda Items:

- [[User Story] CLI Cmds for Trust Policy Management](https://github.com/notaryproject/roadmap/issues/39) I remember this US is not in rc.1, suggest to remove this from rc.1. Another suggestion is to add issue of OCI artifact support into rc.1 -- Yi
- alpha.4 is about to release on Oct 13 PST time. Since COSE Support is now in alpha.4, so Samir may need to update the release note accordingly. -- Yi
- Updated the status in notation planning board. In short, Shiwei's team will start to work on command implementation according to the updated spec, and this issue [Debug option](https://github.com/notaryproject/notation/issues/300), on which rough estimation al least 3 weeks effort. -- Yi
- Suggest to review and merge [PR 373](https://github.com/notaryproject/notation/pull/373) rather than [PR 370](https://github.com/notaryproject/notation/pull/370) for "verifying using TS/TP", since the code is already in dev-rc.1 branch with additional changes and already tested in dev-rc.1 branch. Sorry for missing the communication before last holiday week. Now it is just need to be merged back to main branch. -- Yi
- Added CLI help doc for Alpha.4 in [PR 384](https://github.com/notaryproject/notation/pull/384/files) and [PR 394](https://github.com/notaryproject/notation/pull/394/files), need to be reviewed before cutting Alpha.4 (Feynman)
- Alignment of the issues as part of RC-1 https://github.com/orgs/notaryproject/projects/10/views/8. Estimate for completion. (Pritesh/Vani)
- Discussion Threat model (Notary + Internal) https://github.com/notaryproject/notation/issues/391 (Pritesh)
- Notation sign/verify Tag to Digest translation  https://github.com/notaryproject/roadmap/issues/61 (Pritesh)
- Local key signing https://github.com/notaryproject/roadmap/issues/44 (lower priority) (Pritesh/Vani)
- Documentation - Multiple open issue; ReadME; hello world example
    - Website updation like official binary linking etc
    - Will be get Nate from CNCF?
- External Security Review ? (Discussion - Pritesh/Vani)

### Meeting Minutes:
- Fine to publish an updated alpha.4 release IF we can get the two CLI help PRs merged today (North America day time).  China team will release their daytime 10/14 with those two PRs if merged or not, so 10/14 morning NA time it is released.
- Ok to add COSE to release notes after release
- Pritesh added some items to [RC-1](https://github.com/orgs/notaryproject/projects/10/views/8), briefly reviewed on call and seem reasonable.  Some items might have already been in process by Shiwei's team.  Need to assign owners where there are none.
- Need to cleanup RC-1 issues backlog.  Many of the issues are closed, for instance COSE support. After this we need to have a sync with Vani/Yi/Samir/David about timelines for alpha.5 and RC-1 as well as trying to get into a more regular and smaller release cadence with a smaller set of scoped user stories which deliver end-user value.  This would ideally be out-of-band from community calls.
- Need to clarify what else we actually need for notary website with RC-1.  The RC-1 tagged issues are out of date. [Created this "epic"](https://github.com/notaryproject/notaryproject.dev/issues/77) to track in a single place.

## Oct 10, 2022
### Attendees:
- Patrick Zheng
- Yi Zha
- David Tesar
- Vani Rao
- Pritesh Bandi
- Samir Kakkar
- Milind Gokarnm

### Agenda Items:

- Enable the official release start from Notation Alpha.4 and disable the weekly dev build, see [proposal](https://github.com/notaryproject/notation/discussions/372) (Feynman)
- The [Notary documentation structure and content](https://notaryproject.dev/docs/) has been updated by Zach; We need to improve the user manual for KubeCon and RC.1 (Feynman)
- Feynman is updating the Notary release process doc and will provide a guideline for cutting alpha.4 (Feynman)
- Will Notation v1.0.0-alpha.4 work with AWS KMS? Can we provide a guide for users? (Feynman) --> not now or in time for KubeCon
- [PR review list](https://cloud-native.slack.com/archives/C0412355BRT/p1664336094452079) updated 
- Way forward https://github.com/notaryproject/notation/pull/370
- Walk through [rc.1 issue list](https://github.com/orgs/notaryproject/projects/10/views/8)

### Meeting Minutes:
- Cut the alpha-4 release now with the support for "self signed cert", and for use at KubeCon
- Alpha-5 will come with "Trust store and Trust Policy" support.
    - As soon as alpha-4 is released, we check in PR from Rakesh https://github.com/notaryproject/notation/pull/370 first, and then add any other changes on top
- In Thursday meeting we can discuss if items from RC-1 can be brought into Alpha-5.
- Lets rethink the [user/system level split](https://github.com/notaryproject/notation/issues/203)  It needs to be more simple/clear.
- Samir/Vani will cut alpha.4 release for notation-go (core-go is done). Yi/Feynman will release notation alpha.4 after dependency update PR merged including latest notation-go with alpha.4 and ideally removing notation-core-go dep if reasonable to easily remove.  If notation-core-go dep can't easily be removed, then put into file new issue.


## Oct 06, 2022
### Attendees:
- Vani Rao
- David Tesar
- Samir Kakkar
- Pritesh Bandi
- Nima Talebi
- Brian Lee

### Agenda Items:
- Alpha4 dev build for Oct 13, 2022 - GREEN - Any call outs ?
- Question from MSFT - [Notation Github Action](https://github.com/Duffney/notary-sign-action) consider moving to notaryproject repo as "notation-action"- Vani/ Steve commented in the notary v2 channel. (David/Pritesh/Vani).
- Go through RC1 stories/issues and call out any blockers. 

### Meeting notes


## Oct 03, 2022
### Attendees:
- Vani Rao
- David Tesar
- Samir Kakkar
- Pritesh Bandi

### Agenda Items:
Alpha 4 Release Task List - 10/13/2022 will be the Dev Build - Status is GREEN. 
- Alignment of Trust Store and Trust Policy in Alpha 4 (Pritesh/Feynman)
  - As per https://github.com/notaryproject/roadmap/issues/45, notation should perform signature verification using TS/TP and customer will manage TS/TP manually (on their own). – Pending Work for Alpha 4
- Alpha-4 release (10/13/2022) - David / Feyman / Samir / Vani
•	PR Priority List – Work in progress
    - https://github.com/notaryproject/notation-go/pull/137 dir package isolates read/write path 
    - ~~https://github.com/notaryproject/notation-go/pull/146 support cose envelope~~
    - ~~https://github.com/notaryproject/notation/pull/341 Add notation sign CLI spec~~
    - https://github.com/notaryproject/notation/pull/361 add CLI notation certificate and key specs 
    - https://github.com/notaryproject/notation/pull/362 add CLI specs for notation list/login/logout/plugin 
- Go through RC1 User Story / Issues and call out any blockers


### Meeting Notes:


## Sep 29, 2022
### Attendees:
- David Tesar
- Vani Rao

### Agenda Items:
- Re-Opened Story https://github.com/notaryproject/roadmap/issues/45 - Trust Store and Trust Policy in Alpha 4
- Testing of the Dev Build.
- Readiness to cut Release Alpha 4
- Call out if any blockers for RC-1, or any dependency on any development work for anyone to proceed.
- [Notation Github Action](https://github.com/Duffney/notary-sign-action) consider moving to notaryproject repo as "notation-action"
- Please review PRs in [order of priority](https://cloud-native.slack.com/archives/C0412355BRT/p1664336094452079)
- RC-1 high-priority item to consider - [local/offline signing](https://github.com/notaryproject/roadmap/issues/15)
 
## Sep 26, 2022
### Attendees:
- Pritesh Bandi
- Patrick Zheng
- Vani Rao
- David Tesar
- Yi Zha
- Feynman Zhou

### Agenda Items:
- Kudos to Pritesh and Shiwei's team for making big progress in PR review in a collaborative way. (Yi)
- Any update on PR review priority list? (Yi)
- Anything we need prioritzation and dependency consideration, since next week is public holiday in China. (Yi)
- Trust store and trust policy in alpha-4? (Pritesh)
    - It's been moved to RC-1

***Alpha 4 Release Task List** -* 09/30/2022 - Status is YELLOW Team to align across all the pending activities for Alpha4

- refactor: refactor pluginSigner to support new signature interface#131 - All reviews are completed. Waiting for MFT to merge. Post merge Pritesh to create a new PR. (Pritesh)
- Fix the certs validation in trust store - https://github.com/notaryproject/notation-go/pull/151 - COMPLETED (Pritesh)
- COSE envelope implementation - https://github.com/notaryproject/notation-core-go/pull/75 - 2 Pending reviews which is part RC-1 (Pritesh/Milind).
- Failed to sign images using self-signed certificates created from Key vault#320 - Yi is waiting on merge notaryproject/notation-go#147 and notaryproject/notation-go#131.  Use latest notation-go and notation-core-go and test. Yi to come back with the results. (Shiwei)
- Bump notation-go libraries for alpha-4 release#347 - David created and linked to  #357 which might resolve this issue. Once PR #357 is merged #347 will be automatically closed.Currently#357 is in draft. What is blocking ? (David)
-  Create v2.0.0.alpha-4.MD release notes #65 - verify (All) - Any questions can be commented on git.
- Release a new version of Notary V2 specification#183 - David modified the milestone to point to Alpha 4. (David)
- Testing Plugins prior to Alpha 4 Release. (Discussion)
- Any clarification or roadblock for RC-1 ? (Call Out)

## Sep 22, 2022
### Attendees:
- David Tesar
- Samir Kakkar
- Ian McMillan
- Pritesh Bandi
- 
### Agenda Items:
- Sorry for a long agenda item. I did a status update on notation planning board, there are 8 PRs to be reviewed or in-review, and 5 issues pending PR creations. If we spend one week on reviewing one PR in sequential, there will be at least 8+5 weeks, which means 3 months, then it will be next year. Not to mention there will be more PRs to be fired in upcoming weeks. How can we speed up to clean up the PR-review queue? Can we complete the existing 8 PRs by end of Sep? The following PR need to be reviewed and merged ASAP, since there are some refactoring code merged in notation-core-go these days, and the following one is for refactoring in notation-go. (Yi)
    *    https://github.com/notaryproject/notation-go/pull/131

#### Alpha 4 Release Task List - Status - GREEN Ready for the Alpha 4

*  	Cut Alpha 4 release on 09/23/2022 or 09/26/2022. 
    - Relax the certificate chain requirement to be compatible with the self-signing certificate. Complete the update to the Spec. https://github.com/notaryproject/notaryproject/pull/193. - COMPLETED
	- Build notation-go and notation core-go with the latest ORAS-GO lib changes. - COMPLETED

#### RC 1 Release Task List - Status - Yellow ( No Blockers called out - Yet to determine Release cutoff date)

o	Notation Sign experience https://github.com/notaryproject/roadmap/issues/40 
        - Yet to be reviewed by Yi/Milind/Pritesh. In Progress
o	As part of the user story https://github.com/notaryproject/roadmap/issues/41
        - Need feedback for the issue https://github.com/notaryproject/notation/issues/228 from Yi and Feynman. InProgress
o	Notation plugin extensibility to sign and verify - https://github.com/notaryproject/notation/issues/240
        - Reduced scope as part of the user story (https://github.com/notaryproject/notation/issues/193) - based on the Dir structure Spec document copy paste the plugin - Roughly 2 weeks. Yi/Shiwei- InProgress.
o	Validate if the implementation is sufficient for RC1 "Notation Plugin List - https://github.com/notaryproject/notation/issues/241 "-
The user story is here to ensure:
        - There is nothing missing/needed for what we're deeming RC-1.
        - That we're all on the same page that we want to support this for RC-1. 
            - Pritesh to verify - InProgress
o	Two main items from the user story https://github.com/notaryproject/notation/issues/230 need clarification. Steve
        - Validate if "Implementation of the new Plugin command" is in place.
        - Validate if we need additional story for the "Spec CLI Command" to modify and have visibility on the new plugin command.
        - Scope for Signer plugin - need to test and verify. Internal to AWS ONLY

o	Support COSE as signing envelope https://github.com/notaryproject/roadmap/issues/7. Yi to confirm if this is merged to the Main in the other cose branch. Review from Pritesh/Milind. - InProgress
o	Other items for RC-1, not covered by explicit user stories above.
        - CLI logging is part of RC1 (debug) https://github.com/notaryproject/notation/issues/300 - For notation client Sign and Plugin.
            - Logging framework in ORAS ? Need more discussion. Shiwei - In Discussion
        - Notation default signature format. Milind/Shiwei/Roy
            - COSE and JWS - Which format is default during signing.
o	One review pending for "Relax EKU requirements on signing certificates " - https://github.com/notaryproject/notaryproject/pull/167 - Milind
o	Threat Model - Larger team discussion.
o	External Pentest of Notation, decide if RC1 is the right time to do this. - Larger team discussion.
o	Complete revocation spec in RC-1

### Meeting notes
1. To help with the backlog of PR open for reviews, we need to establish a priortization mechanism. Before the Monday NV2 sync meeting, we must establish that prority list, ideally the friday before. Lets make it a recurring agenda item, and any person waiting on their PR must add it in the list.  We also discussed going back to utilizing the Monday evening calls for resolving high-priority PRs with goal to merge during call.  [PR Review criteria guidance still valid](https://github.com/notaryproject/notation/discussions/263) and suggestion for non-critical PRs where we don't necessarily need cross-org review to have same team quickly give two different code reviews so can merge no later than 1 week after approvals.  Made a minor suggestion to this guidance in that discussion thread.
2. Before Alpha-4 is released, need to test https://github.com/notaryproject/notation/issues/320 is now working. We created a new alpha-4 milestone
3. Vani and Samir will work with Yi and Feyman, on doing the alpha-4 release  steps  before or during the 9/26/2022 call.
4. Pen Test and Threat Modeling. Want to do it as part of RC-1, but is this a must have will require further discussion.  David proposed it being after RC-1 as COSE already has this testing and it will cause likely significant delays to RC-1.
5. Ian is going to sync up with David to fix the DCO issue on the [minor spec PR](https://github.com/notaryproject/notaryproject/pull/167).  Agreed we should just merge this after that is resolved.


## Sep 19, 2022
### Attendees:
- Yi Zha
- Feynman Zhou
- Samir Kakkar
- Pritesh Bandi
- Shiwei Zhang
- Patrick Zheng
- Josh Duffney
- Sajay Antony
- Milind Gokarnm
- Roy Williams


### Agenda Items:
- COSE PR review
    - Pushing review on refactor PR [#76](https://github.com/notaryproject/notation-core-go/pull/76): Once this PR is merged, Stage/cose branch will be rebased and merged to main since JWS refactoring is done.
- Confirm the rc.1 scope

**Alpha 4 Release Task List** Status : Green
* Relax the  certificate chain requirement to be compatible with the self-signing  certificate. Complete the update to [[the Spec](https://github.com/notaryproject/notaryproject/pull/193)] - Spec approved by David
* Implementation of  the self-sign certificate changes, ETA will be 09/22/2022. Review is in progress for https://github.com/notaryproject/notation-core-go/pull/77
* Build notation-go  and notation core-go with the latest ORAS-GO lib changes.
* Cut Alpha 4  release on  09/23/2022 or  09/26/2022. Group alignment.



**RC 1 Release Task List** Status : TBD based on scope and planned release date
- ***Status of [user Stories for RC-1]***(https://github.com/orgs/notaryproject/projects/10/views/10)
    * Review and add any comments  on the proposal of using CLI to manage trust store published by Yi. https://hackmd.io/@yizha1/cli_trust_store - Pritesh/Milind. InProgress
        * Configuring Trust Store in  notation and CLI work for Trust Store https://github.com/notaryproject/roadmap/issues/38. Once the  review of CLI spec for Trust store is completed by all of us, Patrick Zheng  to implement trust store CLI commands. -  InProgress
    * Notation Sign experience https://github.com/notaryproject/roadmap/issues/40 . To be reviewed by Yi/Milind/Pritesh. InProgress
    * As part of the user story https://github.com/notaryproject/roadmap/issues/41
        * Need feedback for this issue https://github.com/notaryproject/notation/issues/228 from Yi and  Feynman. InProgress
    * Notation plugin extensibility  to sign and verify https://github.com/notaryproject/notation/issues/240
        * Reduced scope as part of the  user story (https://github.com/notaryproject/notation/issues/193) - based on the Dir  structure Spec document copy paste the plugin - Roughly 2 weeks. Yi/Shiwei-  InProgress.
    * Validate if the  implementation is sufficient for RC1 "Notation Plugin List - https://github.com/notaryproject/notation/issues/241 ". The user story is here to ensure:
        * There is nothing  missing/needed for what we're deeming RC-1.
        * That we're all on the same  page that we want to support this for RC-1. 
        * Pritesh to verify -  InProgress
    * Two main items from the user  story https://github.com/notaryproject/notation/issues/230 need clarification. Steve
        * Validate if  "Implementation of the new Plugin command"  is in place.
        * Validate if we need  additional story for the "Spec CLI Command" to modify and have  visibility on the new plugin command.
    * Support COSE as signing envelope https://github.com/notaryproject/roadmap/issues/7. Yi to confirm if this is  merged to the Main in the other cose branch. Review from Pritesh/Milind. -  InProgress

* ***Other items for RC-1, not covered by explicit user stories above.****
    * CLI logging is part of RC1  (debug) https://github.com/notaryproject/notation/issues/300 - For notation client Sign  and Plugin.
        * Logging framework in ORAS ?  Need more discussion. - Shiwei -  In Discussion
    * Notation default signature  format. Milind/Shiwei/Roy
        * COSE and JWS - Which format  is default during signing.
    * One review pending for  "Relax EKU requirements on signing certificates " - https://github.com/notaryproject/notaryproject/pull/167 - Milind
    * Threat Model - Larger team  discussion.
    * External Pentest of Notation,  decide if RC1 is the right time to do this.  - Larger team  discussion.
    * Complete revocation spec in RC-1
 
**Task List Post RC1 Release**
* No  objections to moving implementation of revocation feature to RC2, we'll  complete spec in RC1
* No  objections to moving TSA support to post RC1. This will impact scenarios  where short lived certs are used. 
* Implementation of Trust policy for CLI commands to RC2. https://github.com/notaryproject/roadmap/issues/39
* Two issues for  notation to support OCI reference type, as following: (No action listed -  Build to be done with the updated dependencies)
    * notation-go repo: https://github.com/notaryproject/notation-go/issues/136
    * notation CLI repo: https://github.com/notaryproject/notation/issues/33 (https://github.com/notaryproject/notation/issues/335)5
* The issue of  supporting OCI reference type tracked in ORAS-go is https://github.com/oras-project/oras-go/issues/271, which is  included in ORAS-go milestone v2.0.0-rc.4 planned in late Oct 2022.


**Miscellaneous Tasks**
* Junjie need the following  clarification (requested on 09/13/2022) - Who is helping ? The go version  has been updated to 1.19 for notation and 1.18 for notation-go and  notation-core-go, but our Github CI required check need go 1.17 to be  built, which blocks the PR to be merged. Can someone with repo admin  privilege help to cancel the go 1.17 required check for us? - More Context  on this blocker.
* Gated release process via GH  actions where # of maintainers must approve - David. 


### Meeting Notes
- We covered the next steps on two user stories, "[Trust Stores CLI Cmd](https://github.com/notaryproject/roadmap/issues/38)" and "[Sign Cmd](https://github.com/notaryproject/notation/issues/91)"
- Live discussion on refactor PR [#76](https://github.com/notaryproject/notation-core-go/pull/76
- We agreed to create seperate issues for RC-1 for items that are not expressely covered by user stories ( all items in the above agenda . 
- We agreed to trial using the "comments" coulmn in "Notation Planning" project to track last updates Vs putting them in the list of Agenda items

## Sep 15, 2022

### Attendees:
- David Tesar
- Samir Kakkar
- Milind Gokarn
- Roywill
- Pritesh

### Agenda Items:

**Alpha 4 Release Task List**
- Relax the certificate chain requirement to be compatible with the self signing certificate  , Complete the update to the spec https://github.com/notaryproject/notaryproject/pull/193.
- Implementation of the self-sign certificate changes, ETA will be 09/22/2022. PR is raised.
- Build notation-go and notation core-go with the latest ORAS-GO lib changes.
- Cut Alpha 4 release on  09/23/2022 or 09/26/2022. Community alignment.

**RC 1 Release Task List**
•	Notation Sign experience https://github.com/notaryproject/roadmap/issues/40
•	Use an extensible plugin to sign and verify the artifacts https://github.com/notaryproject/notation/issues/240
•	Notation Plugin List https://github.com/notaryproject/notation/issues/241. Ensure there is nothing missing for RC-1 and the community alignment and confirmation. Conclude the next steps for https://github.com/notaryproject/notation/issues/230
•	Review proposal of using CLI to manage trust store published by Yi https://hackmd.io/@yizha1/cli_trust_store 
•	Configuring Trust Store in notation and CLI work for Trust Store https://github.com/notaryproject/roadmap/issues/38. Yi has CLI spec for Trust store.
•	Support COSE as signing envelope https://github.com/notaryproject/roadmap/issues/7. Is this confirmed for RC-1
•	CLI logging is part of RC1 (debug) - Conclude if anything here.
•	Should this user story be removed since both trust store and trust policy are tracked separately https://github.com/notaryproject/roadmap/issues/41
•	Notation default signature format.
•	External Pentest of Notation, decide if RC1 is the right time to do this.
•	Two issues for notation to support OCI reference type, as following: (No action listed - Build to be done with the updated dependencies)
•	notation-go repo: https://github.com/notaryproject/notation-go/issues/136
•	notation CLI repo: https://github.com/notaryproject/notation/issues/335
•	The issue of supporting OCI reference type tracked in ORAS-go is https://github.com/oras-project/oras-go/issues/271, which is included in ORAS-go milestone v2.0.0-rc.4 planned in late Oct 2022.
 
**Task List Post RC1 Release**
•	Revocation feature implementation will be added in RC2, we'll complete spec in RC1
•	TSA support will be added post RC1. This will impact scenarios where short lived certs are used. 
•	Implementation of Trust policy for CLI commands to RC2. https://github.com/notaryproject/roadmap/issues/39


**Miscellaneous Tasks**
•	Junjie need the following clarification (requested on 09/13/2022) - Who is helping ? The go version has been updated to 1.19 for notation and 1.18 for notation-go and notation-core-go, but our Github CI required check need go 1.17 to be built, which blocks the PR to be merged. Can someone with repo admin privilege help to cancel the go 1.17 required check for us?
•	Gated release process via GH actions where # of maintainers must approve




## Sep 12, 2022

### Attendees:
- Roywill
- Milind Gokarn
- Yi Zha
- Feynman Zhou
- Steve Lasker
- Samir Kakkar
- Vani Rao
- Shiwei Zhang

### Agenda Items:
1. Next steps for alpha-4 /alpha-3-patch? Any remaining updates to release process? With oras-go v2.0.0-rc.3 released just waiting on support for [self signed cert](https://https://github.com/notaryproject/notaryproject/issues/192).
1. Estimates for "migrate to OCI artifact from ORAS artifact"(Library that will work with OCI Spec).  Shiwei/Yi/Milind
    - Readiness for RC.1 - Work to be done in ORAS-go. [oras-go #271](https://github.com/oras-project/oras-go/issues/271)
    - Finalize the ORAS library commands.
1. PR [#73](https://github.com/notaryproject/notation-core-go/pull/73) notation-core-go refactor
    - Branches
        - `stage/cose`: stage changes to be merged to `main`
        - `cose` for working COSE envelope
    - Full PRs:
        - https://github.com/notaryproject/notation-core-go/pull/26
        - https://github.com/notaryproject/notation-core-go/pull/68
    - Related PRs:
        - notation-go: https://github.com/notaryproject/notation-go/pull/131
1. Walkthrough all the user story readiness for RC.1 and its timeline.
1. (If needed) Close out on [diagnostic logging scope RC.1](https://github.com/notaryproject/notation/issues/300#issuecomment-1240938829)
1. (If needed) Close out on [E2E CLI testing scope RC.1]()
1. Review the test results for stability of RC.1
1. (If Needed) [TSA](https://github.com/notaryproject/notation-go/issues/78) - consider just 1&2 in scope RC.1, 3&4 RC.2
1. Trust Store  & Trust Policy Milind walkthrough --> Discuss cli experience for RC.1
1. [CLI maturity](https://hackmd.io/@yizha1/notation_cli_status)
    - Cache
    - Push/Pull
    - List
1. Signature revocation - Need to align on plan even if no implemention in Notation for RC.1



## Sep 8, 2022
### Attendees:
- David Tesar
- Nima Talebi
- Vani Rao
- Milind Gokarn

### Agenda Items:
- Align and conclude notation rc.1 release scope and ETA(release date), see [Proposal](https://hackmd.io/@yizha1/notation_rc1_plan). We can add comments in this proposal link, once we are aligned, we can update the GitHub milestones. (Yi)
- Align the work for sign and verify CLI experiences (Yi)
    - see the proposal in [comment](https://github.com/notaryproject/notation/issues/91#issuecomment-1240335267)
    - Review [CLI maturity](https://hackmd.io/@yizha1/notation_cli_status)
- Include diagnostic logging in RC.1 feature set. efine what type of logging and the estimate.
- 

## Sep 6, 2022
### Attendees:
- Yi Zha
- Feynman Zhou
- Steve Lasker
- Samir Kakkar
- Vani Rao
- Roy Willimas
- David Tesar
- Milind Gokarnm
- Shiwei Zhang


### Agenda Items:
- Align Notation rc.1 release content with effort estimate for all in scope user stories [RC-1-UserStories](https://github.com/orgs/notaryproject/projects/10/views/10) in the notatary-plan board.
- Procedural cadence for the release. Define roles and responsibilities. Ex: Approval for release cut after submitting test results and release notes - Members from Maintianers group (https://github.com/orgs/notaryproject/teams/notaryproject-org-maintainers/members)
- Notation plans for supporting OCI spec. Migrate to OCI Artifact from ORAS Artifact. (https://github.com/oras-project/oras-go/issues/271)
- Next Steps for Alpha 4/Alpha 3-Patch.
- As part of rc.1, we need to document the APIs.
- Ensure all items for rc.1 have an assigned owner.

### Meeting Notes
- Shiwei and Milind reviewed the open PRs 
- Alpha-4/Alpha-3-patch is gated on having support for "self signed certificate" and "oras-go rc.3 release"
- Reviewed the proposed RC-1 release content
    - Milind requested bringing in diagnostic logging in RC-1
    - Milind pointed out the CLI commands for trust policy will be significant effort
    - Milind clarified that sign and verify commands needs spec and implementation.
    - We will break out trust store and trust policy work seperately
    - Samir asked for inclusion of https://github.com/notaryproject/notation/issues/300 in RC-1
    - Steve will get data on the open items in OCI-reference spec and Shiwei will help us get a scope estimate for (https://github.com/oras-project/oras-go/issues/271)

- Will use automated end to end test cases to ensure quality releases.

## Sep 1, 2022
### Attendees:
- Jared Stein (MSFT)
- Samir Kakkar
- Nima Talebi

### Agenda Items:
- Any more review comments from Rekesh on PR [notation-core-go#53](https://github.com/notaryproject/notation-core-go/pull/53). This PR will be merged this week according to PR review process. (Yi)
- Align Notation rc.1 release date, the proposal is to release rc.1 by end of Sep, and the scope of user stories is as [RC-1-UserStories](https://github.com/orgs/notaryproject/projects/10/views/10) in the notatary-plan board (Yi)

### Meeting Notes
- PRs are still in review
- Lets add the scope effort for all items in RC-1, and then we can better estimate the date
- FYI : [ORAS-go v2.0.0-rc.3](https://github.com/oras-project/oras-go/milestone/8) release date is ~~8/31~~ 9/5 

## Aug 29, 2022
### Attendees:

- Yi Zha
- Feynman Zhou
- Steve Lasker
- Libinbin
- Rakesh Gariganti
- Samir Kakkar
- Niaz Khan
- Vani Rao

### Agenda Items:

- Review
    - PR [notation-core-go#53](https://github.com/notaryproject/notation-core-go/pull/53)
    - Pritesh's question answered at discussion [notation#278](https://github.com/notaryproject/notation/discussions/278)
- Spec conflicts [notaryproject#189](https://github.com/notaryproject/notaryproject/issues/189)
    - [signing-and-verification-workflow.md](https://github.com/notaryproject/notaryproject/blob/main/signing-and-verification-workflow.md#signing-steps) verifies the certificate chain **before** signing (steps _1.i_ and _1.iii_).
    - [specs/plugin-extensibility.md](https://github.com/notaryproject/notaryproject/blob/main/specs/plugin-extensibility.md#signing-workflow-using-plugin) verifies the ceritifate chain **after** signing (steps _5.i.c_ and _5.i.d.c_).
- Align Notation rc.1 scope(feature level) and target date (Yi)
- Alpha-3 patch for pulling in "oras-go" upate for https://github.com/oras-project/oras-go/pull/237, and doing a system release of Notar v2 (Vani/Samir)

### Notes:

- Rakesh to review the PR [notation-core-go#53](https://github.com/notaryproject/notation-core-go/pull/53)
- Rakesh to reply to issue [notaryproject#189](https://github.com/notaryproject/notaryproject/issues/189) and help to resolve the spec conflicts 
- We will announce alpha-3 after the ORAS-go latest release 2.0.0.rc_3 ( due 8/31) is brought into an alpha-3 patch release
- Need to ensure the alpha-3-path ( or alpha-4) release is usable end to end
- For COSE to be a part of RC-1, need to understand the scope.
- OCI WG reference spec implementation work in ORAS-GO, should be a part of RC-1.
- Need to define our release process to ensure maintainers approve a release. Need to define test caes and ensure they are passing before release
- Yi will create a bug issue for the alpha-3 issue blocking signing/verifying end to end workflow
- Samir/Pritesh to merge  PR to allow a self signed cert (not insist on a certificate chain)

## Aug 25, 2022
### Attendees:
- Pritesh Bandi
- Nima Talebi
- Vani Rao
- Milind Gokarn
### Agenda Items:
- What's the purpose of notation-core-go refactoring? (Pritesh) Need more elaboration on the discussion  https://github.com/notaryproject/notation/discussions/278
- Discuss the governance control for release.(Niaz).
- Reply to Pritesh's item, Binbin provided more information in GitHub discussion, please take a look, let us know any other questions. Due to time difference, it's hard to join the community morning meeting, but we could try using slack or Github for an offline discussion as well. Feel free to ping us if needed. (Yi)
- I cannot join the morning meeting due to timezone, but I would like to kick off the discussion for roadmap. Please provide your feedback on the following items (Yi)
    - Align Notation rc.1 scope(feature level) and target date.
    - The milestones post rc.1, what is the scope and timeline for rc.2, rc.x, 1.0.0 GA release
    - Proposal: Can we book a dedicate timeslot to review the existing issues in roadmap repo, and make a release plan accordingly, we could review and update the release plan every month or other candence?

### Notes
- 
- 

## Aug 22, 2022
### Attendees:
- Milind Gokarnm
- Nima Talebi
- Pritesh Bandi
- Shiwei Zhang
- Vani Rao
- Sajay Antony
- Yi Zha
### Agenda Items:
- What's the purpose of notation-core-go refactoring? (Pritesh) Need more elaboration on the discussion  https://github.com/notaryproject/notation/discussions/278
- Milind to clarify this issue [Define experience for notation sign command #91](https://github.com/notaryproject/notation/issues/91) (Yi)
- What is left for issue [Relax EKU requirements on signing certificates #167](https://github.com/notaryproject/notaryproject/pull/167) (Yi)
- Nima need help driving the ORAS issue to closure https://github.com/oras-project/oras-go/pull/237 and doing the release of oras-go. (Samir/Vani).
- Discuss the governance control for release.(Niaz).

### Notes
- Shiwei to update signing alg to verbose names
- Milind to open a issue for changing keyId to keyName
- Milind to open an issue to simplify `generate-signature` such that keyspec->signing alg mapping is done by Notation instead of every plugin
- Nima is adding unit tests for fixing [empty response Docker-Content-Digest](https://github.com/oras-project/oras-go/pull/237) in ORAS-go. Shiwei and Sylvia will help to review this PR later
- Release ORAS-go and ORAS CLI after the issue [empty response Docker-Content-Digest](https://github.com/oras-project/oras-go/pull/237) is resolved, then apply it in Notation

## Aug 18, 2022
### Attendees:
- David Tesar
- Samir Kakkar
- Milind Gokarnm
- Pritesh Bandi
- Shiwei Zhang
- Vani Rao


### Agenda Items:
- For alpha-3:
    -  Need alignment on the version numbering
    - Updating the https://github.com/notaryproject/notation/blob/main/RELEASE_CHECKLIST.md process to capture dependencies (notation-core-go -> notation-go -> notation) and (oras-go -> notation-go); 
    - And releasing each repo with version or not (https://github.com/notaryproject/notation-go/pull/111)
    - Progress on https://github.com/oras-project/oras-go/pull/237 for registery interop .. PR in progress
- Post alpha-3:
    - https://github.com/notaryproject/notaryproject/issues/163 

### Notes
- Our release process needs to be well documented. The current process does not apply to all repos
- We will do another alpha  (or patch) release before RC-1 to include the PRs
- Milind/Pritesh provided feedback on PRs by Shiwei
    - https://github.com/notaryproject/notaryproject/pull/185
    - https://github.com/notaryproject/notaryproject/pull/186
    - https://github.com/notaryproject/notaryproject/pull/187
- Shiwei/David: To identify signatures envelope (COSE or JWS) there are two use cases
    - Signature coming from local storage where we don't have the manifest to tell us the signature envelope type
    - Signature being pulled from registry, there we have the "media-type"
    - Additionally, there could different verions of a signature envelope ( e.g. COSE could have multiple formats) Action Item: @shizh / @david to create an issue
        - Pritesh: versioning for a particular signature format be left to the format. Example - JWS does it by using ‘cty' header
- Action items
    -  Samir update the System release (aka roadmap repo) notes for alpha-3 PR with the new version numbering
    -  Samir create an issue with third party library
    -  David to update Release checklist for all repos.
    -  Samir/Milind 



    
    

## Aug 15, 2022
### Attendees:


### Agenda Items:
- alpha 3: still two PRs not merged: [#104](https://github.com/notaryproject/notation-go/pull/104) and [#294](https://github.com/notaryproject/notation-go/pull/294), if not merged, notation sign and verify won't work. (Yi)
- alpha 3: addtional issue [#97](https://github.com/notaryproject/notation-go/pull/97) (go-ldap/ldap upgraded from 3.4.3 to 3.4.4) reported by dependabot 15 days ago, recommend to merge it (Yi)
- alpha 3: Let Yi release notation-go, since there are release dependencies: notation CLI -> notation-go -> notation-core-go (Yi)
- [Revise plugin extensibility spec by Shiwei](https://github.com/notaryproject/notaryproject/pull/185)
 

### Notes

## Aug 11, 2022
### Attendees:
- Steve Lasker (Microsoft)
- Milind Gokarnm
- Vani Rao
- Samir Kakkar

### Agenda Items:
- Finalize the [Release notes for Alpha 3](https://github.com/notaryproject/roadmap/pull/64) and update on remaining open items if any. (Samir)
- Documentation of the Release Process. (Samir)
    - [RELEASE_CHECKLIST.md](https://github.com/notaryproject/notation/blob/main/RELEASE_CHECKLIST.md)
    - David recorded the process on ~May 31st, 2022
    - Steve to look up recordings and post them
    - [May 31, 2022 - including release process from David](https://youtu.be/HvmjvS2nzPk) release process at 59:52
- Need approval for Samir's request to add 'Vani Rao' to maintain release from GitHUB -https://github.com/orgs/notaryproject/teams/notation-release-managers/discussions.
    - Completed
- [fix: dir package optimize #104](https://github.com/notaryproject/notation-go/pull/104) needed for Alpha 3 (Steve)
- [fix: update notation-go #294](https://github.com/notaryproject/notation/pull/294) needed for Alpha 3 (Steve)
    - Would like to be date driven for Alpha-3, cutting Friday
- [ecr: oras pull error: empty response Docker-Content-Digest #225](https://github.com/oras-project/oras-go/issues/225) Reminder for ECR folks (Steve)
    - Milind following up with Michael
- https://github.com/notaryproject/notation/discussions/299#discussioncomment-3374337 ( Samir)


## Aug 08, 2022
### Attendees:
- David Tesar
- Samir Kakkar
- Milind Gokarnm
- Roy Williams
- Yi Zha
- Feynman Zhou
- Shiwei Zhang
- Sajay Antony
### Agenda Items:
- Security issue [signature verification](https://github.com/notaryproject/notation/discussions/278) found by Shiwei
- Agree on Way forward for [issue#268](https://github.com/notaryproject/notation/issues/268). The proposal is to fix the issue according to existing spec, and then release alpha.3. The reason is updating spec takes time for PR reivew, and COSE support also need to update the spec, so we can wait for COSE implementation to update the spec in upcoming weeks.
- 
### Notes
- Security issue was discussed. Milind will create a PR to address it.
- We reached a consensus on this issue#268, that is, go ahead releasing alpha.3 with existing spec. Shiwei will create a separate PR based on COSE PR to formally fix both the spec and implementation.
- Besides the above we did Q&A on the plugin spec.
    - Proposal of changing the payload to digest of payload in the request contract for generating signature. need further discussion.
    - Proposal of changing the response contract for generating signature. We reached a consensus.
    - Millind brought up a [discussion](https://github.com/notaryproject/notation/discussions/278), which will be moved to next community call, since this discussion issue will be updated soon.
- Alpha.3 release is delayed to end of this week, since there is a new issue reported, and some PRs are not merged yet.

## Aug 04, 2022
### Attendees:
- David Tesar
- Samir Kakkar
-  Pritesh Bandi
-  Vani Rao
-  
### Agenda Items:
- Review of alpha-3 milestone. Pending items and ETA
- PR of alpha-3 release notes
- Effort estimates for RC-1 items

### Notes
- David, start with creating issues in each "Repo" to start our release process for alpha-3.
- 


## Aug 1, 2022

### Attendees:
- Yi Zha
- Samir Kakkar
- Milind Gokarnm
- Pritesh Bandi
- Sajay Antony
- Steve Lasker
- Feyman Zhou
- David Tesar
- Shiwei Zhang
- Roy Williams

### Agenda Items:
- PR review - Update COSE support spec: https://github.com/notaryproject/notaryproject/pull/179
- The three open issues in https://github.com/notaryproject/notation/issues/93, are they still needed?
- Requesting more details on "CodeCov" bot
- Requesting more details on https://github.com/orgs/notaryproject/projects/10/views/17
- Update on all items open for alpha-3. What are the remaining blockers for alpha-3 ? 
- Proposal of creating user story of COSE support in notationproject/roadmap repo as roadmap [#38](https://github.com/notaryproject/roadmap/issues/38)
- [go-cose security review](https://github.com/veraison/go-cose/tree/main/reports)

### Notes


## July 28, 2022

### Attendees:
- David Tesar
- Samir Kakkar

### Agenda Items:
- Bring completed (or in flight items such as those pending PR review) into alpha-3 (Samir)

### Notes
- David and Samir moved all "done" and relevant "in-progress" items into Alpha-3 ( Refer [here](https://github.com/orgs/notaryproject/projects/10/views/4?filterQuery=milestone%3A%22alpha-3%22+-is%3Aclosed&sortedBy%5Bdirection%5D=asc&sortedBy%5BcolumnId%5D=Status )), based on the draft releases notes content (Refer [here](https://hackmd.io/LLCH4EcOTaaxlaJk0ZdVfA ))

## July 25, 2022

### Attendees:
- David Tesar (Microsoft)
- Yi Zha
- Samir Kakkar
- Milind Gokarnm
- Pritesh Bandi
- Feynman Zhou
- Niaz Khan
- Sajay
- Shiwei Zhang

### Agenda Items:

- Review pending PRs
    - https://github.com/notaryproject/notation/pull/255
    - https://github.com/notaryproject/notation-go/pull/87
    - https://github.com/notaryproject/notation/pull/256
- Notary planning board updates (Most of issues have assignees now)
- Create a review process guide and onboard new qualified maintainers
- Review the proposal on weekly build for Notation https://github.com/notaryproject/notation/discussions/261
- Review draft alpha-3 release notes at https://hackmd.io/LLCH4EcOTaaxlaJk0ZdVfA?both 
- Notation CLI support for Timestamp Authority signatures: https://github.com/notaryproject/roadmap/issues/59#issuecomment-1193795172


### Notes
- Multiple PRs are out for review. Milind will propose the [draft rules](https://github.com/notaryproject/notation/discussions/263) for review of code PRs, where two code reviews and one of the maintainers from "Code-review" group will be required
- Lets do weekly builds for Notation client, and use the dd-mm-yy or mm-dd-yy format for the release. Lets keep it simple.
- For anything in the roadmap repo, whoever has it assigned, could they close any duplicates in another repo, and/or link to the roadmap item. Keep the roadmap item open, until we get maintainers to close it. Going forward, roadma repo should only have high level user stories and not granular/implementation items. Refer example here. https://github.com/notaryproject/roadmap/issues/38 
- Alpha-3 discussion . Any items marked for RC-1 which is completed, or will be completed at time of alpha-3, should be included in alpha-3.
- The existing commands for certiicates CRUD are not compatiable with the new Trust store (directory based) design. For alpha-3, we should not wait on fixing this. Before deciding to include this in RC-1, lets first define the behaviour we want for the Certification CLI command before starting implementation. 

## July 21, 2022

### Attendees:
- David Tesar
- Steve Lasker
- Samir Kakkar
- Rakesh Garigant
- Milind Gokarnm
- Pritesh Bandi
- Niaz Khan
- Vani Rao


### Agenda Items:
- [Support multiple trust stores and custom verification level #164](https://github.com/notaryproject/notaryproject/pull/164) (Milind)
- [Verification Plugins #165](https://github.com/notaryproject/notaryproject/pull/165) (Milind)
- Complete evaluation of "Discuss" milestone items. (Samir/David)
- Alpha-3 release date before RC-1 release date

### Notes:
- Milind will update PR based on the feedback
- Alpha-3 will be the next milestone. RC-1 will come after that.
- Samir and David will propose what goes in Alpha-3 ( what all user stories to support). Will adjust its scope definition accordingly in https://github.com/notaryproject/roadmap

## July 18, 2022

### Attendees:
- David Tesar (Microsoft)
- Steve Lasker (Microsoft)
- Yi Zha
- Sajay Antony
- Samir Kakkar
- Rakesh Garigant
- Milind Gokarnm
- Pritesh Bando
- Roy Williams
- Feynman Zhou

### Agenda Items:
- [Ready to close release candidate signature format](https://github.com/notaryproject/notaryproject/issues/105)
- [Consider dropping docker-* commands](https://github.com/notaryproject/notation/discussions/251)
- PR [Signing Scheme #175](https://github.com/notaryproject/notaryproject/pull/175) and [Verification Plugins #165]
- PR [Support multiple trust stores and custom verification level](https://github.com/notaryproject/notaryproject/pull/164) (Milind)
- [Discuss in/out scope user-stories for RC-1](https://github.com/orgs/notaryproject/projects/10/views/7?filterQuery=is%3Aopen+label%3A%22User+Story%22) (David & Samir)
- Alpha 3 milestone consideration (David & Samir)
(https://github.com/notaryproject/notaryproject/pull/165) (Milind)

### Notes:
- - [closed as JWS for RC-1 signature format](https://github.com/notaryproject/notaryproject/issues/105)
- - [Dropped docker-* commands for initial/RC-1 release. Will revisit if and when a need arises](https://github.com/notaryproject/notation/discussions/251)

- 



## July 14, 2022

### Attendees:
- Niaz Khan
- David Tesar
- Steve Lasker
- Samir Kakkar
- Roy Williams
- _add yourself_

### Agenda Items:

- Notary RC1 scope (Samir and David)
- PR [Signing Scheme #175](https://github.com/notaryproject/notaryproject/pull/175) and [Verification Plugins #165](https://github.com/notaryproject/notaryproject/pull/165) (Milind)
- PR [Support multiple trust stores and custom verification level](https://github.com/notaryproject/notaryproject/pull/164) (Milind)
- [cose signature format inclusion](https://github.com/notaryproject/notaryproject/issues/117#issuecomment-1184580286) (Steve)
- _add your topics_

### Notes:
- _meeting minutes_

### Notes:

## July 11, 2022

### Attendees:
- David Tesar
- Sajay Antony
- Feynman Zhou
- Yi Zha
- Steve Lasker
- Niaz Khan
- Roy Williams
- Ramkumar Chinchani
- Samir Kakkar
- Milind Gokarn
- Rakesh Gariganti
- Pritesh
- _add yourself_

### Agenda Items:
- [Verification Plugins #165](https://github.com/notaryproject/notaryproject/pull/165) - h2 enable flexibility and cross instance stability for verification? (Steve)
- [Review #PR 218: support notation login](https://github.com/notaryproject/notation/pull/218) (Shiwei)
- PR [Support multiple trust stores and custom verification level](https://github.com/notaryproject/notaryproject/pull/164) (Milind)
- [Change targetArtifact to subject, consistent with the artifact spec #169](https://github.com/notaryproject/notaryproject/pull/169) - accidently merged before additional reviews. Revert or keep (Steve)
- notation user stories on planning board (David & Feynman)
- [notation milestones](https://github.com/notaryproject/notation/milestones) alphas & rcs (Steve)


### Notes:
- Continue disucssion on verification plugin extensibilty offline

## July 7, 2022

### Attendees:
- Iam McMillan
- Milind Gokarnm
- Rakesh Gariganti
- Pritesh
- Samir Kakkar
- Ivan Wallis
- David Tesar
- Steve Lasker
- Niaz Khan

### Agenda Items:

- EKU Discussion, use of various signing certs (Ian McMillan)
- Close on migration off of spreadsheet (David)
- Triage RC-1 items on board (David/Samir)
- Triage alpha.2 and alpha.3 items on board (David/Samir)
- Cover new user story proposals for RC-1 (David)
- [Support multiple trust stores and custom verification level](https://github.com/notaryproject/notaryproject/pull/164) (Milind)
- [Verification Plugin and Signing Scheme spec](https://github.com/notaryproject/notaryproject/pull/165)(Milind)
- Unresolved discussions on implementation PRs (Milind)

## July 5, 2022

### Attendees:
- David Tesar
- Samir Kakkar
- Milind Gokarn
- Rakesh Gariganti
- Feynman Zhou
- Jesse Butler
- Pritesh
- Roy Will
- Sajay Antony
- Yi Zha
- Niaz Khan
- Steve Lasker

### Agenda Items:

- Clarity on [code signing EKU cert requirement](https://github.com/notaryproject/notaryproject/issues/157)
- Proper spec location(s) and inspect spec - (Yi Zha)
- [Where is Verify Spec?](https://github.com/notaryproject/notation/issues/216)
- Clarify `recommended` vs. `required` in [Notation Directory Structure](https://github.com/notaryproject/notation/blob/main/specs/directory.md#notation-directory-structure) (Steve)
- Trust policy updates [PR](https://github.com/notaryproject/notaryproject/pull/164) (Milind)

### Meeting Notes:
- [Verify Spec](https://github.com/notaryproject/notaryproject/blob/main/trust-store-trust-policy-specification.md#signature-verification)
- The rationale of seperating the Notation Specs in Notation repo Vs putting all the specs in notaryproject repo, is to keep Notation specific details with its implementation.
- System-level directories are required.  User-level directories are recommended.  The defaults vary based on operating system.
- id-kp-codeSigning discussion will be continued in next meeting. 
- User expereince should not change after RC-1 is released. Applying this tenet to CLI imply - "The CLI commands and sub options we agree and approve should be the only ones supported in Notation"
- Milind provied an overview of two PRs he requested for approval/review

## June 30, 2022

### Attendees:
- Steve Lasker
- David Tesar
- Milind Gokarn
- Rakesh Gariganti
- Pritesh

### Agenda Items:
- Upcoming spec updates (Milind)
    - Specify multiple trust stores in policy
    - Custom verification level
    - Directory based config precedence  ([#203](https://github.com/notaryproject/notation/issues/203))
- Task status updates (Milind)
- [Code reviewers group](https://github.com/notaryproject/notaryproject/issues/160)
- Showcase project board, feedback, and "epic" views
- Migration off of spreadsheet nearly complete minus yellow items assigned to AWS

### Notes:


## June 27, 2022

### Attendees:
- David Tesar
- Samir Kakkar
- Milind Gokarn
- Rakesh Gariganti
- Shiwei Zhang
- Feynman Zhou
- Jesse Butler
- Michael Brown
- Pritesh
- Roy Will
- Sajay Antony
- Yi Zha

### Agenda Items:

- Samir  - Requesing a scope/time Update on https://cloud-native.slack.com/archives/CQUH8U287/p1656163785567499  ORAS-Go client libraries needed in Notation Client to support the latest ORAS artifact spec 1.0.0-rc.1
    - notation is waiting for #140, #175, and #188 from this milestone. https://github.com/oras-project/oras-go/milestone/5  
    - https://github.com/oras-project/oras-go/issues/140
    - https://github.com/oras-project/oras-go/issues/175
    - https://github.com/oras-project/oras-go/issues/188. ( Fixed)
- Samir - Requesting a daily scrum update on all pending items for RC-1 release. 
- Pritesh - https://github.com/notaryproject/notation-core-go/pull/7
- Registy auth with local credentials [#206](https://github.com/notaryproject/notation/issues/206) (Milind)
- Local key support [#31](https://github.com/notaryproject/roadmap/issues/31) (Milind)
- notary-release-managers group needs to have access to notation-core-go and roadmap repos

### Notes:
- Daily Scrum - we will do daily updates of items chat via project board & chat in slack.  Keep existing two meetings per week.
- We will snap milestone names to what is [listed in the roadmap repo](https://github.com/notaryproject/roadmap/milestones).  They vary across repositories.

## June 23, 2022

### Attendees:
- David Tesar
- Pritesh
- Rakesh Gariganti
- Samir Kakkar 


### Agenda Items:
- Samir - Project task review, and compare with the planned roadmap repo work
### Notes:
- _meeting minutes_

## June 20, 2022

### Attendees:
- David Tesar
- Feynman Zhou
- Roy Will
- Milind Gokarn
- Pritesh
- Rakesh Gariganti
- Samir Kakkar 
- Shiwei Zhang
- Yi Zha

### Agenda Items:
- Yi and Feynman - Confirm the scope and timeline of RC1
- Yi and Feynman - Align the code review process: like who are reviewers and review deadline
- Pritesh - Review [[notaryproject/notaryproject #162] Added requirement for codesigning and timestamping certificate](https://github.com/notaryproject/notaryproject/pull/162) *Roy will review and comment back*
- Milind - PR reviews  . *https://github.com/notaryproject/notation/pull/192*
- Rakesh - Registry Interactions update
### Notes:
- _meeting minutes_



## June 16, 2022


### Attendees:
- Samir Kakkar
- Rakesh Gariganti
- Pritesh Bandi
- Milind Gokarnm
- Jeremy Rickard (Microsoft)

### Agenda Items:
* [`config.json` spec](https://github.com/notaryproject/notation/blob/main/specs/notation-config.md) is outdated and needs updates (low priority) (Milind)
* Scope of Registry auth spec [PR 192](https://github.com/notaryproject/notation/pull/192)
 (Milind)

### Meeting Notes:
1. Jeremy gave an intro and Milind provided and update to the overall Notation project status to attendees
2. David - Lets do another Notation CLI release once the bug fix from Shiwei fore registry authentication (443 port) is addressed. In the meantime lets edit the release notes of the last release to include the workaround
3. Responded and updated the project status items in the task spreadsheet


## June 13, 2022

### Attendees:
- Samir Kakkar
- Rakesh Gariganti
- Pritesh Bandi
- Milind Gokarnm
- Yi  (Microsoft)
- Feynman Zhou
- Shiwei Zhang
- Steve Lasker
- Roy Williams
- David Tesar


### Agenda Items:
-  Samir: Update on everyone's action items
-  Shiwei: PR approvals
-  Milind: Registry Authorization Spec PR; Directory structure spec PR; Directory structure implementation
-  Rakesh : Taks for the above items and change of ownership
-  Steve: CLI commands


### Meeting Notes:
- Milind reviewed PR for directory spec; Need more discussion (Milind will create a new issue) on System Level Vs User Level priority/overrides for directory structure of Plugins, Configuration, Truststore, Trust policies, Signature caches. The solution should be secure by default and usable.
- Milind reviewed Registry Authentication spec : Need to find a way to support http (non https) registries
- Rakesh and Milind covered the item from the spreadsheet. We will continue to coordinate via spredsheet until RC-1 as  single source of truth. We can migrate to project board in parallel and deprecate spredsheet after RC-1. 
- Shiwei suggested how to split notation, Notation-go work vis-a-vis registry authentication.
- Shiwei and Feyman will update the start dates for items assigned to Shiwei. Priortize authentication and directory spec ahead of other work to unblock others.
- Shiwei gave an overview and requested review of PR 198 and 199
- Steve gave an overview and requested review of PR https://github.com/notaryproject/notation/pull/171

## June 9, 2022

### Attendees:
- Steve Lasker (Microsoft)
- Samir Kakkar
- Rakesh Gariganti
- Pritesh Bandi
- Ivan Wallis
- David Tesar


### Agenda Items:
-  Samir : Update on everyone's action items
-  Samir : Add new work items identified (Directory structure implemementation based on spec)
-  David on project managmeen
-  Steve on PKCS #8, #12 update on libraried to encrypt/decrypt keys
-  Ivan has questions on Plugins and Signature format

### Meeting Notes:
- Lets have an offline disccusion on CLI usabilty, secuirty, for the commands for RC-1
- [PKCS #8, #12 ](https://github.com/notaryproject/roadmap/issues/31)Need more dev work to support key encrypt/decrypt. Suggestion to defer password protection for keys stored locally on disk beyond RC-1. Lets think over oher options and make a decision next week https://github.com/notaryproject/roadmap/issues/31
- Added new work item for "Directory structure implementation"
- Reassigned some items between Milind and Shiwei to ublock progress
- We will  gradually migrate to the new centralized "Project beta" on Github that David created, and deprecate use of spreadsheet and roadmap to track work items.  https://github.com/orgs/notaryproject/projects/10/views/4


## June 6, 2022

### Attendees:
- Steve Lasker
- Samir Kakkar
- Milind Gokarnm
- Pritesh Bandi
- David Tesar
- Roy Williams
- Rakesh Gariganti
- Feynman Zhou
- Shiwei Zhang

### Agenda Items:
-  Update on everyone's action items

### Meeting Notes:
- Milind and Shiwei are notation, notation-go, and notation-go-core maintainers and can approve PR. This will move things along faster
- PR Review: [Registry Authentication Spec #192](https://github.com/notaryproject/notation/pull/192)

## June 2, 2022

### Attendees:
- Steve Lasker
- Samir Kakkar
- Milind Gokarnm
- Pritesh Bandi
- Ivan Wallis ( Venafi)
- David Tesar
- Roy Williams

### Agenda Items:
- Streamline code reviews (Milind)

### Meeting Notes:
- Discussion on Plugin model: Changes are merged in https://github.com/notaryproject/notaryproject/blob/main/specs/plugin-extensibility.md
- PKCS#7 is the signature format; PKCS#11 is the API spec for integerating with HSMs/Token devices.
- 

## May 31, 2022

### Attendees:
- Samir Kakkar
- Rakesh Gariganti
- Feynman Zhou
- David Tesar
- Milind Gokarn
- Steve Lasker
- Roy Williams
- Jesse Butler
 

### Agenda Items:
- [Signature spec updates](https://github.com/notaryproject/notaryproject/pull/158)(Milind)
- [Code review process](https://github.com/notaryproject/notation/pull/176)(Milind)
- Code reviewers from Microsoft (Milind)
- [Review spec updates](https://docs.google.com/spreadsheets/d/1em5S59gvfiaqMJ1y4dW1VOtHUvPCCC3PoBiqyiTKk24/edit#gid=0) - Rakesh
- CICD and Release process (Rakesh)

### Meeting Notes:
- [v0.9.0-alpha.1](https://github.com/notaryproject/notation/releases/tag/v0.9.0-alpha.1) released
- Feyman will work with Shwewei to get dates on past due items
- Shiwei and Milind will look at each other's PR and approve asap
- For CLI commands, lets focus on -Sign, Verify, Inspect and plugin commands. Rest can wait.
- David  did a demdemo what is currently implemented for CI/CD/Testing, by taking the example of this upcoming alpha release
- Feyman will lay a plan for where we want to end up for end to end test and release process

## May 26, 2022

### Attendees:
- Samir Kakkar

### Agenda Items:
- Need a "Notation" release with the latest ORAS libraries to address (iamsamirzon)
    - https://github.com/notaryproject/notation/issues/119
    - There are  lot of other updates as well.
- Need additional member for https://github.com/orgs/notaryproject/teams/notary-project-admins/members  (iamsamirzon)
    - Once done, create a new version of "MilestonesAcrossAllRepos" and directly track all work going for first RC-1 release there.
- Go through RC-1 roadmap items and cleanup, set status, assign owners.   (iamsamirzon) https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3ARC-1
- Go through open PRs in thee specfic repos and ensure alignment with roadmap (iamsamirzon)
- Work to merge spreadsheet backlog into specfic repos and assign owner (iamsamirzon)

### Notes:
- 

## May 19, 2022

### Attendees:
- Feynman Zhou
- David Tesar
- Milind Gokarn
- Samir Kakkar
- Pritesh

### Agenda Items:
- Go through roadmap items and cleanup, set status, assign owners.  Focus on Alpha-3 items first: https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3Aalpha-3
- Work to merge spreadsheet backlog into public items

### Notes:
- We may or may not have an Alpha-3 release, but definitely will be making alpha releases in interim to RC1.  Alpha-3 items are needed for RC-1. 
- Discussed whether or not we should just merge Alpha-3 into RC milestones or not.  Will follow up on this next week.

## May 16, 2022

### Attendees:
- Feynman Zhou
- David Tesar
- Roy Williams
- Milind Gokarn
- Pritesh Bandi
- Rakesh Gariganti
- Sajay Antony

### Agenda Items:
- PRs for review (Milind)
  - [Notation-go plugin code](https://github.com/notaryproject/notation-go/pull/42)
  - [Notation Directory Structure Spec](https://github.com/notaryproject/notation/pull/175)
  - [Signature spec updates](https://github.com/notaryproject/notaryproject/pull/158)
- Logging from Notation CLI and lib (Milind)

### Notes:


## May 12, 2022

### Attendees:
- Iilya Dmitrichenko
- Maik Riechert
- Samir Kakkar
- Milind Gokarn
- Pritesh Bandi
- Rakesh Gariganti
- Steve Lasker
- Roy Williams
- Shiwei Zhang

### Agenda Items:
- [Discovery and configuring trust policy](https://github.com/notaryproject/notation/issues/172) (Steve)
- PRs for review
  - [Notation Directory Structure Spec](https://github.com/notaryproject/notation/pull/175)

### Notes:
- Introduction of new and old members. 
- Review of the above two PRs
    - [Notation Directory Structure Spec](https://github.com/notaryproject/notation/pull/175)  (Required for RC-1)
    - [Discovery and configuring trust policy](https://github.com/notaryproject/notation/issues/172) (Continue discussion on PR. Not part of RC-1)


## May 9, 2022

### Attendees:
- Steve Lasker
- Roy Williams
- Milind Gokarn
- Samir Kakkar
- Shiwei Zhang
- Rakesh Gariganti
- Sajay Antony

### Agenda Items:
- PRs ready to merge
    - [Load and Validate Trust Policy documents](https://github.com/notaryproject/notation-go/pull/39)
- PRs for review
    - [Implement generate signature plugin workflow](https://github.com/notaryproject/notation-go/pull/42)
    - [Support managing plugin keys](https://github.com/notaryproject/notation/pull/168)
    - [Address review comments on #148 for JWS](https://github.com/notaryproject/notaryproject/pull/156)
    - [ Draft PR for CLI command feedback](https://github.com/notaryproject/notation/pull/171)
- Any changes to project plan dates (Milind, Shiwei)
- Spec updates

### Notes:
- _meeting minutes_


## May 5, 2022

### Attendees:
- Steve Lasker
- Roy Williams
- Milind Gokarn
- Samir Kakkar
- Pritesh Bandi
- _add yourself_

### Agenda Items:
- New meeting schedule (Milind)
- Where should we store signature envelope? (Pritesh)
    1. As blob only (which is referred by manifest)
    1. As data field in manifest + blob
    1. As annotations only
*Conclusion:* We will go with approach 1 where the signature will be stored as separate blob only.
- [Spec : Notation directory structure](https://github.com/notaryproject/notation/issues/167) (Milind)
- [Project plan updates](https://docs.google.com/spreadsheets/d/1em5S59gvfiaqMJ1y4dW1VOtHUvPCCC3PoBiqyiTKk24/edit#gid=0) (Milind)
- [Notation registry auth](https://github.com/notaryproject/notation/discussions/170)(Milind)
- Code review process (Milind)
    - https://github.com/notaryproject/notation-go/pull/37
- Project Tracking in Roadmap repo(Samir)
- [Draft PR for CLI command feedback #171
](https://github.com/notaryproject/notation/pull/171)

### Notes:
- Move Thursday meeting From 5-6pm to 9-10am
- Adding a Monday 5-6pm pacific time to account for EU and US
- **Signature Envelope Storage** - To minimize churn for RC1, we'll use the existing persistance as a blob in the ORAS Artifact reference object.
- **Config** - keep config.json for shared items, with two additional configs to manage isolation of configurations, avoiding having to merge into a single config.json
- **Directory Location**: discussion for where config can be stored, securely, avoiding code running as part of a build from having access to the config of keys or certs. No decision, but needs more thought.
- _meeting minutes_


## April 28, 2022

### Attendees:
- Steve Lasker
- David Tesar
- Milind Gokarn
- Samir Kakkar
- Roy Williams
- Sajay Antony
- Rakesh Gariganti
- Shiwei Zhang
- _add yourself_

### Agenda Items:
- RC1 scope (Samir)
    - Closed the two TBD items from last week. JWS format for RC-1
    - Security review for Notation RC-1 cliet decision to be made close to it being ready
    - Will explore a process to close roadmap items in a async manner based on PRp;ls being closed 
- PR code review process (Milind)
- [Simplify trust store and trust policy](https://github.com/notaryproject/notaryproject/pull/149) (Milind)

### Notes:
- _meeting minutes_

## April 21, 2022

### Attendees:
- Steve Lasker (Microsoft)
- Samir Kakkar 
- Milind Gokarn 
- Rakesh Gariganti 
- David Tesar (Microsoft)
- Shiwei Zhang (Microsoft)

### Agenda Items:
- [Rename notation-go-lib to notation-go](https://github.com/notaryproject/notation-go/issues/33)
- [Simplify trust store and trust policy](https://github.com/notaryproject/notaryproject/pull/149)

### Notes:
- [Rename notation-go-lib to notation-go](https://github.com/notaryproject/notation-go/issues/33)
    - Repository renaming done
    - [Rename go module #34](https://github.com/notaryproject/notation-go/pull/34)
- Security reviews kickoff initiaited for go-cose library, and its integration with Notation cleint_
- TBD : Schedule Security review for Notation RC-1 release, that will use existing JWS encoding format
- TBD : Dual support for both JWS and COSE signature encoding format for subsequent releases

## April 14, 2022

### Attendees:
- Steve Lasker (Microsoft)
- Milind Gokarn
- Samir Kakkar
- Rakesh Gariganti
- Sajay Antony
- Shiwei Zhang

### Agenda Items:
- Signature spec [PR](https://github.com/notaryproject/notaryproject/pull/147)
- Notation [design goals and versioning](https://hackmd.io/DJi7Ig94SVSaftQxWByVEQ)

### Notes:
- _meeting minutes_

## April 7, 2022

### Attendees:
- Steve Lasker (Microsoft)
- Milind Gokarn
- Samir Khan
- Sajay Antony
- Shiwei Zhang
- Pritesh
- _add yourself_

### Agenda Items:
- Review updates to [signature spec and policy ](https://hackmd.io/h9L1CBeVTbmUUGID46UAYA)

### Notes:
- _meeting minutes_


## March 31, 2022

### Attendees:
- Marina Moore (NYU)
- Samir Kakkar (AWS)
- Steve Lasker (Microsoft)

### Agenda Items:
- New time, Wednesdays 5-6pm Pacific Time, 8-9pm Eastern, 8-9am Shanghai (Steve)
    - Based on updated doodle poll results, proposing 5-6pm Thursday 9-10am Shanghai
- Trust Stores and changes to config (Milind)
- _add your topics_

### Notes:
- _meeting minutes_

## March 24, 2022

### Attendees:

- Steve Lasker (Microsoft)
- Tianon
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- Brandon Mitchell
- David Tesar (Microsoft)

### Agenda Items:
- Should the signature format support multiple signing forms now? (Milind)
    - (Steve) We're hoping to land the [COSE format for the initial release](https://github.com/notaryproject/notaryproject/pull/139), but we've said notary will support multiple signature formats over time, for instance different governments (China has been the common example, but also support for newer over time). If we add multiples now, we validate the spec supports multiples. If we land COSE for v1, we can pull JWT out, knowing the spec supports multiple formats.
    - [go-cose library design](https://github.com/veraison/go-cose/pull/14) - but this is merged into the [remote-signing branch](https://github.com/veraison/go-cose/blob/remote-signing/DESIGN.md)
- Doodle poll (Steve)
    - promise to get it out today
- Trust Policy (Steve)
    - public key discovery
    - policy for configuring what a user wants to trust
- _add your topics_

### Notes:
- _meeting minutes_

## March 17, 2022

### Attendees:
- Steve Lasker
- Samir Kakkar (Chair)
- Marina Moore (NYU)
- Lukas Pühringer (NYU)
- Tianon
- _add yourself_

### Agenda Items:
- New time for notary call to account for Shanghai timezones
    -  Steve to create a doodle poll
- Alpha 3 milestone (Samir)
- _add your topics_

### Notes:
- _meeting minutes_


## March 10, 2022

Cancelled, folks are working on PRs and execution

## March 3, 2022

### Attendees:
- Steve Lasker (Microsoft)
- Brandon Mitchell
- Tianon
- Pritesh
- Samir
- _add yourself_

### Agenda Items:
- [Alpha 2](https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3Aalpha-2) complete
- [Alpha 3 goals](https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3Aalpha-3) (Samir)
- [RC1 goals](https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3Arc-1)
- _add your topics_

### Notes:
- _meeting minutes_

## February 24, 2022

### Attendees:
- Samir Kakkar ( AWS)
- Pritesh Bandi (AWS)
- Brandon Mitchell
- Marina Moore (NYU)

### Agenda Items:

- Getting Alpha-2 released (Samir)
- _add your topics_

### Notes:
- _meeting minutes

## February 17, 2022

### Attendees:
- Samir Kakkar ( AWS)
- Pritesh Bandi (AWS)
- Brandon Mitchell

### Agenda Items:

- PR Reviews are making progress
  - https://github.com/notaryproject/notaryproject/pulls
- _add your topics_

### Notes:
- _meeting minutes_

## Feb 10, 2022

### Attendees:
Mark Grand (JFrog)
Samir Kakkar ( AWS)
- _add yourself_

### Agenda Items:
- _add your topics_

### Notes:
- We had a short meeting. No new PRs to review this week
- Recommend everyone to look at the roadmap repo and the project plan there. We are getting close to alpha-2

## Feb 3, 2022

### Attendees:
- Steve Lasker (Microsoft)
- Brandon Mitchell
- Tianon
- Samir Kakkar (AWS)
- Pritish Bandi (AWS)
- Milind Gokarn (AWS)
- _add yourself_

### Agenda Items:
- [Add support for signature filtering.](https://github.com/notaryproject/notaryproject/discussions/127) (Pritesh)
- [Add support for trust anchor.](https://github.com/notaryproject/notaryproject/discussions/129) (Pritesh)
- Fall back options [ORAS](https://github.com/oras-project/artifacts-spec/pull/84) and [Notary Project](https://github.com/notaryproject/notaryproject/issues/112#issuecomment-984741895) (Brandon)

### Notes:
- Subject example:
  - ![](https://i.imgur.com/CGB0bfc.png)
  - ![](https://i.imgur.com/mh21KlY.png)


- _meeting minutes_


## January 27, 2022

### Attendees:
- Samir Kakkar (AWS)
- Pritish Bandi (AWS)
- Milind Gokarn (AWS)
- Mark Grand (JFrog)
- Steve Lasker (Microsoft)
- Marina Moore (NYU)
- Tianon
- Brandon Mitchell
- _add yourself_

### Agenda Items:
- Open PRs for review
    - [Notation plugin for signing](https://github.com/notaryproject/notaryproject/pull/124) (Milind)
    - [Adding scope to trust policy.](https://github.com/notaryproject/notaryproject/pull/119) (Pritesh)
    - [Registry Interop](https://github.com/oras-project/artifacts-spec/pull/84) (Steve)

### Notes:
- [Azure Key Vault Plug-in](https://github.com/Azure/notation-azure-kv/blob/main/docs/nv2-sign-verify-aks.md)
- Closing on the [COSE format](https://github.com/notaryproject/notaryproject/issues/117) becomes important to closing on the plug-in spec
- _meeting minutes_

## January 20, 2022

### Attendees:
- Brandon Mitchell
- Tianon
- Marina Moore
- Samir Kakkar
- Steve Lasker (Microsoft) [Chair]
- Pritesh Bandi

### Agenda Items:
- Open PRs for review
  - [Adding scope to trust policy.](https://github.com/notaryproject/notaryproject/pull/119) (Pritesh)
  - [Added support for signature filtering.](https://github.com/priteshbandi/notaryproject/pull/1) (Pritesh)
      - PR is in my fork as its stacked on existing open PRs

### Notes:
- _meeting minutes_
- Discussion on explict distinction for scpoping for repositories Vs namespaces
    - Supported cases:
        1. `wabbit-networks.io/software`   <-- repo match
        1. `wabbit-networks.io/software/*`  <-- match immediate namespace  
        `wabbit-networks.io/software/prod-good`
        1. `wabbit-networks.io/software/*/*`  <-- `wabbit-networks.io/software/prod/asd` <-- will add if requried in future 
        1. `wabbit-networks.io/software/**`  <-- match all nested namespaces inside software namespace
    - Invalid cases:
        1. `wabbit-networks.io/software*` <-- parse error
        1. `wabbit-networks.io/software/prod-*` <-- parse error
        1. ` wabbit-networks.io/software/prod-bad/ `<-- parse error
        1. ` wabbit-networks.io/soft*` <-- parse error


## January 13, 2022

[Recording](https://youtu.be/9vTex2_4KfQ)

### Attendees:
- Mark Grand
- Brandon Mitchell
- Marina Moore [Chair]
- Samir Kakkar
- Tianon
- Steve Lasker
- Pritesh Bandi

### Agenda Items:

- Open PRs for review
  - [Adding scope to trust policy.](https://github.com/notaryproject/notaryproject/pull/119) (Pritesh)
  - [Added signing and verification workflows](https://github.com/notaryproject/notaryproject/pull/122) (Pritesh)

### Notes:
- Trust policy:
    - Reviewing discussion points from last meeting for scoping
    - Considered but not interested in allowing multiple policies to match, only planning to match a single policy, requiring ordering.
    - Other possible scoping suggestions looked at, but not planned for current development efforts
    - Scope isn't being treated as a security control so they aren't concerned about prefix matching matching the wrong thing. The user controls what images are being matched external to this.
    - In general the current design in extendable for future use.
	    1. For now moving with the Longest prefix match and deferring wild card for a later time.
	    2. Discussed we can make different trust stores. If the same policy scope has two different artifact type with different signing keys, we can even add an artifact type in the future.
	    3. If we need to put rich comments in the JSON files, we could add a "description" field in the future.

- Discussion on Revocation ()
	1. Refer the paper from Steve on this topic https://stevelasker.blog/2022/01/11/roles-and-responsibilities-of-signing-sboms-and-security-scanners/ 
	2. When should a key be revoked ( In case of compromise ? Any other reasons ?)
		a. Ideally a key should not be revoked because a vulnerability is found in the code it signed
	3. When could a signature be revoked on an artifact( In case of a finding a vulnerability ?) https://github.com/notaryproject/notaryproject/blob/main/scenarios.md#scenario-11-revoking-a-signature
	    a. Is there a standard for this? Should we add this in scope for NotaryV2 ?
    4. Some users may not want revocation to automatically  hamper their production envoirnement    
    


## January 5, 2022

[Recording](https://youtu.be/9ntTFcE6tkk)

### Attendees:

- Mark Grand
- Justin Cormack [Chair]
- Brandon Mitchell
- Steve Lasker
- Mahendra Reddy
- Tianon
- _add yourself_

### Agenda Items:

- Review the [doodle poll](https://doodle.com/poll/x39vzgpp4ukibr3q?utm_source=poll&utm_medium=link) for the 2022 timeslot. Please get your votes in. (Steve)
- Review [Trust Policy Scoping Scenarios](https://hackmd.io/@pritesh/TP-scoping-scenarios) (Pritesh)
- Review [Trust Anchor in TrustPolicy](https://hackmd.io/@pritesh/trust-anchor-in-TS-TP) (Pritesh)
- Review [Signing and verification workflows, Including detailed verification workflow](https://hackmd.io/@pritesh/signing-verfication-workflow) (Pritesh)
- Review [signing inline](https://github.com/justincormack/sign-index) (Justin)
- _add your topics_

### Notes:
- [Doodle poll concensus](https://doodle.com/poll/x39vzgpp4ukibr3q?utm_source=poll&utm_medium=link#table): Thursday 9-10am pacific time
- Trust Policy: can we skip the priority determination and instead accept any matching policy regardless of the order (Brandon)
    - [Pritesh - post meeting] If we go with the longest prefix match order doesn't matter as each and every policy will be evaluated for applicability with a longest-prefix match.
- Wildcards must be scoped to a dns segment. To avoid SQL injection style attacks, adding a . in the replacement would be considered invalid. 
    - [Pritesh - post meeting] That's interesting, we should do thiswith wildcard but we still have a policy ordering issue.
- There's a desire to limit scope to other signature metadata rather than host/repo. E.g. originator may include metadata on their name to make portable images+signatures. Also some users may want to sign SBOMs or attestation data with a different key than the image, and only trust one key to a certain type of signature. (Brandon)
    - [Pritesh - post meeting] IMO initially, we should keep default notary validations simple and generic. If a user wants complex validation they can implement them using extensions. Or if the use-case becomes popular we can add support later.
- For regionalized entries, for now, should we defer this, where the user enters multiple trust policies. One for each region, which all point to the same trust store.
- Consider two levels of wildcards like git, `*` for a single dns/path element, `**` for multiple levels (Brandon)
- _meeting minutes_


# Archived Notes

Older meeting notes have been archived to: https://github.com/notaryproject/meeting-notes

* 2021 meeting notes https://hackmd.io/-5DLI3xiRmmgiC1ugo7fHw?view

# Meeting Notes Template
(template for copying)

## Meeting Date

### Attendees:
- _add yourself_

### Agenda Items:
- _add your topics_

### Notes:
- _meeting minutes_
