# Notary v2 Meeting Notes 2021


###### tags: `notary`

## December 29, 2021

Meeting skipped for the holidays

## December 22, 2021

Meeting skipped for the holidays

## December 15, 2021

[Recording](https://youtu.be/DTL7GsJBR5k)

### Attendees:
- Brandon Mitchell
- Steve Lasker (Microsoft) [Chair]
- Shiwei Zhang (Microsoft)
- Tianon
- Samir Kakkar (AWS)
- Pritish Bandi (AWS)
- _add yourself_

### Agenda Items:

- [Extensibility framework](https://github.com/notaryproject/notation/pull/142) (Steve)
- Alpha 2 - scope to extensibility, push remaining to alpha 3 (Steve)
- [Subject may be redundant #111 - any other changes?](https://github.com/notaryproject/notaryproject/pull/111) (Pritesh)
- [[PR] Adding scope to trust policy](https://github.com/notaryproject/notaryproject/pull/119) (Pritesh)
- _add your topics_

### Notes:
- _meeting minutes_
- Doodle poll for new meeting time will go out
- Incorporate PR feedback on #142, merge and incoproate feedback into the extensibility spec.
- Cut Alpha 2 to cover extensibility, and move remaining items to Alpha 3, starting on policy
- naming of subject/notary: considered multiple names. Concerns around [jwt "sub" property](https://datatracker.ietf.org/doc/html/rfc7519.html#section-4.1.2) 
    - subjectDescriptor
    - subject
    - notary
    - descriptor
    - content
    - signed
    - naming-is-hard
    - namingIsHard
    - naming_is_hard-property
- Landing on `subject` as it aligns with the artifact manifest property that we debated quite a bit around. And, it maps to the `sub` property in expanded form. 
   - Next steps: Brandon to update the PR
- Discussing if wildcarding needed for scoping in trust policy
    - [Kyverno uses wildcards](https://kyverno.io/policies/best-practices/restrict_image_registries/restrict_image_registries/)
- Policies - writeup some examples of dev, staging, prod registries, and what the policies would look like
- Next two meetings skipped for the holidays

## December 8, 2021

[Recording](https://youtu.be/JX0_wvwYnbs)

### Attendees:
- Brandon Mitchell
- Marina Moore [Chair]
- Steve Lasker (Microsoft)
- Tianon
- Faisal Razzak
- Shiwei Zhang (Microsoft)
- Nate W. (CNCF)
- Jason Hall (Red Hat)
- Samir Kakkar (AWS)
- Pritish Bandi (AWS)
- Milind Gokarn (AWS)
- _add yourself_

### Agenda Items:
- [Signing/Verification Extensibility](https://github.com/notaryproject/notaryproject/discussions/114) (Milind)
- [Fallback registry support](https://hackmd.io/FIa5U4xcSV6ccftwCPAZjA) (Jason)
- (quickly) [YouTube recordings are a few months out of date](https://www.youtube.com/playlist?list=PL1ykZdgmLkb7SlXax-hJVUgvNHmq4Cyz9) (Jason)
    - [Steve] I thought I caught up. I'll check today.
- Meeting times for January - would like to shift later in the day (Steve)

### Notes:
- Reviewed the Extensibility doc from Milind and went through the open items. 
    - Discussion on versioning of notation cli and plugins interface
        - The CLI and GoLib versioning will continue as is, and will be independently released
    - Why should we keep two separate signature generation functions ?
        - There is a downside of “generate-signature” is that it wont FIPS compliant(we need seperate binary to make it FIPS).
        - Agreed to proceed with just the “generate-envelope” for now, and revisit later if “generate-signature” is needed
    - Steve brought up, a use case for signing things which are not even in a registry by using Notation. Example IoT Firmware. 
    - Discussion on the need for signatureEnvelopeType, Chaining plugins
    - Brandon requested we define Verification aspects quickly, specifically in relation to certificate chaining
        - We covered the merged PR from Pritesh Bandi, on how verification will work.
- Faisal brought up what are the signing providers we are targeting? Is there a list?
    - PKCS#11, PIV - Will these be built into Notation directly? This is TBD
    - At a high level, nothing in Notation should be cloud or vendor specific. 
    - NotaryV1 supported Hardware Tokens, but perhaps never the full PKCS#11
- Jason initiated discussion on Brandon’s hackmd doc on supporting signing without the reference API 
    - Steve requested we start with requirements and definitions, and then look at solutions
        - Can we version the existing manifest, and create a new one?
        - Is cost of polluting tag justified , given that no other registry side changes are required.
    - The requirements in Brandon’s doc a good place to start solutioning from there, lets give  a weight and definition to those requirements, and add any missing ones. Example - Immutable tags 


## December 1, 2021

[Recording](https://youtu.be/FatlwFooB28)

### Attendees:
- Brandon Mitchell
- Steve Lasker (Microsoft) [Chair]
- Marina Moore (NYU)
- Mark Grand (JFrog)
- Shiwei Zhang (Microsoft)
- Tianon
- Justin Cormack (Docker)
- Samir Kakkar (AWS) - Note taker today
- Mahendra Reddy
- Anish Ramasekar (Microsoft)

### Agenda Items:
- [Options for backwards compatibility](https://github.com/notaryproject/notaryproject/issues/112) (Brandon)
- [Signing/Verification Extensibility](https://github.com/notaryproject/roadmap/issues/26) (Samir)
- Demo of remote signing with Azure Key Vault (Anish)
- _add your topics_

### Notes:
- Backwards compatibility:
    - Need to create a list of requirements in addition to possible solutions
    - Brandon and Justin will sync up on this
- Signing/Verification Extensibility:
    - Reviewed this document : https://hackmd.io/jhYbA4aNRFW7nmp7gPTIBA?view
    - Should signing plugin also be able to verify signatures?
    - There's a need for verification only plugins
    - Most signing solutions will want to use the second method (full content), only a few cloud solutions want it pre-hashed
    - May be able to remove generate-signature since it's a subset of generate-envelope, any plugin that needs a hash can compute the hash in the plugin and send that to the external system
- Demo of remote signing:
    - showing end to end with register plugin, sign, and verify
    - Also need to think about how plugin based signing will integrate with key distribution solutions layer (need to extract public keys via plugin)
    - Desirable to keep plugin implementation and registraction mechanism simple.
- _meeting minutes_

## November 24, 2021

Canceled due to Thanksgiving.

## November 17, 2021

[Recording](https://youtu.be/rxpL9Cl4CoE)

### Attendees:
- Mark Grand
- Brandon Mitchell
- Shiwei Zhang (Microsoft)
- Tianon
- Marina Moore  [Chair]
- Nate Waddington (CNCF)
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- Mahendra Reddy
- Steve Lasker (Microsoft)
- _add yourself_

### Agenda Items:
- Curate the [features marked for alpha-2 release](https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3Aalpha-2) (Samir Kakkar)
  

### Notes:
- _meeting minutes_

## November 10, 2021

[Recording](https://youtu.be/_X8fm4FN7Ts)

### Attendees:
- Marina Moore (NYU)
- Brandon Mitchell
- Steve Lasker (Microsoft) (Chair)
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- Shiwei Zhang (Microsoft)
- Faisal Razzak (Venafi)
- Mark Grand (JFrog)
- Christoph Hamsen (Connaisseur)
- Tianon
- _add yourself_

### Agenda Items:
- [Notation extensibility for signing](https://hackmd.io/jhYbA4aNRFW7nmp7gPTIBA?view) (Milind)
- Answer questions about Pyrsia (Mark) 

### Notes:
- Signing payload, can we minimize the registry concepts, such as knowledge of a manifest, so the offline signing service can sign content that isn't specific to registries. For things like annotations, are the name/value pairs tied to registry concepts? There isn't a hard requirement for signing content that isn't stored in a registry, just good hygene to minimize the dependencies.
- How are signing and verifications plug-ins identified to avoid bad-verifier being installed to verify good-co signatures. 
- _meeting minutes_

## November 3, 2021

[Recording](https://youtu.be/9H-h5O-MKuU)

### Attendees:
- Brandon Mitchell
- Tianon
- Hector Fernandez (VMware)
- Shiwei Zhang (Microsoft)
- _add yourself_

### Agenda Items:
- [tuf-notary project board](https://github.com/notaryproject/tuf/projects/1)
- [Alpha 2 goals](https://hackmd.io/@stevelasker/nv2-alpha2-goals) and [the roadmap/board](https://github.com/notaryproject/roadmap/projects/1?card_filter_query=milestone%3Aalpha-2) (steve/samir)


### Notes:
- _meeting minutes_


## October 27, 2021

[Recording](https://youtu.be/WTQdGB3VVEY)

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Marina Moore (NYU)
- Samir Kakkar (AWS)
- Sajay Antony (Microsoft)
- Jason Hall (Red Hat)
- Tianon
- _add yourself_

### Agenda Items:
- Options for backwards compatibility with existing registries (Brandon)
    - https://github.com/notaryproject/notaryproject/issues/112
- Permissions/merging for tuf repository (Marina)
- _add your topics_

### Notes:
- Fix permissions issues on TUF repository - Steve to follow up
- Backwards compat (fallback)
    - cosign uses .sig tag suffix, supports multiple signatures: https://gist.github.com/imjasonh/dc60025ee7ce31143880230e9fc3d593
    - Discussion around what we're trying to solve (requirements) so we can decide which we need in the fallback model, vs. the Reference Type support with the artifacts spec, including the referrers api
    - Steve to take the action item for writing the requirements down with a table for discussion
- TUF discussion for storing in a registry (https://github.com/notaryproject/tuf/pull/10/) and https://github.com/notaryproject/tuf/pull/11/
    - https://github.com/SteveLasker/Presentations/blob/master/KubeCon/kubeconus-2021-notaryv2-promoting-artifacts.md - promotion demo script
    - New TUF meeting is 1pm eastern (10am pacific) on Fridays [TUF-notary meeting notes](https://hackmd.io/wii3-L8ZQZ-U3ET0XNY8Gg)
- Nate following up with Amye on how to get links to specific CNCF calendar items.
- _meeting minutes_

## October 20, 2021

[Recording](https://youtu.be/592BtBAwLWU)

### Attendees:
- Tianon
- Christoph Hamsen ([Connaisseur](https://github.com/sse-secure-systems/connaisseur))
- Pritesh Bandi (AWS)
- Brandon Mitchell
- Shiwei Zhang (Microsoft)
- Hector Fernandez (VMware)
- Sajay Antony (Microsoft)
- Steve Lasker (Microsoft)
- Samir Kakkar (AWS)
- _add yourself_

### Agenda Items:
- Readiness Review for the first release
    - https://github.com/notaryproject/roadmap/blob/main/RELEASENOTES/v2.0.0.alpha-1.MD
- Is the "subject" field needed (Brandon)
    - https://github.com/notaryproject/notaryproject/pull/111

### Notes:
- Discussion on what versions we should use. Should we start with 2.0 to avoid user confusion around Notary v1? We're also wanting to keep alpha-1 labes on the versions to indicate it's not ready for production, and the alpha-[n] label indicates the compatibility across notation, notation-go-lib, notaryproject specs, and the dependencies on oras for registry push|discover|pull
- Ask to include what's in and not in a particular release, based on the requirements. This would help consumers understand what is/isn't in a partiuclar release, and what's coming in the future. For example, revocation, policy. 
- _meeting minutes_

## October 13, 2021

[Recording](https://youtu.be/r7hQzEhiuTY)

### Attendees:
- Tianon
- Shiwei Zhang (Microsoft)
- Brandon Mitchell
- Steve Lasker (Microsoft)
- Nate W. (CNCF)
- Serge Hallyn (Cisco)
- Christoph Hamsen ([Connaisseur](https://github.com/sse-secure-systems/connaisseur))
- Pritesh Bandi (AWS)
- Samir Kakkar (AWS)
- _add yourself_

### Agenda Items:
- PR [Signature Specification](https://github.com/notaryproject/notaryproject/pull/102/) (Pritesh)
- Notary V2 Roadmap and Release process (Samir)
    - https://hackmd.io/Q2V1stKVRXaSynn_8kSMNg?view
    - https://github.com/iamsamirzon/roadmap

### Notes:
- _meeting minutes_


## September 29, 2021

[Recording](https://youtu.be/iV_DVY58mX8)

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Nate W. (CNCF)
- Samir Kakkar (AWS)
- Marina Moore (NYU)
- Milind Gokarn (AWS)
- Brandon Mitchell
- Pritesh Bandi (AWS)
- Hector Fernandez (VMware)
- Serge Hallyn (Cisco)
- _add yourself_

### Agenda Items:
- Update on alpha release and roadmap planning (Samir)
- Quick demo on the Notation CLI and Go library PRs (Shiwei)
    - https://github.com/notaryproject/notation/pull/94
    - https://github.com/notaryproject/notation-go-lib/pull/11

### Notes:
- Alpha-1 release should include merged PRs into the notaryproject specs that another implementation could create their own alpha-1 release without looking at notation code and libraries. -Brandon
- Alpha-2 might be a good place to target integration with the tuf-notary work. -Marina
- _meeting minutes_


## September 22, 2021

[Recording](https://youtu.be/pyIejid8O78)

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Tianon
- Justin Cormack (Docker)
- Nate Waddington (CNCF)
- Brandon Mitchell
- Miloslav Trmač (Red Hat)
- Sajay Antony
- Hector Fernandez (VMware)
- Serge Hallyn (Cisco)
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- _add yourself_

### Agenda Items:
- [Project Board](https://hackmd.io/NCqqkHq2Tk-2yxLv1oOslw) (Samir)
- [Automated Builds from main -looking for help #71](https://github.com/notaryproject/notation/issues/71) (Steve/Sajay)
- [Close on location of doc content](https://github.com/notaryproject/notaryproject/issues/101) (Nate)
- Signature format update? (?)
- _add your topics_

### Notes:
- Docs
    - Discussion on Option 1 and 2. The main issue around 2 has been permissions. We can solve that through github permissions
    - Leaning into the SME principal, the doc expert has shown how docs in a common location (option 2) has worked with other projects ([etcd](https://etcd.io/docs/v3.5/)), we should lean into it here. 
    - There are additional localization and versioning reasons to have in a single repo.
    - Action item is to add to the contributing guidance for how docs are managed
    - Additional action item: to bring the [Documentation project board](https://github.com/notaryproject/notaryproject.dev/projects/1) to the notaryproject org top level
- _meeting minutes_

## September 15, 2021

[Recording](https://youtu.be/8ZPpLomgLrw)

Chair: Marina

### Attendees:
- Steve Lasker (Microsoft)
- Marina Moore (NYU)
- Shiwei Zhang (Microsoft)
- Nate W. (CNCF)
- Tianon
- Christoph Hamsen (Connaisseur)
- Hector Fernandez (VMware)
- _add yourself_

### Agenda Items:
- [Artifacts Spec](https://github.com/oras-project/artifacts-spec/) Draft Release Update (Steve)
- [Notation CLI](https://github.com/notaryproject/notation/pull/83) update (Sajay)
- [Project Board](https://hackmd.io/ogZ99S7uTE-UDJC6s8epvQ?view) (Samir)
- _add your topics_

### Notes:
- Notation CLI
    - a few remaining issues, need to add tests
    - Will add github issue for remaining work
- Project board
    - will be moved to GitHub (WIP)
    - contents in hackmd
- _meeting minutes_

## September 13, 2021

[Recording](https://youtu.be/yBur3KphJNk)

### Attendees:
- Samir Kakkar (AWS)
- _add yourself_

### Agenda Items:
- Project Board Prep for coming up with release milestones for Notaryproject/Notation (Samir)
- _add your topics_

### Notes:
- _meeting minutes_

## September 8, 2021

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Marina Moore (NYU)
- Brandon Mitchell
- Nate Waddington (CNCF)
- Tianon
- Pritesh Bandi (AWS)
- Samir kakkar (AWS)

### Agenda Items:
- [Merging notation updates for continued iteration #83](https://github.com/notaryproject/notation/pull/83) (Steve)
    - It depends on [notaryproject/notation-go-lib#5](https://github.com/notaryproject/notation-go-lib/pull/5) (Shiwei)
- [Finalizing the signature format](https://github.com/notaryproject/notaryproject/pull/93) (Milind/Steve)
- [Define releases](https://github.com/orgs/notaryproject/projects/1) (Steve)
- [Trust Policy and Trust Store Configuration - Open Questions](https://github.com/notaryproject/notaryproject/discussions/98) (Pritesh)
    - [Alternate Proposal for Trust Store/Policy](https://github.com/notaryproject/notaryproject/discussions/100) (Brandon)
- [Notary Project website](https://notaryproject.dev) (Nate)
  - [Information Architecture (IA) proposal, issue #23](https://github.com/notaryproject/notaryproject.dev/issues/23)
    - Please find an editable version of the IA Proposal here: [notaryproject.dev IA Proposal](https://hackmd.io/@nate-double-u/H1JkSDYWF)
  - [Landing page updates, issue #16](https://github.com/notaryproject/notaryproject.dev/issues/16)
  - [Migrate Notary documentation content, issue #21](https://github.com/notaryproject/notaryproject.dev/issues/21) -- discussion, moving docs from the notaryproject/notary project to the website (when, how)
- _add your topics_

### Notes:
- Documentation considering whether docs should be one repo or distributed among sub-projects.
    - One repo avois fragile integration between repos
    - Docs per project keeps PRs changing functionality linked to doc changes in the same PR
- Merging notation 
    - Agreement to merge in notation as the baseline into main, documenting its status
    - Open issues on the merged cli and library to address gaps and changes
    - Enables the project to reflect things that are known, and functional, while we work on the next round of spec & design elements

## September 1, 2021

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Justin Cormack (Docker)
- Marina Moore (NYU)
- Brandon Mitchell
- Nate Waddington (CNCF)
- Christoph Hamsen (Secure Systems / [Connaisseur](https://github.com/sse-secure-systems/connaisseur))
- Tianon
- Pritesh Bandi (AWS)
- Samir Kakkar (AWS)

### Agenda Items:
- [Notation PRs to release an updated notation cli (updated from prototype-2](https://github.com/notaryproject/notation/pulls) (Steve)
- [Trust Policy and Trust Store Configuration - Open Questions](https://github.com/notaryproject/notaryproject/discussions/98) (Pritesh)
- [Notary Project website](https://notaryproject.dev) (Nate)
  - [Information Architecture (IA) proposal, issue #23](https://github.com/notaryproject/notaryproject.dev/issues/23)
    - Please find an editable version of the IA Proposal here: [notaryproject.dev IA Proposal](https://hackmd.io/@nate-double-u/H1JkSDYWF)
  - [Landing page updates, issue #16](https://github.com/notaryproject/notaryproject.dev/issues/16)
  - [Migrate Notary documentation content, issue #21](https://github.com/notaryproject/notaryproject.dev/issues/21) -- discussion, moving docs from the notaryproject/notary project to the website (when, how)

### Notes:
- Scope paths:
    - `registry.acme-rockets.io/namespace/sub-namespace/repo:tag`
        a scope must be: `registry.acme-rockets.io/namespace/`
        This would be invalid, as it's a partial namespace: `registry.acme-rockets.io/name`

- _meeting minutes_

## August 25, 2021

### Attendees:
- Justin Cormack (Docker)
- Steve Lasker (Microsoft)
- Marina Moore (NYU)
- Tianon
- Pritesh Bandi (AWS)
- Nate Waddington (CNCF)
- Christoph Hamsen (SSE / Connaisseur)
- _add yourself_

### Agenda Items:
- meeting chair, governance update (Justin)
- [Trust Policy and Trust Store Configuration](https://github.com/notaryproject/notaryproject/discussions/98) (Pritesh)
- [Notary Project website](https://notaryproject.dev) (Nate)
  - [Website & documentation project board](https://github.com/notaryproject/notaryproject.dev/projects/1)
  - [Documentation assessment](https://github.com/cncf/techdocs/blob/main/assessments/0002-notary-project.md)
  - [Information Architecture proposal, issue #23](https://github.com/notaryproject/notaryproject.dev/issues/23)
### Notes:
- _meeting minutes_

## August 18, 2021

### Attendees:
- Brandon Mitchell
- Nate Waddington (CNCF)
- Tianon
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Niaz Khan (AWS)
- Miloslav Trmač (Red Hat)
- Trishank Karthik Kuppusamy (Datadog)
- Dan Lorenc (Google)
- Marina Moore (NYU)
- _add yourself_

### Agenda Items:
- [Key Discovery](https://github.com/notaryproject/notaryproject/pull/66) (Niaz)
- [PR Scrubbing](https://github.com/notaryproject/notaryproject/pulls) (Steve)
- [Scoping Fall vs. Spring Releases](https://github.com/orgs/notaryproject/projects) (Steve)
- [Notary Project website](https://notaryproject.dev) (Nate)
  - [Website & documentation project board](https://github.com/notaryproject/notaryproject.dev/projects/1)
  - [Documentation assessment](https://github.com/cncf/techdocs/blob/main/assessments/0002-notary-project.md)
- _add your topics_

### Notes:
- Clarification for pull/66: Notary should include a mechanism for chain discovery to track which root a signature chains up to. This is not a m
- _meeting minutes_

## August 11, 2021

### Attendees:
- Brandon Mitchell
- Justin Cormack (Docker)
- Shiwei Zhang (Microsoft)
- Marina Moore (NYU)
- Dan Lorenc (Google)
- Sajay Antony (Microsoft)
- Steve Lasker (Microsoft)
- Tejaswini Duggaraju (Microsoft)
- Tianon
- Miloslav Trmač (Red Hat)
- _add yourself_

### Agenda Items:
- Governance update [github.com/theupdateframework/notary/pull/1606](https://github.com/theupdateframework/notary/pull/1606) (Justin via Lachie)
- Update on [Signature Format](https://github.com/notaryproject/notaryproject/pull/93) (Milind)
- Signing and Validation [discussion](https://github.com/notaryproject/notaryproject/discussions/94) (Milind)
- Scoping Fall vs. Spring Releases (Steve)
- Revisit prs discussed last week (Marina )
- _add your topics_

### Notes:
- Focus on JWS today, as it was what was approved by Microsoft and AWS Crypto boards, representing customer requirements. As DSSE evolves to meet the requirements, future versions can consider adopting DSSE based signatures. 
- Interopability - One of Notary v2's primary goals is the interoperability of content copying within and across private and public registries. Having a knwon signature format, for a particular version is core to that goal.
- Signing/verification needs not to directly depend on a registry client implementation or call out to cloud key management software, at the low level; allow integrating with these things, but also allow a purely in-memory operation.
    - Notary v2 has defined goals for extensibility to support cloud provider key valuts, or other key vault providers through extensibility so that it has no coupling to a specific implementation.
- What does Notary v2 sign: We'll focus on signing a descriptor, as it's the most generic registry object. This allows Notary v2 to consider blob signing (base layers) in the future, without reving the spec. The current notary client libraries will focus on manifests, prioritizing a certain experience, enabling it to evolve later.
- [OCI image-spec Layout](https://github.com/opencontainers/image-spec/blob/main/image-layout.md) for formatting registry objects on the filesystem (for disconnected portability and integration with other tooling)
- _meeting minutes_

## Aug 4, 2021

### Attendees:
- Brandon Mitchell
- Milind Gokarn (AWS)
- Miloslav Trmač (Red Hat)
- Tianon
- Shiwei Zhang (Microsoft)
- Pritesh Bandi (AWS)
- _add yourself_

### Agenda Items:
- Signature Format
    - [NV2 Signature Formats updates](https://hackmd.io/0GKGd0-1QQirbe1yty5vPg?view#Notary-v2-Signature-Formats) (Pritesh)
- Open PRs for review
    - [Trust Policy Management and Trust Store Updates](https://github.com/notaryproject/notaryproject/pull/89) (Milind) (Review: Marina)
    - [Signing Key Expiry](https://github.com/notaryproject/notaryproject/pull/87) (Shiwei) (Review: Pritesh)
    - [Signature Expiry](https://github.com/notaryproject/notaryproject/pull/88) (Shiwei) (Review: Milind)
    - [Timestamping](https://github.com/notaryproject/notaryproject/pull/92) (Shiwei) (Review: Marina, Pritesh)
    - [Signature Specification](https://github.com/notaryproject/notaryproject/pull/93) (Shiwei) (Review: Brandon)
    - [Attacker Goals](https://github.com/notaryproject/notaryproject/pull/76) (Marina) (Review: Milind, Brandon, Shiwei)
    - [Governance WIP](https://github.com/theupdateframework/notary/pull/1606) (Brandon) (Review: Marina, All) 


### Notes:
- [Signature Samples from Prototypes](https://hackmd.io/V7-71xB_R5-k8UrdNdhlBg?view)

## July 28, 2021


### Attendees:
- Tianon
- Brandon Mitchell
- Marina Moore (NYU)
- Joshua Lock (VMware)
- Trishank Karthik Kuppusamy (Datadog)
- Miloslav Trmač (Red Hat)
- Tejaswini Duggaraju (Microsoft)
- Shiwei Zhang (Microsoft)
- Milind Gokarn (AWS)
- Pritesh Bandi (AWS)
- _add yourself_

### Agenda Items:
- Signature Format
    - [NV2 Signature Formats](https://hackmd.io/0GKGd0-1QQirbe1yty5vPg?view#Notary-v2-Signature-Formats) (Pritesh)
- Open PRs for review
    - [Trust Policy Management and Trust Store Updates](https://github.com/notaryproject/notaryproject/pull/89) (Milind)
    - [Signing Key Expiry](https://github.com/notaryproject/notaryproject/pull/87) (Shiwei)
    - [Signature Expiry](https://github.com/notaryproject/notaryproject/pull/88) (Shiwei)
    - [Timestamping](https://github.com/notaryproject/notaryproject/pull/92) (Shiwei)
    - [Signature Specification](https://github.com/notaryproject/notaryproject/pull/93) (Shiwei)
- [TUF Design](https://github.com/notaryproject/nv2/blob/prototype-tuf/tuf-design.md) (Marina)

### Notes:
- [Governance WIP](https://github.com/theupdateframework/notary/pull/1606)
- [OCI Annotations](https://github.com/opencontainers/image-spec/blob/main/annotations.md)
- _meeting minutes_
    - Various discussion of the signature format, with notes captured in the [working document](https://hackmd.io/0GKGd0-1QQirbe1yty5vPg?view#Notary-v2-Signature-Formats).
- Discussion on signature annotations vs custom fields in signature envelop: deciding point may be whether that data would be useful to a downstream consumer of the descriptor. (Brandon)
- We can avoid namespace collisions in the annotations by reserving the `org.cncf.notary.*` for internal uses and reject that field for any user provided annotations (Brandon)



## July 21, 2021

### Attendees:
- Dan Lorenc (Google)
- Marina Moore (NYU)
- Shiwei Zhang (Microsoft)
- Trishank Karthik Kuppusamy (Datadog)
- Steve Lasker (Microsoft)
- Joshua Lock (VMware)
- Tianon
- Kavitha Krishnan (VMware)
- Brandon Mitchell
- Milind Gokarn (AWS)
- Pritesh Bandi (AWS)
- _add yourself_

### Agenda Items:
- TUF Requirements/Goals: https://github.com/notaryproject/nv2/pull/41 (Dan Lorenc)
- Signature Format
    - [Requirements updates](https://hackmd.io/Vz_tGRvGTL6Spmdpv8QulA?both#Requirements) (Milind)
    - [NV2 Signature Formats](https://hackmd.io/0GKGd0-1QQirbe1yty5vPg?view#Notary-v2-Signature-Formats) (Pritesh)
- Open PRs for review
    - [Trust Policy Management and Trust Store Updates](https://github.com/notaryproject/notaryproject/pull/89) (Milind)
    - [Signing Key Expiry](https://github.com/notaryproject/notaryproject/pull/87) (Shiwei)
    - [Signature Expiry](https://github.com/notaryproject/notaryproject/pull/88) (Shiwei)

### Notes:
- Discussion on TUF requirements/goals
  - why you need `snapshot` metadata to prevent rollback attacks of artifacts you haven't installed yet
  - Discussion of signature movement with TUF: https://github.com/notaryproject/nv2/blob/prototype-tuf/tuf-design.md#image-movement-withinbetween-registries
  - There are no concrete, formal processes for resolving PRs. Steve has asked Marina to close her PR, and open separate concerns as discussions instead. This is not a great resolution, as discussions can be ignored just as much as branches in a repo. We need to collectively agree on efficient processes for resolving PRs/issues/discussions, and not simply ignore them for months on end.
- Convert [Signature Format](https://hackmd.io/Vz_tGRvGTL6Spmdpv8QulA?view) in to a PR.
- _meeting minutes_

## July 14, 2021
Time: 0000 GMT (0700 PT; 1000 ET; 1600 CET; 2200 CST)

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Justin Cormack (Docker)
- Tianon
- Marina Moore (NYU)
- Dan Lorenc (Google)
- Trishank Karthik Kuppusamy (Datadog)
- Brandon Mitchell
- Milind Gokarn (AWS)
- Pritesh Bandi (AWS)
- _add yourself_

### Agenda Items:
- [DSSE discussion](https://github.com/secure-systems-lab/dsse/issues/39) (Marina)
- [Signature Format followup on last week's discussion](https://hackmd.io/_vrqBGAOSUC_VWvFzWruZw?both#Notes1) (Milind)
    - TSA Support
    - Signature envelope and multiple signatures, multiple blobs
    - Indicating signature algo and other params
    - Custom attributes in signature payload
- PRs for review
    - [Trust Policy Management and Trust Store Updates](https://github.com/notaryproject/notaryproject/pull/89) (Milind)
    - [Signing Key Expiry](https://github.com/notaryproject/notaryproject/pull/87) (Shiwei)
    - [Signature Expiry](https://github.com/notaryproject/notaryproject/pull/88) (Shiwei)

### Notes:
- Specify only 1 signature in the envelope for Notary v2 in the spec.
- Concerns with separating blobs for signing and certificate chain
    - Packaging could have an "collection" of blobs, and that collection may inline the data of the embedded blob using the [data field](https://github.com/opencontainers/image-spec/pull/826). (Brandon)
    - It's ideal for a Signing component/service to produce a single signature envelope that contains the payload, TSA signature, cert chain and paylod signature. If these are seperated into differrent blobs then the signing component either needs to be called muliple times of respond with a response containing multiple fields, either of which seems to introduce unnecesarry complexity.
- [Pointer to storing a "hint" to which key](https://github.com/SteveLasker/artifacts/blob/oci-artifact-manifest/manifest-referrers-api.md). See annotations example result of artifacts that reference the net-monitor image `"org.cncf.notary.v2.signature.subject": "wabbit-networks.io"`: 
    ```json
    {
      "references": [
        {
          "digest": "sha256:3c3a4604a545cdc127456d94e421cd355bca5b528f4a9c1905b15da2eb4a4c6b",
          "manifest": {
            "schemaVersion": 3,
            "mediaType": "application/vnd.oci.artifact.manifest.v1-rc1+json",
            "artifactType": "cncf.notary.v2-rc1",
            "blobs": [
              {
                "mediaType": "application/tar",
                "digest": "sha256:9834876dcfb05cb167a5c24953eba58c4ac89b1adf57f28f2f9d09af107ee8f0",
                "size": 32654
              }
            ],
            "subjectManifest": {
              "mediaType": "application/vnd.oci.image.manifest.v1+json",
              "digest": "sha256:3c3a4604a545cdc127456d94e421cd355bca5b528f4a9c1905b15da2eb4a4c6b",
              "size": 16724
            },
            "annotations": {
              "org.cncf.notary.v2.signature.subject": "wabbit-networks.io"
            }
          }
        },
        {
          "digest": "sha256:3c3a4604a545cdc127456d94e421cd355bca5b528f4a9c1905b15da2eb4a4c6b",
          "manifest": {
            "schemaVersion": 1,
            "mediaType": "application/vnd.oci.artifact.manifest.v1-rc1+json",
            "artifactType": "example.sbom.v0"
          },
          "blobs": [
            {
              "mediaType": "application/tar",
              "digest": "sha256:9834876dcfb05cb167a5c24953eba58c4ac89b1adf57f28f2f9d09af107ee8f0",
              "size": 32654
            }
          ],
          "subjectManifest": {
            "mediaType": "application/vnd.oci.image.manifest.v1+json",
            "digest": "sha256:3c3a4604a545cdc127456d94e421cd355bca5b528f4a9c1905b15da2eb4a4c6b",
            "size": 16724
          },
          "annotations": {
            "example.sbom.author": "wabbit-networks.io"
          }
        }
      ],
      "@nextLink": "{opaqueUrl}"
    }
    ```
    - The lookup the key could also be based on a hash of the root key (or intermediates). (Brandon)
    - Advantage of a hash instead of a named field is the hash will point back to a specific key, where a name could be copied by a mistaken user claiming they have the "Docker Hub" root for signing their data when that may not be the case. (Brandon)
    - Hash itself does not need to be secure, it's a method to lookup/query which certificate chain the client wants to pull and later validate. (Brandon)
- Request for a diagram for the various signing envelop options. (Brandon)
- Steve- Next steps to prototype the payload formats, including merging DSSE with some proposed TSA properties to provide feedback to DSSE. However, there's concern we can't do two prototypes. JWT and JWS with DSSE. 
- Payload being signed could be a descriptor pointing to the image, and that descriptor could include different annotations, the digest, and size. (Justin)
    - This has been specified in [Notary v2 - Signature Format](https://hackmd.io/Vz_tGRvGTL6Spmdpv8QulA?view#Payload). (Shiwei)
- Signature algorithm can be a signed attribute in cases where it cannot be determined by the key in cert chain. Notary V2 can have mapping for signature alg to specific encryption + hash alg in these cases similar to JWT alg mapping.
- Custom attributes will be stored in payload, details will be part of payload structure we'll add to Signature format doc, and discussed next week. (Milind)
- _meeting minutes_

## July 9, 2021
8am Pacific Time

### Attendees:
- Steve Lasker (Microsoft)
- Lachlan Evenson (Microsoft)
- Shiwei Zhang (Microsoft)
- Brandon Mitchell
- Miloslav Trmač (Red Hat)
- Tianon
- Tejaswini Duggaraju (Microsoft)
- Marina Moore (NYU)
- Dan Lorenc (Google)
- Trishank Karthik Kuppusamy (Datadog)
- Pritesh Bandi (AWS)
- _add yourself_

### Agenda Items:
- Identify owners and next steps to convert hackdocs to PRs (Steve)
    - [Key Management - Rescinding Signatures #72](https://github.com/notaryproject/notaryproject/issues/72) (Milind)
    - [Key Management - Signature Expiry #81](https://github.com/notaryproject/notaryproject/issues/81) (Shiwei)
    - [Key Management - Signing Key Expiry #84](https://github.com/notaryproject/notaryproject/issues/84) (Shiwei)
    - [Key Management - Rescinding Signature Validity  #85](https://github.com/notaryproject/notaryproject/issues/85) (Milind)
    - [Key Management - TSAs #82](https://github.com/notaryproject/notaryproject/issues/82) (Shiwei)
    - [Key Management - Trust Policy Management and Trust Store Updates #83](https://github.com/notaryproject/notaryproject/issues/83) (Milind)
    - [Key Management - Signature Format](https://github.com/notaryproject/notaryproject/issues/86) (Shiwei)
- _add your topics_


### Notes:
- signature format security issues
    - [vulnerabilities in nv1 due to signature algorithm](https://github.com/theupdateframework/notary/blob/master/docs/resources/ncc_docker_notary_audit_2015_07_31.pdf)
    - Why [signing algos and parameters should not be communicated in unsigned payload](https://github.com/secure-systems-lab/dsse/issues/35)
    - [Exclusive ownership problem](https://github.com/secure-systems-lab/dsse/pull/37#issuecomment-864723336) may apply when public keys are not distributed in a trustworthy manner, such as in the signed payload itself
- Can DSSE do what we want?
    - [Discussion on timestamps with DSSE](https://github.com/secure-systems-lab/dsse/issues/39#issuecomment-876610697)
    - Does DSSE allow some cloud providers to add extra parameters in the signed payload if they wanted to? Yes, it should, because it is completely agnostic to the contents of the payload itself. When we define our payload, we should be careful to allow custom, optional attributes.
- Are there updates on the governance issue?
    - Waiting for updates from Justin Cormack. Might ask him to delegate.
- Stable Go libraries
    - For DSSE? [link here]
        - If the implementation is in the in-toto repo, can we make a standalone repo with just DSSE in it?
        - Here is the in-toto golang [implementation](https://github.com/in-toto/in-toto-golang/commit/5b9e472f1a6e04f14d62266dd8e24749c2e9900c)
    - For TSA/RFC3161?
- _meeting minutes_

## July 2, 2021

[Recording](https://youtu.be/U1r00FFbGfY)

### Attendees:
- Marina Moore (NYU)
- Justin Cormack (Docker)
- Dan Lorenc (Google)
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Kavitha Krishnan (VMware)
- Brandon Mitchell
- Niaz Khan (AWS)
- Milind Gokarn (AWS)
- Michael Hough (IBM)
- Tianon (InfoSiftr)
- Miloslav Trmač (Red Hat)
- Joshua Lock (VMware)
- _add yourself_

### Agenda Items:
- Review GOVERNANCE PR and agreed on how to proceed with seed maintainers - https://github.com/notaryproject/notaryproject/pull/78#discussion_r658936040 (Lachlan however I'll be out on vacation)
- [New Notary v2 meeting time doodle poll](https://doodle.com/poll/dut73p9ys9dirtxi) to provide for Asia and UK participants (Steve)
- Provide feedback on updated version of [Signature Format](https://hackmd.io/Vz_tGRvGTL6Spmdpv8QulA?view) design (Milind)
- _add your topics_

### Notes:

- YouTube playlist not updated, Steve looking into it
- Justin will be pushing a different governance doc that should be simpler, but also handles sub-groups, targetting 5 mods that can approve PRs, but could have more if we have active maintainers
- [Notary Project page](https://github.com/orgs/notaryproject/projects) exists to track goals
- Next week should focus on Signature Format discussion, ensuring needed extensibility exists, and whether features should go into payload or signature envelope
- _meeting minutes_

## June 25, 2021
[Recording](https://youtu.be/aRsoUjYwhx8)
### Attendees:
- Marina Moore (NYU)
- Lachlan Evenson (Microsoft)
- Tianon (InfoSiftr)
- Brandon Mitchell
- Miloslav Trmač (Red Hat)
- Dan Lorenc (Google)
- Shiwei Zhang
- Serge Hallyn
- Tejaswini Duggaruju
- Tianon Gravi
- Iahiru
- Kavitha Krishnan (VMWare)
- Milind Gokarn (AWS)
- _add yourself_

### Agenda Items:
- Project governance and contributor guidelines (Brandon)
    - Goal - get workflow going to get things into the project
- Continue iterating on [Signature Format](https://hackmd.io/Vz_tGRvGTL6Spmdpv8QulA?view) design (Milind)
- [Scenario for revoking signatures](https://github.com/notaryproject/notaryproject/pull/49) looking for approval (Brandon)
- [Document describing key revocation](https://github.com/notaryproject/notaryproject/pull/47) can this be approved (Brandon)
- _add your topics_

### Notes:
- Will work on getting a governance policy defined - Lachlan
- Add Work in Progress notice in README - Lachlan (https://github.com/notaryproject/notaryproject/pull/79)
- Potential maintainers should raise a PR nominating themselves with their GitHub ID.
- How can we make promises to the community without agreement - Marina - https://github.com/notaryproject/notaryproject/issues/77
- There are different workstreams happening and people are being caught offguard - Can we communicate more with the larger group - Lachlan
- _meeting minutes_

## June 18, 2021

[Recording](https://youtu.be/SggZaqW8Ua0)

### Attendees:
- Brandon Mitchell
- Marina Moore (NYU)
- Hank Donnay (quay)
- Miloslav Trmač (Red Hat)
- Dan Lorenc (Google)
- _add yourself_ 

### Agenda Items:
- Status update on [Signature Format](https://hackmd.io/Vz_tGRvGTL6Spmdpv8QulA?view) design (Milind)

### Notes:
- _meeting minutes_

## June 11, 2021

[Recording](https://youtu.be/p0RBGXpUoeA)

### Attendees:
- Brandon Mitchell
- Jackline Mutua (VMware)
- Miloslav Trmač (Red Hat)
- _add yourself_ 

### Agenda Items:
- Review changes to [key discovery scenarios](https://github.com/notaryproject/notaryproject/pull/66) (Marina)

### Notes:
- _meeting minutes_
 
## June 4, 2021

[Recording](https://youtu.be/F51oXAwGNvs)

### Attendees:
- Brandon Mitchell
- Tianon (InfoSiftr)
- Joao Pereira (VMware)
- Steve Lasker (Microsoft)
- Miloslav Trmač (Red Hat)
- Marina Moore (NYU)
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- _add yourself_

### Agenda Items:

- [Key revocation approaches](https://github.com/notaryproject/notaryproject/pull/47) (Marina)
- Review changes to [key discovery scenarios](https://github.com/notaryproject/notaryproject/pull/66) (Marina)
- Update on design documents (Milind)

### Notes:
- Key revocation
    - Marina to generalize PR#47
    - Milind to merge the key revocation hackmd doc onto the contents of #47
- Key Discovery
    -  #10 as written can merge
    -  Marina will iterate on 11 as there was discussion on the granularity of key management.
- _meeting minutes_

## May 28, 2021

### Attendees:
- _add yourself_

### Agenda Items:

- cancelled

### Notes

## May 21, 2021

[Recording](https://youtu.be/nWQBAyjzjgM)

### Attendees:
- Steve Lasker (Microsoft)
- Joao Pereira (VMware)
- Tianon
- Serge Hallyn (Cisco)
- Brandon Mitchell
- Marina Moore
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- _add yourself_

### Agenda Items:
- Review [revocation requirements](https://hackmd.io/2rc07WwHTdmPjpgoMbvYfA?view) (cover open issues from last week) (Milind Gokarn)
- Discuss [key revocation approaches](https://github.com/notaryproject/notaryproject/pull/47) (Marina)
- Review changes to [key discovery scenarios](https://github.com/notaryproject/notaryproject/pull/66) (Marina)
- Reviewing [OPA PR](https://github.com/notaryproject/nv2/pull/62) (Daniel)
- _add your topics_

### Notes


## May 14, 2021

[Recording](https://youtu.be/TOX_DBccBRQ)

### Attendees:
- Brandon Mitchell
- Marina Moore (NYU)
- Tianon
- Joao Pereira (VMware)
- Michael Hough (IBM)
- Steve Lasker (Microsoft)
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- Paavan Mistry (AWS)
- _add yourself_

### Agenda Items:
- Review [revocation requirements](https://hackmd.io/2rc07WwHTdmPjpgoMbvYfA?view) document (Milind Gokarn)
- _add your topics_

### Notes:
- Consider whether there's only fail open or fail closed. A potential 3rd option is to have an expiration window on signatures that has `$n` expiration, and the signer expects to refresh at `$n/2` time, giving a `$n/2` window to recover from a failure until deployers are impacted. (Brandon)
- Should revist the fail open/closed decision and make sure everyone is in agreement. (Brandon) This may not be needed if it's a user configurable setting.
- A list of infrastructure needed by air-gapped environments to maintain to implement the solution would be useful (Brandon)

## May 7, 2021

Cancelled due to KubeCon focus/catchup

## April 30, 2021

### Attendees:
- Steve Lasker (Microsoft)
- Shiwei Zhang (Microsoft)
- Marina Moore (NYU)
- Tianon
- Hank Donnay (Quay)
- Serge Hallyn (Cisco)
- Brandon Mitchell
- Niaz Khan (AWS)
- _add yourself_

### Agenda Items:
- Review requirements for (Niaz)
    - Key expiry - https://hackmd.io/n82ZTBv3TK2Y4rujlnW3ng
    - Signature expiry - https://hackmd.io/pT4IicsQRlGhR9szlrIUWQ (not covered on 4/30)
- [Key discovery scenarios](https://github.com/notaryproject/notaryproject/pull/66)

### Notes:
- Short term vs long term keys depends on threat scenarios. Long term signing keys protect the issuer from frequently issuing new keys. Short term signing keys protect from a compromised signer.
- Recognition we should add some overviews for the decentralized model we're enabling and assuming with Notary v2. 
- _meeting minutes_

## April 23, 2021

### Attendees:
- Steve Lasker (Microsoft)
- Marina Moore (NYU)
- Paavan Mistry (AWS)
- Tianon
- Brandon Mitchell
- Michael Hough (IBM)
- Niaz Khan (AWS)
- Samir Kakkar (AWS)
- Milind Gokarn (AWS)
- Furkat Gofurov (Ericsson)
- Serge Hallyn (Cisco)
- _add yourself_

### Agenda Items:
- [Key Management Requirements PR#38](https://github.com/notaryproject/notaryproject/blob/5d77d981fa4fe66a3a47e75df6030b4d7a3fad83/keymanagementrequirements.md) (Niaz)
- _add your topics_

### Notes:     
- Need to add some key management scenarios
    - specifying a key for a particular artifact
    - trusted artifacts: what goes here?
    - does scope fall through
- Move open topics to issues so PR can be merged with open discussions being discussed as issues.
- Brandon: `scope` could be moved up to trust policy
- Brandon: in `trustedRoots` add a `name` element
- Marina: it's possible to have metadata/signatures expire without having to constantly re-sign
- Signature expiry
    - Add a step-by-step scenario with short lived CI signing key, how that gets extended with timestamp service, what gets pushed to the registry, and how do clients know to trust
    - What happens if timestamp root is compromised
    - What needs to be updated on the registry
- _meeting minutes_

## April 16, 2021

### Attendees:
- Niaz Khan (AWS)
- Steve Lasker (Microsoft)
- Miloslav Trmač (Red Hat)
- Marina Moore (NYU)
- Brandon Mitchell
- Mauren Berti (VMware)
- Tianon
- Hank Donnay (Quay)
- Joao Pereira (VMware)
- Ralph Squillace (Microsoft)
- Serge Hallyn (Cisco)
- Jan Tilles (Ericsson)
- Furkat Gofurov (Ericsson)
- Sravan Rengarajan (AWS)
- Paavan Mistry (AWS)

### Agenda Items:
- Trust Policy and Trust Store Management - https://github.com/notaryproject/notaryproject/pull/38 (Niaz)
- _add your topics_

### Notes:
- Need to add a "Policy" definition and start to identify what we can include in a policy.
- How do we handle artifacts that can come from multiple locations (mirrors)?
- There's a need to limit what repositories a key is permitted to sign, rather than approve anything a key signs.
- Discussing if and how artifacts could be verified with any name based on just the signer to remove the name of the registry and repository from the validation.
- What is the output of the Trust Policy? "Allow", "Deny", and discussion on whether "Warn" should be a third option.
- Steve - we're touching on the content movement issue. How do we trust a thing, regardless for where it's coming from? How can we decouple where something is stored from what we trust?
- Paavan Mistry - Would it be useful to extend the Wabbit Networks/ACME scenario to demonstrate and define the trust policy and store in this doc?
- Steve - ^ yes, great suggestion to incorporate
- Brandon Mitchell - The ideal for me is a client side mapping, deployer has a list of permitted mappings that it permits to allow repo/tag to validate in a different location.
- Miloslav Trmač - Yes, the client must configure a specific mapping of expected image movement/mirrors. Without a mapping to allow specific movements, “trust regardless where it’s coming from” collapses to unbounded “allow any key trusted for some purpose, however small, for any artifact at all”
- Ralph Squillace - I am skeptical that any identity of an artifact should require a url. The argument that Microsoft can't be hijacked is likely mostly true; but what about squillace.com? smaller domains **can** and yet there must be another way to understand and verify identity of the artifact even if the domain was.
- Joao Pereira - But isn’t that policy?
- Miloslav Trmač It’s very convenient when the identity _looks_ like a location because everyone is already specifying a location when pulling. It doesn’t have to be the physical location from where that the content is actually downloaded — that’s basically the same kind of client mapping policy.
- Steve Lasker - Docker is one of the unique package types where the location is tied to the type. This is something we're hoping to decouple with artifact mappings. So, I'm hoping we don't create more dependencies on location for signing validation.
- Milind Gokarn - The better analogy than TLS/TLS certs would be code signing certs, software signed with say authenticode would be trusted irrespective of where it was downloaded from.
- Ralph Squillace - containers tied to location of storage was one of the most RESTful but poor design... incompletions that we experienced in this space. #hotTake
- From Brandon Mitchell - I think the question here is do we want that, when we have the ability to limit that trust with the registry/repo design while we don't have that ability to limit scope with code signing.
- Miloslav Trmač -If Authenticode signs a kernel driver, it doesn’t really matter anymore what the purpose of the driver was because it has SYSTEM level access anyway; with isolated containers, it makes much more sense to distinguish between publishers and individual container identities
- Steve Lasker - current nv2 sample "trust policy" - overly simply allow list
     ```json
     {
        "enabled": true,
        "verificationCerts": [
            "/home/stevelas/nv2-demo/wabbit-networks.crt"
        ]
     }
     ```
- Brandon Mitchell- I'd push for only having "allow" or "deny" and make "warning" or other capabilities an externality that could be implemented within the policy
- Sravan Rengarajan - +1 allow or deny* are tablestakes 
- Miloslav Trmač +1; “warning” is unactionable.
- Sravan Rengarajan - just like that policy snippet from the prototype, is there an example json response with scenarios of how the policy passed or failed?

## April 9, 2021

### Attendees:
- Jan Tilles (Ericsson)
- Brandon Mitchell
- Steve Lasker (Microsoft)
- Mauren Berti (VMware)
- Joao Pereira (VMware)
- Tianon
- Niaz Khan (AWS)
- Furkat Gofurov (Ericsson)
- Milind Gokarn (AWS)
- Samir Kakkar (AWS)
- Dan Lorenc (Google)
- Serge Hallyn (Cisco)

### Agenda Items:
- Revisit [threat model](https://github.com/notaryproject/notaryproject/pull/35/files) and [attacker scenarios](https://github.com/notaryproject/notaryproject/pull/33/files) (Marina)
- Review scope for additional key management requirements https://github.com/notaryproject/notaryproject/pull/38 (Niaz)

### Notes:
- To capture the definition of key hierarchy
- Key management is extensible. Users can integrate with their key management system, and Notary will suppor that flexibility
- _meeting minutes_

## March 29, 2021

### Attendees:
- Steve Lasker (Microsoft)
- Hank Donnay (Quay)
- Robert Szumlakowski (VMware)
- Furkat Gofurov (Ericsson)
- Jan Tilles (Ericsson)
- Niaz Khan (AWS)
- Brandon Mitchell
- Mauren Berti (VMware)
- Joao Pereira (VMware)
- Stuart Hayton (IBM)
- Jackline Mutua (VMware)
- Marina Moore (NYU)
- Serge Hallyn (Cisco)
- _add yourself_

### Agenda Items:
- [New time Doodle](https://doodle.com/poll/97sti3k684dhhmu4?utm_source=poll&utm_medium=link) (Serge, Marina)
- [Repos](https://github.com/notaryproject/notaryproject/issues/51), Branching & Releases (Steve)
- [OPA/Validation](https://github.com/notaryproject/notaryproject/issues/61) (Daniel  from NTTData)
- Possible move from `oci.artifact.manifest` to Justin's [new generic manifest proposal](https://gist.github.com/justincormack/523dc229f0dd7b882edf19c60aed1581), [moved to WIP PR under OCI-artifacts](https://github.com/opencontainers/artifacts/pull/37) (Justin or Steve)
- Signature format: https://github.com/notaryproject/nv2/issues/39 (Dan)
- Short lived vs. long lived keys? (Dan)

### Notes

- Short vs Long key options: [PR 47](https://github.com/notaryproject/notaryproject/pull/47)

## March 22, 2021

### Attendees:
- Steve Lasker (Microsoft)
- Ralph Squillace (Microsoft)
- Marina Moore (NYU)
- Miloslav Trmač (Red Hat)
- Dennis Leon (VMware)
- Brandon Mitchell
- Jan Tilles (Ericsson)
- Mauren Berti (VMware)
- Sumana Harihareswara (NYU) [had to leave early]
- Niaz Khan (AWS)
- Robert Szumlakowski (VMware)
- Dan Lorenc (Google)
- Serge Hallyn (Cisco)
- Samuel Karp (AWS)
- Furkat Gofurov (Ericsson)
- Jackline Mutua (VMware)
- _add yourself_

### Agenda Items:
- Prototype (Steve)
    - [Prototype 1 Scope](https://github.com/notaryproject/notaryproject/issues/3)  - complete
    - [Prototype 2 Scope](https://github.com/notaryproject/notaryproject/issues/4) - underway
    - [Prototype 3 Scope](https://github.com/notaryproject/notaryproject/issues/5) - draft, with details needed for what we want and don't expect to achieve in this phase.
- Key Management PRs
- Status of signature and payload specifications? Timeline for moving out of prototype branch (Dan)
- Project Structure/Governance stuff: https://github.com/notaryproject/notaryproject/issues/2 (Dan)
- _add your topics_

### Notes:
- Prototype 1 [certificate?] prototype discussion/status -- incubating
    - request for details/clarification on, e.g., integrity checking, need to re-sign things, signature flow
    - NOT using Trust on First Use
    - concerns about putting the string in the certificate....
        - response: *a* place user can verify -- user goes *back* to that place to get the content
        - Users may push to multiple registries and want to sign using the same certificate (Brandon)
        - The signer of a key is more important than the CN value on the certificate (Brandon)
        - Goal is to have a secondary check that key was signed by an upstream entity (Steve)
    - is it a business or technical decision re: key management & whom the user default trusts?
    - question re optionality of CNAME, fundamental structure/usage of x.509 certificate
    - need better clarity re dummy data in this demo, example & root CA & what client trusts
        - We should update the demo to include a minimal chain of trust
    - some of this conversation overlaps with key management -- separate from conversations on persistence, etc. -- but those outcomes may lead to changes in certificate structure
    - need to file these issues, tag them, reduce need for future re-clarification for new entrants
- Prototype 2 [better name that covers waht this covers?] discussion/status
    - Prototype 2 validates the Artifact spec with Notary as a use case


## March 15, 2021
[Recording](https://www.youtube.com/watch?v=mBzZ7_FrMZw)

### Attendees:
- Dennis Leon (VMware)
- Brandon Mitchell
- Steve Lasker (Microsof)
- Marina Moore (NYU)
- Mauren Berti (VMware)


### Agenda Items:
- [Aligning TUF design with Notary v2 goals](https://github.com/notaryproject/nv2/pull/41) (Marina)
- [Adding scenario for tag signing](https://github.com/notaryproject/requirements/pull/48) (Brandon)
- [Adding scenario for revoking trust in an artifact](https://github.com/notaryproject/requirements/pull/49) (Brandon)
- Prototype 2 & 3 goals (Steve)
- _add your topics_

### Notes:
- Need to revise TUF design as key management goals are merged in
- Question about how TUF allows multiple signatures
    - TUF targets metadata files are independent, but each targets metadata can have multiple signatures
    - Allows clients to set policy by defining their own top-level targets metadata
    - Marina will add a diagram or example metadata (with a white background)
- How to minimize security losses when separating registries into many roots for privacy reasons?
    - Snapshot merkle trees and auditing can give you similar protection (like a transparancy log)
- What are the benefits of combining repositories into the same root?
    - More protection against rollback attacks on metadata from the snapshot metadata
    - Increased auditability
    - Simplified key management if the user needs to access less roots
    - Marina will add a diagram/description
- Discussion about balancing tag signing and pulling old version by digest
    - TUF needs to continue to list older digests and signatures if they are not revoked
    - Allow for company policy for whether to pull by tag or digest
- How to diferentiate between valid and malicious rollback
    - Always roll forward: new revision with the same digest
    - Also need to protect against a fast forward attack
- Revoking a signature
    - Why not just delete?
        - Can it be securely deleted?
    - What is the purpose of signing something? Does it attest to security?
    - Revoking a signature is a finer scale than revoking a key - it only applies to the one artifact
    - Make sure that something that's revoked can't be replayed
- Prototypes
    - Add tag signing
    - Differentiate originating signatures?
    - TUF integration in a prototype
- _meeting minutes_


## March 8, 2021
[Recording](https://www.youtube.com/watch?v=tmAQAVATbMQ)

### Attendees:
- Niaz Khan (AWS)
- Joao Pereira (VMware)
- Dennis Leon (VMware)
- Robert Szumlakowski (VMware)
- Brandon Mitchell
- Steve Lasker (Microsoft)
- Samuel Karp (AWS)
- Mauren Berti (VMware)
- Jackline Mutua (VMware)

### Agenda Items:
- Key Management Updates (Revised pull request https://github.com/notaryproject/requirements/pull/38)
- [TUF Prototype specification](https://github.com/notaryproject/nv2/pull/38) (Marina)
- _add your topics_

### Notes:
- Added key management requirement document
- [Notary v2 demo script](https://github.com/notaryproject/nv2/blob/prototype-1/docs/nv2/demo-script.md) Updated demo steps to fix bugs
- Plan to make a similar demo for key management
- TUF prototype specification describes how TUF prototype can be made to work with distribution work
- TUF addresses key management requirements (discovery, key revocation)
- Notary registry implementation: aiming for generic storage of artifacts. Can iterate for key management/TUF requirements
- Can we combine TUF work with registry implementation? Steve will work on demo for next week
- Marina will connect TUF to Notary requirement documents (https://github.com/notaryproject/nv2/pull/41)
- Need to define interfaces in prototypes so that they can fit together
- Need to focus on reviewing and merging open requirements prs
- _meeting minutes_


## March 3, 2021

[Recording](https://www.youtube.com/watch?v=TyDvb_SiJOQ)

### Attendees
- Niaz Khan (AWS)
- Marina Moore (NYU)
- _add yourself_

### Agenda Items:
- Key Management Prototype Components
    - Keys used for signing
    - Key rotation
    - Trust store configuration and signature source validation
    - Signature allowlist/denylist
- Key Rotation Requirement (Doc outline)
- Signature/Key Allowlist/Denylist 
    - Review https://github.com/notaryproject/requirements/pull/47
    - Determine next steps
- _add your topics_

### Notes:
- Overall prototype components are good. We may in the future decide to merge prototypes based on alignment in Key Rotation and Signature/Key Allowlist/Denylist discussions. Will share with larger group in 3/8 meeting
- Updated outline for key rotation requirements in https://github.com/notaryproject/requirements/pull/38/commits/3a7100a541dae95784488477e0f763fd25a5ef66. Niaz and Marina to work on this doc for 3/15 meeting.
- The https://github.com/notaryproject/requirements/pull/47 covers three areas, key expiration, signature/key allowlist/denylist and key distribution. Discussed covering these as individual topics. Detailed feedback will be tracked as comments.
- Schedule weekly call at 10 AM ET on Wednesdays going forward.


## March 1, 2021
[Recording](https://www.youtube.com/watch?v=oF0ydMcUOfc)

### Attendees:
- Niaz Khan (AWS)
- Dennis Leon (VMware)
- Steve Lasker (Microsoft)
- Garry Ing (VMware)
- Brandon Mitchell
- Robert Szumlakowski (VMware)
- Jackline Mutua (VMware)
- Samuel Karp (AWS)
- Marina Moore (NYU)
- Serge Hallyn (Cisco)
- Paavan Mistry (AWS)

### Agenda Items:
- Identify next phases of prototypes, with an open invite for folks to contribute (Steve)
- _add your topics_

### Notes:

- Next round of prototypes:
    - OPA/Gatekeeper validation w/k8s
    - Complete CNCF distribution/distribution implementations
        - [Add support for linked artifacts #3](https://github.com/notaryproject/distribution/pull/3)
        - [Add OCI Artifact Type #31](https://github.com/opencontainers/artifacts/pull/31)
        - https://github.com/shizhMSFT/notary
        - https://github.com/sajayantony/nv2-demo
    - ORAS
- Continued maintanance of Notary v1? Probably not, Notary v2 will replace Notary v1
- Concern about moving forward with prototypes without a plan for key management
- Key revocation especially is blocking
- Other prototypes can still move forward.
- Discussion around key management and revocation, Marina and Niaz will work on a document of a possible solution.
- Key managment working session planned for Wednesday 10am EST on same zoom link.
- Challenges with adding to OPA/Gatekeeper upstream. Can extend locally, but harder to distrubute extensions to Gatekeeper instances
- Need input from OPA/Gatekeeper community
- _meeting minutes_

## February 22, 2021

[Recording](https://www.youtube.com/watch?v=8HMpVsXSiGQ)

### Attendees:
- Joao Pereira (VMware)
- Garry Ing (VMware)
- Steve Lasker (Microsoft)
- Hank Donnay (Quay)
- Brandon Mitchell
- Niaz Khan (AWS)
- Marina Moore (NYU)
- Mauren Berti (VMware)
- Robert Szumlakowski (VMware)
- Omar Paul (AWS)
- Samuel Karp (AWS)
- Serge Hallyn (Cisco)
- Paavan Mistry (AWS)

### Agenda Items:
- [Key Management Requirements](https://github.com/notaryproject/requirements/pull/38) - Niaz
- [Publishing the Notary v2 Status - feedbck before publishing?](https://github.com/notaryproject/notaryproject/pull/1)
- SBoM Working Group quick update (Steve)
- _add your topics_

### Notes:
- _meeting minutes_

## February 15, 2021

### Agenda Items:
- cancelled due to the US holiday

## February 8, 2021

[Recording](https://www.youtube.com/watch?v=itYqzloJKro)

### Attendees:
- Steve Lasker (Microsoft)
- Andy Goldstein (VMware)
- Brandon Mitchell
- Joao Pereira (VMware)
- Manish Dangi(Student India)
- Miloslav Trmač (Red Hat)
- Niaz Khan (AWS)
- Samuel Karp (AWS)
- Omar Paul (AWS)
- Serge Hallyn (Cisco)
- Marina Moore (NYU)
- Mauren Berti (VMware)
- _add yourself_

### Agenda Items:
- Container Signing Demo - Dan Lorenc (Google)
- Key Management Requirements (https://github.com/notaryproject/requirements/pull/38)
- _add your topics_

### Notes:
- Dan is from Google, working on signing solutions
    - Presenting [cosign](https://github.com/projectcosign/cosign)
    - Similar to minisign and signify
    - Using the Red Hat SimpleSigning format with the Google binary auth service
- _meeting minutes_

## February 1, 2021

[Recording](https://www.youtube.com/watch?v=eAjXTG1nhZM)

### Attendees:
- Steve Lasker (Microsoft)
- Joao Pereira (VMware)
- John Ryan (VMware)
- Garry Ing (VMware)
- Brandon Mitchell
- Josh Dolitsky
- Peter Engelbert
- Samuel Karp (AWS)
- Marco Franssen (Philips - Research)
- Niaz Khan (AWS)
- Rio Kierkels (UvA: SNE Master Student)
- Hank Donnay (Quay)
- Serge Hallyn (Cisco)
- Marina Moore (NYU)
- Paavan Mistry (AWS)
- Mauren Berti (VMware)
- _add yourself_

### Agenda Items:
- Status Update (Steve)
- Work through backlog of issues and PRs (Steve-group)
- Hackmd.io performance: Archive these notes to a repo under https://github.com/notaryproject/ (Steve)
- [How to enable dynamic (delegation) certificates in CI? #44](https://github.com/notaryproject/requirements/discussions/44) (Marco)
- [What should the root key cover](https://github.com/notaryproject/nv2/discussions/27) (Marina)
- New timeslot?
- _add your topics_

### Notes:
- Status Update - steve to get a doc out this week, with time for feedback to provide a status for others to read as well.
- [Quay update for Hank](https://github.com/notaryproject/requirements/pull/39) Merged 
- Brandon will add a PR to cover [issue #43](https://github.com/notaryproject/requirements/issues/43)
- Discussion around whether Docker Hub would sign user repos to verify image came from logged in user. Potentially better than trust on first use.
- Looking for volunteers to help with key management scenarios.
- Steve looking for volunteer to run a poll for finding a better time slot.
- Steve also looking at new cncf-provided meeting venue, so link may change.  (check HackMD)
- [More information about the TUF design](https://github.com/notaryproject/nv2/tree/prototype-tuf)
- [Discussion on manifest list API](https://github.com/opencontainers/distribution-spec/issues/222)
- Paavan Mistry
  Would there be a limit to how many signatures that can be attached?
  - Steve 
  There could be, but that would be a client config. At least that's the current thinking.
- Jon 
  public registries should use something like transparency logs for tags... shoving this requirement into notary feels like scope creep
- Niaz Khan
  We should have this be individual organizations. If you  haven't heard of Wabbit Networks, why would you trust their software?
## January 25, 2021

[Recording](https://www.youtube.com/watch?v=14c7tcM1MAk)

### Attendees:
- Steve Lasker (Microsoft)
- Rio Kierkels (UvA: SNE Master Student)
- Mohanad Elamin (UvA: SNE Master Student)
- Niaz Khan (AWS)
- Hank Donnay (Quay)
- Marco Franssen (Philips - Research)
- Samuel Karp (AWS)
- Omar Paul (AWS)
- Paavan Mistry (AWS)
- Brandon Mitchell
- Miloslav Trmač (Red Hat)
- Marina Moore (NYU)

### Agenda Items:
- [OCI Artifact/Notary v2 Signature Persistance Updates](https://github.com/SteveLasker/artifacts/blob/artifact-manifest/artifact-manifest/artifact-manifest.md) (steve)
- [Scenarios for types of artifacts and delayed verification](https://github.com/notaryproject/requirements/pull/41) (Brandon)
- [Should tags be signed in addition to digests?](https://github.com/notaryproject/requirements/issues/43) (Brandon)
- [Scenario for clients to limit trust of a signing key](https://github.com/notaryproject/requirements/issues/42) (Brandon)
- [TUF Implementation Discusions](https://github.com/notaryproject/nv2/discussions?discussions_q=%5BTUF%5D) (Brandon)
- Should Roots be tied to Registry/Repository? (Niaz)
- SPIFFE/Spire (some thoughts)
- Marco: PodMan did a similar [registry configuration feature](https://github.com/containers/podman/blob/c70f5fb19bb411f81183d025d18bbf1e8cdc0938/pkg/registries/registries.go#L19)
- _add your topics_

### Notes:
- Steve talked us through some of the thoughts on the artifact manifest:
    - https://github.com/SteveLasker/artifacts/blob/artifact-manifest/artifact-manifest/artifact-manifest.md
    - https://stevelasker.blog/2020/10/21/is-it-time-to-change-default-registry-references/
        - RH experience: allowing short ambiguous names is deeply problematic. It may make sense for an UI (per-user aliases on manually-typed input), but should never be in data like Helm charts / k8s pod specs. Consider what happens if two different vendors deliver Helm charts that require different short-name configurations: you end up with search paths and conflicts and attacks via registry DoS to redirect references. Instead, have names that are worldwide-unique, and map them to physical locations.
  - Multiple concerns with dropping the registry server in references, including ambiguous references to `name.with.dots/path:tag` where the name may be a part of the repo or a hostname, and intentional repository name conflicts to push malicious images. My preference is to use an upstream registry name, and clients can configure mirrors that attempt to pull images for a specific upstream registry from a specific mirror. (Brandon)
  - Add topic around signature revocation, in addition to key revocation
  - Will send the OCI Artifact Manifest PR out later this week for feedback
  - Recursive lookups on references (CNAB -> Helm -> Image) is probably best left to a client side implementation to avoid server-side DoS attacks. (Brandon)
  - It would be helpful for a lookup of signatures on an image to include the contents of the multiple signatures, rather than only a list of descriptors that needs to be queried separately (reducing the number of round trips to find a usable signature). (Brandon)
- SPIFFE/Spire
  - Marco - could we use this for a deferred signing solution. Not sure how this would work with keys that are continually rotating


## January 11, 2021

[Recording](https://www.youtube.com/watch?v=t8D5IAMmmjU)

### Attendees:
- Steve Lasker (Microsoft)
- Hank (quay)
- Peter Engelbert (Blood Orange)
- Josh Dolitsky (Blood Orange)
- Rio Kierkels (University of Amsterdam: Security and Network Engineering Master Student)
- Mohanad Elamin (University of Amsterdam: Security and Network Engineering Master Student)
- Marco Franssen (Philips - Research)
- _add yourself_

### Agenda Items:
- Update on prototypes
- Conflict process
- _add your topics_

### Notes:
- GPG support vs. x509?
    - GitHub issue: https://github.com/notaryproject/nv2/issues/21
- Conflict Process
  Today, the referenced conversations are captured in incomplete hackmd.io notes, or recording videos. While captured, these aren't fairly searchable.
  Now that we have a baseline of content in the git repos:
  - https://github.com/notaryproject/requirements
  - https://github.com/notaryproject/requirements/blob/main/scenarios.md
  
  We committed in the meeting today to capture the specific items as PRs and issues.  
  The git history will be better for search and resolution.
## January 4, 2021

[Recording](https://www.youtube.com/watch?v=4xvko9Zjtb8)

### Attendees:
- Steve Lasker (Microsoft)
- Niaz Khan (AWS)
- Justin Cormack (Docker)
- Brandon Mitchell (self)
- Marco Franssen (Philips - Research)
- Marina Moore (NYU)
- Santiago Torres-Arias (Purdue)
- Trishank Karthik Kuppusamy (Datadog)
- Garry Ing (VMware)
- _add yourself_

### Agenda Items:
- Open discussion pertaining to the SolarWinds exploit and how Notary v2 would pertain and what we could/should add to our scope.
  Based on the publicly disclosed info, the build system appears to have been exploited. Source code was not exploited, but we all know the extent of what is capable in a build environment.
    - Were packages exploited?
    - Were additional packages injected?
    - Was the build environment locked down to not allow external sources/packages to be pulled in?
    - Where do the scripts that replicate the builds originate from?
    - What verification systems were in place to validate what went in is what came out?
    - _add your topics_

### Notes:
Open discussion on the SolarWinds attack, and what could have been done to mitigate, based on what we know about the attack and what we know about build systems.

- Trishank Kuppusamy
    The Trusting Trust attack, exactly, Steve
    From santiago torres to Everyone:  09:54 AM
    to add: xcodeghost was an attack like that. A compiler that injected malware in popular iOS apps (one was angry birds iirc)
- Ian McMillan
    Totally agree with what Marina is saying here. At the very least, supporting TUF and in-toto and/or SBOM would increase the cost to compromise and reduce the cost/velocity of post-compromise investigations. 
- santiago torres
    Agreed! I also wanted to add taht there are other exciting solutions: using keylime (TPM+Kernel IMA) and embedd this information inside of in-toto attestations to verify the integrity of buildservers
- Marco Franssen
    Joined a bit late, but hearing the last 40 minutes I think the key point is to find a way to make it easier for others to understand these topics. Personally I also struggle to convince people that we need more then just a PKI solution to do signatures. We need simple tools to integrate in the process, preferably hard to bypass, but still easy for developers to integrate. Personally I really liked notary v1 after we added a small tool to manage the certificates. Notary v2, in-toto can pull this further. Make it easier for developers, make it easier to understand for management to make them understand a relative low investment can save huge amounts of costs. etc. etc.
- Trishank Kuppusamy
    100% @Marco
- Marco Franssen
    Shouldn’t we pull this even further then just OCI registries. Many things before we reach a Docker build phase would benefit from notary as well. Supporting other registry types, npm, gradle, nuget, go modules etc. Would add a lot of value, probably even more if adding in-toto in the mix to verify images came from those registries.

Info about the SolarWinds attack:
- https://www.sec.gov/Archives/edgar/data/0001739942/000162828020017451/swi-20201214.htm
- https://labs.sentinelone.com/solarwinds-understanding-detecting-the-supernova-webshell-trojan/
- https://www.fireeye.com/blog/threat-research/2020/12/evasive-attacker-leverages-solarwinds-supply-chain-compromises-with-sunburst-backdoor.html
- https://www.microsoft.com/security/blog/2020/12/18/analyzing-solorigate-the-compromised-dll-file-that-started-a-sophisticated-cyberattack-and-how-microsoft-defender-helps-protect/
- https://blog.reversinglabs.com/blog/sunburst-the-next-level-of-stealth
