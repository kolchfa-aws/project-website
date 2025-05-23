---
layout: fullwidth-with-breadcrumbs
primary_title: Release Schedule and Maintenance Policy
title: Release Schedule and Maintenance Policy
breadcrumbs:
  icon: platform
  items:
    - title: About
      url: '/about.html'
    - title: Releases
      url: '/releases.html'
include_mobile_tables: true
---

- [Release Schedule](#release-schedule)
- [Maintenance Policy](#maintenance-policy)
- [Release History](#release-history)
- [Change Log](#change-log)

## Release Schedule ##

For more information on the changes planned for each release, please see the [Project Roadmap](https://github.com/orgs/opensearch-project/projects/206)

See below for criteria for a major releases.


| Release Number | First RC Generated (release window opens) | Latest Possible Release Date (release window closes) | Release Manager                                   | Tracking Issue                                                             |
|:---------------|:------------------------------------------|:-----------------------------------------------------|:--------------------------------------------------|:---------------------------------------------------------------------------|
| 2.19.0         | January 28th, 2025                        | February 11th, 2025                                  | [Rishabh Singh](https://github.com/rishabh6788)   | [5152](https://github.com/opensearch-project/opensearch-build/issues/5152) | 
| 2.19.1         | February 20th, 2025                       | February 27th, 2025                                  | [Divya Madala](https://github.com/Divyaasm/)      | [5323](https://github.com/opensearch-project/opensearch-build/issues/5323) | 
| 3.0.0-alpha1   | March 04th, 2025                          | March 18th, 2025                                     | [Peter Zhu](https://github.com/peterzhuamazon)    | [3747](https://github.com/opensearch-project/opensearch-build/issues/3747) | 
| 3.0.0-beta1    | April 08th, 2025                          | April 22nd, 2025                                     | [Peter Zhu](https://github.com/peterzhuamazon)    | [3747](https://github.com/opensearch-project/opensearch-build/issues/3747) | 
| 2.19.2         | April 22nd, 2025                          | April 29th, 2025                                     | [Zelin Hao](https://github.com/zelinh)            | [5419](https://github.com/opensearch-project/opensearch-build/issues/5419) | 
| 3.0.0 (GA)     | April 29th, 2025                          | May 06th, 2025                                       | [Peter Zhu](https://github.com/peterzhuamazon)    | [3747](https://github.com/opensearch-project/opensearch-build/issues/3747) | 
| 3.1.0          | June 10th, 2025                           | June 24th, 2025                                      |                                                   |                                                                            | 
| 2.19.3         | July 15th, 2025                           | July 22th, 2025                                      |                                                   |                                                                            | 
| 3.2.0          | August 05th, 2025                         | August 19th, 2025                                    |                                                   |                                                                            | 
| 3.3.0          | September 30th, 2025                      | October 14th, 2025                                   |                                                   |                                                                            | 
| 2.19.4         | October 28th, 2025                        | November 04th, 2025                                  |                                                   |                                                                            | 
| 3.4.0          | December 02nd, 2025                       | December 16th, 2025                                  |                                                   |                                                                            | 
| 3.5.0          | January 27th, 2026                        | February 10th, 2026                                  |                                                   |                                                                            | 
{: .desktop-release-schedule-table}

OpenSearch [follows semver](https://opensearch.org/blog/technical-post/2021/08/what-is-semver/), which means we will only release breaking changes in major versions.  All minor versions are compatible with every other minor version for that major.  For example, 1.2.0 will work with 1.3.2, 1.4.1, etc, but may not work with 2.0.

For minor version releases, OpenSearch follows "release window" model as described in our [releasing documentation](https://github.com/opensearch-project/.github/blob/main/RELEASING.md). The goal is to release a new minor version approximately every eight weeks which includes all the new features and fixes that are ready to go. Once we enter a release window, every day we will generate a release candidate. When the exit criteria are met by a release candidate, we will make an announcement, update the release date column above and publish new artifacts on that date.

**Note:** If we cannot pass the exit criteria by 2 weeks after the start of the release cycle window (1 week for 1.x patch releases), we will cancel the minor release and hold changes until the next release window.

In contrast, OpenSearch releases new major versions only when there are a critical mass of breaking changes (e.g. changes that are incompatible with existing APIs).  These tend to be tied to [Lucene](https://lucene.apache.org/) major version releases, and will be announced in the forums at least 4 weeks prior to the release date.

Both the roadmap and the release dates reflect intentions rather than firm commitments and may change as we learn more or encounters unexpected issues. If dates do need to change, we will be as transparent as possible, and log all changes in the changelog at the bottom of this page.

## Maintenance Policy ##

For OpenSearch and other software in the OpenSearch project, new features and active development always takes place against the newest version. The OpenSearch project follows the semantic versioning specification for assigning version numbers to releases, so you should be able to upgrade to the latest minor version of that same major version of the software without encountering incompatible changes (e.g., 1.1.0 → 1.3.x).

Sometimes an incompatible change is unavoidable. When this happens, the software’s maintainers will increment the major version number (e.g., increment from OpenSearch 1.3.z to OpenSearch 2.0.0). The last minor version of the previous major version of the software will then enter a _maintenance window_ (e.g., 1.3.x). During the maintenance window, the software will continue to receive bug fixes and security patches, but no new features.

We follow [OpenSSF's best practices for patching publicly known vulnerabilities](https://bestpractices.coreinfrastructure.org/en/criteria/0?details=true&rationale=true#0.vulnerabilities_fixed_60_days) and we make sure that there are no unpatched vulnerabilities of medium or higher severity that have been publicly known for more than 60 days in our actively maintained versions.

The duration of the maintenance window will vary from product to product and release to release. **By default, versions will remain under maintenance until the next major version enters maintenance, or 1 year passes, whichever is longer.** Therefore, at any given time, the current major version and previous major version will both be supported, as well as older major versions that have been in maintenance for less than 12 months. Please note that, maintenance windows are influenced by the support schedules for dependencies the software includes, community input, the scope of the changes introduced by the new version, and estimates for the effort required to continue maintenance of the previous version.

The software maintainers will not back-port fixes or features to versions outside of the maintenance window. That said, PRs with said back-ports are welcome and will follow the project’s [review process](https://github.com/opensearch-project/OpenSearch/blob/main/CONTRIBUTING.md#review-process). No new releases will result from these changes, but interested parties can [create their own distribution](https://github.com/opensearch-project/opensearch-build#building-and-testing-an-opensearch-distribution) from the updated source after the PRs are merged.


| Major Version | Latest Minor Version |   Status    | Initial GA Release   | Maintenance Window Start   | Maintenance Window End |
|:--------------|:---------------------|:------------|:---------------------|:---------------------------|:-----------------------|
| 1             | 1.3.20               | Maintenance |  July 12th, 2021     | May 26th, 2022             | April 29th, 2025       |
| 2             | 2.19.0               | Current     |  May 26th, 2022      | April 29th, 2025           | GA release of 4.0.     |
| 3             | 3.0.0-beta1          | In-flight   |  April 29th, 2025    | N/A                        | N/A                    |
{: .desktop-maintenance-policy-table}

*Note that the length of the maintenance window is an estimated minimum and the project may, at its discretion, extend it _to a later_ date

## Release History ##


| Release Number | Release Date         | Release Manager                                                                                                                                 | Tracking Issue |
|:---------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------|
| 3.0.0-alpha1   | March 18th, 2025     | [Peter Zhu](https://github.com/peterzhuamazon) & [Zelin Hao](https://github.com/zelinh/)                                                       | [3747](https://github.com/opensearch-project/opensearch-build/issues/3747) | 
| 2.19.1         | February 20th, 2025  | [Divya Madala](https://github.com/Divyaasm/) & [Peter Zhu](https://github.com/peterzhuamazon)                                                   | [5323](https://github.com/opensearch-project/opensearch-build/issues/5323) | 
| 2.19.0         | February 11th, 2025  | [Rishabh Singh](https://github.com/rishabh6788/), [Divya Madala](https://github.com/Divyaasm/) & [Peter Zhu](https://github.com/peterzhuamazon) | [5152](https://github.com/opensearch-project/opensearch-build/issues/5152) |
| 1.3.20         | December 11th, 2024  | [Brandon Shien](https://github.com/bshien), [Zelin Hao](https://github.com/zelinh/) & [Peter Zhu](https://github.com/peterzhuamazon)            | [4990](https://github.com/opensearch-project/opensearch-build/issues/4990) |
| 2.18.0         | November 05th, 2024  | [Rishabh Singh](https://github.com/rishabh6788/)                                                                                                | [5004](https://github.com/opensearch-project/opensearch-build/issues/5004) |
| 2.17.1         | October 01st, 2024   | [Divya Madala](https://github.com/Divyaasm/) & [Peter Zhu](https://github.com/peterzhuamazon)                                                   | [5046](https://github.com/opensearch-project/opensearch-build/issues/5046) |
| 2.17.0         | September 17th, 2024 | [Sayali Gaikawad](https://github.com/gaiksaya/)                                                                                                 | [4908](https://github.com/opensearch-project/opensearch-build/issues/4908) |
| 1.3.19         | August 27th, 2024    | [Brandon Shien](https://github.com/bshien)                                                                                                      | [4888](https://github.com/opensearch-project/opensearch-build/issues/4888) |
| 2.16.0         | August 07th 2024     | [Prudhvi Godithi](https://github.com/prudhvigodithi)                                                                                            | [4771](https://github.com/opensearch-project/opensearch-build/issues/4771) |
| 1.3.18         | July 16th, 2024      | [Zelin Hao](https://github.com/zelinh/)                                                                                                         | [4763](https://github.com/opensearch-project/opensearch-build/issues/4763) |
| 2.15.0         | June 25th, 2024      | [Peter Zhu](https://github.com/peterzhuamazon)                                                                                                  | [4681](https://github.com/opensearch-project/opensearch-build/issues/4681) |
| 1.3.17         | June 06th, 2024      | [Divya Madala](https://github.com/Divyaasm/)                                                                                                    | [4659](https://github.com/opensearch-project/opensearch-build/issues/4659) |
| 2.14.0         | May 14th, 2024       | [Rishabh Singh](https://github.com/rishabh6788/)                                                                                                | [4562](https://github.com/opensearch-project/opensearch-build/issues/4562) |
| 1.3.16         | April 23rd, 2024     | [Zelin Hao](https://github.com/zelinh/)                                                                                                         | [4531](https://github.com/opensearch-project/opensearch-build/issues/4531) |
| 2.13.0         | April 2nd, 2024      | [Sayali Gaikawad](https://github.com/gaiksaya)                                                                                                  | [4433](https://github.com/opensearch-project/opensearch-build/issues/4433) |
| 1.3.15         | March 05th 2024      | [Jeff Lu](https://github.com/jordarlu)                                                                                                          | [4294](https://github.com/opensearch-project/opensearch-build/issues/4294) |
| 2.12.0         | February 20th 2024   | [Prudhvi Godithi](https://github.com/prudhvigodithi)                                                                                            | [4115](https://github.com/opensearch-project/opensearch-build/issues/4115) |
| 1.3.14         | December 12th 2023   | [Zelin Hao](https://github.com/zelinh)                                                                                                          | [4069](https://github.com/opensearch-project/opensearch-build/issues/4069) |
| 2.11.1         | November 30th, 2023  | [Divya Madala](https://github.com/Divyaasm)                                                                                                     | [4161](https://github.com/opensearch-project/opensearch-build/issues/4161) |
| 2.11.0         | October 16th, 2023   | [Rishabh Singh](https://github.com/rishabh6788) & [Peter Zhu](https://github.com/peterzhuamazon)                                                | [3998](https://github.com/opensearch-project/opensearch-build/issues/3998) |
| 1.3.13         | September 21st       | [Zelin Hao](https://github.com/zelinh)                                                                                                          | [3878](https://github.com/opensearch-project/opensearch-build/issues/3878) |
| 2.10.0         | September 25th       | [Prudhvi Godithi](https://github.com/prudhvigodithi)                                                                                            | [3777](https://github.com/opensearch-project/opensearch-build/issues/3777) |
| 1.3.11         | June 29th, 2023      | [Jeff Lu](https://github.com/jordarlu)                                                                                                          | [3630](https://github.com/opensearch-project/opensearch-build/issues/3630) |
| 2.9.0          | July 24th, 2023      | [Prudhvi Godithi](https://github.com/prudhvigodithi)                                                                                            | [3762](https://github.com/opensearch-project/opensearch-build/issues/3762) |
| 2.8.0          | June 6th, 2023       | [Rishabh Singh](https://github.com/rishabh6788) & [Peter Zhu](https://github.com/peterzhuamazon)                                                | [3434](https://github.com/opensearch-project/opensearch-build/issues/3434) |
| 1.3.10         | May 11th, 2023       | [Prudhvi Godithi](https://github.com/prudhvigodithi) & [Peter Zhu](https://github.com/peterzhuamazon)                                           | [3331](https://github.com/opensearch-project/opensearch-build/issues/3331) |
| 2.7.0          | April 17th, 2023     | [Peter Zhu](https://github.com/peterzhuamazon) & [Zelin Hao](https://github.com/zelinh)                                                         | [3230](https://github.com/opensearch-project/opensearch-build/issues/3230) |
| 1.3.9          | March 9th, 2023      | [Jeff Lu](https://github.com/jordarlu)                                                                                                          | [3195](https://github.com/opensearch-project/opensearch-build/issues/3195) |
| 2.6.0          | February 28th, 2023  | [Sayali Gaikawad](https://github.com/gaiksaya)                                                                                                  | [3081](https://github.com/opensearch-project/opensearch-build/issues/3081) |
| 1.3.8          | February 2nd, 2023   | [Rishabh Singh](https://github.com/rishabh6788) & [Divya Madala](https://github.com/Divyaasm)                                                   | [3012](https://github.com/opensearch-project/opensearch-build/issues/3012) |
| 2.5.0          | January 24th, 2023   | [Rishabh Singh](https://github.com/rishabh6788), [Peter Zhu](https://github.com/peterzhuamazon) & [Zelin Hao](https://github.com/zelinh)        | [2908](https://github.com/opensearch-project/opensearch-build/issues/2908) |
| 1.3.7          | December 13th, 2022  | [Peter Zhu](https://github.com/peterzhuamazon) & [Rishabh Singh](https://github.com/rishabh6788)                                                | [2742](https://github.com/opensearch-project/opensearch-build/issues/2742) |
| 2.4.0          | November 15th, 2022  | [Peter Zhu](https://github.com/peterzhuamazon)                                                                                                  | [2649](https://github.com/opensearch-project/opensearch-build/issues/2649) |
| 1.3.6          | October 6th, 2022    | [Zelin Hao](https://github.com/zelinh)                                                                                                          | [2650](https://github.com/opensearch-project/opensearch-build/issues/2650) |
| 2.3.0          | September 14th, 2022 | [Sayali Gaikawad](https://github.com/gaiksaya)                                                                                                  | [2447](https://github.com/opensearch-project/opensearch-build/issues/2447) |
| 2.2.1          | September 1st, 2022  | [Prudhvi Godithi](https://github.com/prudhvigodithi)                                                                                            | [2481](https://github.com/opensearch-project/opensearch-build/issues/2481) |
| 1.3.5          | September 1st, 2022  | [Prudhvi Godithi](https://github.com/prudhvigodithi)                                                                                            | [2348](https://github.com/opensearch-project/opensearch-build/issues/2348) |
| 2.2.0          | August 11th, 2022    | [Peter Zhu](https://github.com/peterzhuamazon)                                                                                                  | [2271](https://github.com/opensearch-project/opensearch-build/issues/2271) |
| 1.3.4          | July 14th, 2022      | [Zelin Hao](https://github.com/zelinh)                                                                                                          | [2205](https://github.com/opensearch-project/opensearch-build/issues/2205) |
| 2.1.0          | July 7th, 2022       | [Sayali Gaikawad](https://github.com/gaiksaya)                                                                                                  | [1818](https://github.com/opensearch-project/opensearch-build/issues/1818) |
| 2.0.1          | June 16th, 2022      | [Zelin Hao](https://github.com/zelinh) & [Peter Zhu](https://github.com/peterzhuamazon)                                                         | [2165](https://github.com/opensearch-project/opensearch-build/issues/2165) |
| 1.3.3          | June 09th, 2022      | [Prudhvi Godithi](https://github.com/prudhvigodithi) & [Peter Zhu](https://github.com/peterzhuamazon)                                           | [2101](https://github.com/opensearch-project/opensearch-build/issues/2101) |
| 2.0.0          | May 26th, 2022       | [Peter Zhu](https://github.com/peterzhuamazon)                                                                                                  | [2086](https://github.com/opensearch-project/opensearch-build/issues/2086) |
| 1.3.2          | May 5th, 2022        | [Zelin Hao](https://github.com/zelinh)                                                                                                          | [1882](https://github.com/opensearch-project/opensearch-build/issues/1882) |
| 2.0.0-rc1      | May 3rd, 2022        | [Peter Zhu](https://github.com/peterzhuamazon) & [Zelin Hao](https://github.com/zelinh)                                                         | [1624](https://github.com/opensearch-project/opensearch-build/issues/1624) |
| 1.3.1          | March 30th, 2022     | [Abhinav Gupta](https://github.com/abhinavGupta16)                                                                                              | [1885](https://github.com/opensearch-project/opensearch-build/issues/1885) |
| 1.3.0          | March 17th, 2022     | [Zelin Hao](https://github.com/zelinh) & [Peter Zhu](https://github.com/peterzhuamazon)                                                         | [889](https://github.com/opensearch-project/opensearch-build/issues/889)   |
| 1.2.4          | January 18th, 2022   | [Abhinav Gupta](https://github.com/abhinavGupta16) & [Peter Zhu](https://github.com/peterzhuamazon)                                             | [1417](https://github.com/opensearch-project/opensearch-build/issues/1417) |
| 1.2.3          | December 22th, 2021  | [Peter Zhu](https://github.com/peterzhuamazon) & [Peter Nied](https://github.com/peternied)                                                     | [1365](https://github.com/opensearch-project/opensearch-build/issues/1365) |
| 1.2.0          | November 23th, 2021  | [Sayali Gaikawad](https://github.com/gaiksaya), [Peter Zhu](https://github.com/peterzhuamazon) & [Peter Nied](https://github.com/peternied)     | [567](https://github.com/opensearch-project/opensearch-build/issues/567)   |
| 1.1.0          | October 05th, 2021   | [Peter Zhu](https://github.com/peterzhuamazon)                                                                                                  | [564](https://github.com/opensearch-project/opensearch-build/issues/564)   |
| 1.0.1          | September 01, 2021   | [Abhinav Gupta](https://github.com/abhinavGupta16)                                                                                              | [151](https://github.com/opensearch-project/opensearch-build/issues/151)   |
| 1.0.0          | July 12th, 2021      | [Peter Zhu](https://github.com/peterzhuamazon) & [Sayali Gaikawad](https://github.com/gaiksaya)                                                 | [85](https://github.com/opensearch-project/opensearch-build/pull/85)       |
| 1.0.0-rc1      | June 7th, 2021       | [Peter Zhu](https://github.com/peterzhuamazon), [Sayali Gaikawad](https://github.com/gaiksaya) & [Sreekar Jami](https://github.com/sreekarjami) | [48](https://github.com/opensearch-project/opensearch-build/pull/48)       |
{: .data-table__half-width .desktop-release-history-table}

## Change Log ##

| Date                 | Change | Reason          |
|:---------------------|:-------|:----------------|
| April 11th, 2025 | Add release manager for 2.19.2 release | [2.19.2 release issue](https://github.com/opensearch-project/opensearch-build/issues/5419) |
| March 19th, 2025     | Update 3.0.0-beta1 and 3.0.0 GA schedule | [[PROPOSAL] Delay OpenSearch 3.0 Beta (by 2 weeks)](https://github.com/opensearch-project/.github/issues/300) |
| March 05th, 2025     | Update 2.19.1 release history | Update Page |
| February 18th, 2025  | Update 2.19.1 release date and shift following patch releases date for 2.19.x, also update the 2.19.0 release history | [2.19.1 release issue](https://github.com/opensearch-project/opensearch-build/issues/5323) |
| February 07th, 2025  | Update release schedule for year 2025 | Update Page |
| December 11th, 2024  | Update release history for 1.3.20 release | Update Page |
| November 19th, 2024  | Update release history for 2.18.0 release and updated release manager for 1.3.20  | [1.3.20 release issue](https://github.com/opensearch-project/opensearch-build/issues/4990) |
| October 25th, 2024   | Update release history for 2.17.1 release and current progress of release 2.18.0 | Update page |
| September 04th, 2024 | Update release candidate generation date for 2.17.0 | Too many last minute PRs causing CI build issues |
| September 03rd, 2024 | Update release history from 2021 to 2023 | Update page |
| August 28th, 2024    | Update release history from February to August 2024 | Update page |
| April 26th, 2024     | Update release manager for 1.3.16 release          | [1.3.16 release issue](https://github.com/opensearch-project/opensearch-build/issues/4531)       |
| February 21st, 2024  | Update release manager for 1.3.15 release          | [1.3.15 release issue](https://github.com/opensearch-project/opensearch-build/issues/4294)       |
| February 15th, 2024  | Updated 2024 release schedule                  | Per [Proposal - 186](https://github.com/opensearch-project/.github/issues/186)   |
| February 02nd, 2024  | Enhancement | Added Release Manager & Tracking issue for each release back through 2023 to add clarity for the community. Reversed release history - latest is at the top |
| January 04th, 2024   | Updated 2.12 date | Per discussion [in this issue](https://github.com/opensearch-project/opensearch-build/issues/4290) |
| September 29th, 2023 | Updated 2.11 date | Per discussion [in this issue](https://github.com/opensearch-project/opensearch-build/issues/3955) |
| September 11th, 2023 | Link to RELEASING.md  |  updated link from proposal to releasing documentation |
| September 06th, 2023 | Updated 2.10 date  |  8 hour github outage last night - moving to accomodate a few final fixes |
| September 05th, 2023 | Updated 2.10 date  |  Original release date was too close to US Labor Day Holiday |
| August 14th, 2023    | Updated release table to reflect release windows | per adoption of <https://github.com/opensearch-project/project-website/pull/1866> |
| July 20th, 2023      | Update to 2.9.0 release date  | No-Go on the release meeting call - build issues  |
| July 17th, 2023      | Update to 2.9.0 release date  | No-Go on the release meeting call - build issues  |
| April 26th, 2023     | Update to 2.7.0 release date  | Found CVE to resolve, fix issues found in regression tests  |
| January 19th, 2023   | Update to 2.5.0 release date  | Docs team due diligence, moving to accommodate  |
| January 13th, 2023   | Update to 2.5.0 release date  | Maps team found last minute issue, moving to accommodate resolution  |
| October 20th,2022    | Added Initial 2023 schedule|Current schedule was running out|
| October 20th, 2022   | Increased time between 2.5 code freeze and release | 7 days is standard, and there were only 2 days for 2.5 |
| July 01st, 2022      |        | Initial Version |
{: .desktop-change-log-table}
