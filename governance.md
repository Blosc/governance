# Main Governance Document


The Project
===========

[Blosc](https://github.com/Blosc/c-blosc) is a high performance compression library written in C that uses this technique to make compression operations easier, faster, and more flexible.  Blosc splits the datasets into blocks, then transparently packs them into compressed containers.  Blosc extends standard compression by allowing the user to condition the data in every block with filters prior to the compression operation; these filters can be selected depending on the properties of the dataset to be compressed. In addition, Blosc provides a diversity of codecs to cover different needs (better compression, faster speed or a balance between the two).  Finally, Blosc runs its operations in parallel to leverage the high number of cores in modern CPUs.

[This study](http://blosc.org/posts/breaking-memory-walls/) demonstrates how Blosc performs using the features described above.  Using Blosc, a reduction operation (aggregation) of real data (precipitation data) operating on the compressed datasets performs almost as well as operations on the uncompressed datasets -- and, in some configurations, performance is even improved -- while achieving a typical compression ratio between 4x and 6x, depending on the filters and codecs used.  In this sample case, the same machine (or cluster of machines) can handle Blosc-managed datasets 4 times or 6 times larger than the original uncompressed datasets with no loss in performance.

Blosc is currently used in many projects, among them [PyTables](https://www.pytables.org), [python-blosc](https://github.com/Blosc/python-blosc), [JBlosc](https://github.com/Blosc/JBlosc), [bcolz](https://bcolz.readthedocs.io), and [zarr](https://zarr.readthedocs.io) (via its [numcodecs](https://numcodecs.readthedocs.io) subproject).  It is widely appreciated for its fast performance and stability.

The [C-Blosc](https://github.com/Blosc/c-blosc) project is the C library that is the foundation around which the rest of the projects listed above are based.  Although started and maintained by Francesc Alted through the years, this project is developed by a team of distributed developers, called Contributors. Contributors are individuals who have contributed code, documentation, designs or other work to one or more Project repositories. Anyone can be a Contributor. Contributors can be affiliated with any legal entity or none. Contributors participate in the project by submitting, reviewing and discussing GitHub Pull Requests and Issues and participating in open and public Project discussions on GitHub and mailing lists. The foundation of Project participation is openness and transparency.

Here is a list of the current Contributors to the main C-Blosc repository (almost 40 at this time):

https://github.com/Blosc/c-blosc/graphs/contributors

There are also many other Contributors listed in the logs of other repositories behind the [Blosc umbrella](https://github.com/Blosc).

The Project Community consists of all Contributors and Users of the Project. Contributors work on behalf of and are responsible to the larger Project Community and we strive to keep the barrier between Contributors and Users as low as possible.

It is important to stress out that, besides the maintenance of the Blosc version 1.x series (aka Blosc1) most of the development in the project now is happening in the next generation of Blosc, aka Blosc2, and specifically in the [C-Blosc2](https://github.com/Blosc/c-blosc2) project.  Among the improvements on the [C-Blosc2 development roadmap](https://github.com/Blosc/c-blosc2/blob/master/ROADMAP.md) are support of full 64-bit containers, support for more filters and larger filter pipelines, additional memory layouts for the containers, support for Blosc dataset persistence, and support for more architectures.  All of these improvements should conform to the current Blosc1 API and be backward-compatible with Blosc1 containers.

Another important path of development under the Blosc project umbrella is happening at [Caterva](https://github.com/Blosc/Caterva), a C library for handling multi-dimensional, compressed datasets on top C-Blosc2 and its sister companion, the [cat4py](https://github.com/Blosc/cat4py) Python wrapper.  The work to be done is listed on the [Caterva roadmap](https://github.com/Blosc/Caterva/blob/master/ROADMAP.md).

The Project is formally affiliated with the 501c3 NumFOCUS Foundation (https://numfocus.org), which serves as its fiscal sponsor, may hold project trademarks and other intellectual property, helps manage project donations and acts as a parent legal entity. NumFOCUS is the only legal entity that has a formal relationship with the project.

Governance
==========

This section describes the governance and leadership model of The Project.

The foundations of Project governance are:

* Openness & Transparency
* Active Contribution
* Institutional Neutrality

Traditionally, Project leadership was provided by a BDFL (Francesc Alted) and subset of Contributors, called Core Developers, whose active and consistent contributions have been recognized by their receiving “commit rights” to the Project GitHub repositories. In general all Project decisions are made through consensus among the Core Developers with input from the Community. The BDFL can, but rarely chooses to, override the Core Developers and make a final decision on a matter.

While this approach has served us well, as the Project grows and faces more legal and financial decisions and interacts with other institutions, we see a need for a more formal governance model. Moving forward The Project leadership will consist of a BDFL and Steering Council. We view this governance model as the formalization of what we are already doing, rather than a change in direction.

BDFL
----

The Project will have a BDFL (Benevolent Dictator for Life), who is currently Francesc Alted. As Dictator, the BDFL has the authority to make all final decisions for The Project. As Benevolent, the BDFL, in practice chooses to defer that authority to the consensus of the community discussion channels and the Steering Council (see below). It is expected, and in the past has been the case, that the BDFL will only rarely assert his/her final authority. Because rarely used, we refer to BDFL’s final authority as a “special” or “overriding” vote. When it does occur, the BDFL override typically happens in situations where there is a deadlock in the Steering Council or if the Steering Council asks the BDFL to make a decision on a specific matter. To ensure the benevolence of the BDFL, The Project encourages others to fork the project if they disagree with the overall direction the BDFL is taking. The BDFL is chair of the Steering Council (see below) and may delegate his/her authority on a particular decision or set of decisions to any other Council member at his/her discretion.

The BDFL can appointing his/her successor, but it is expected that the Steering Council would be consulted on this decision. If the BDFL is unable to appoint a successor, the Steering Council will make a suggestion or suggestions to the Main NumFOCUS Board. While the Steering Council and Main NumFOCUS Board will work together closely on the BDFL selection process, the Main NUMFOCUS Board will make the final decision.

Steering Council
================

The Project will have a Steering Council that consists of Project Contributors who have produced contributions that are substantial in quality and quantity, and sustained over at least one year. The overall role of the Council is to ensure, through working with the BDFL and taking input from the Community, the long-term well-being of the project, both technically and as a community.

During the everyday project activities, council members participate in all discussions, code review and other project activities as peers with all other Contributors and the Community. In these everyday activities, Council Members do not have any special power or privilege through their membership on the Council. However, it is expected that because of the quality and quantity of their contributions and their expert knowledge of the Project Software and Services that Council Members will provide useful guidance, both technical and in terms of project direction, to potentially less experienced contributors.

The Steering Council and its Members play a special role in certain situations. In particular, the Council may:

* Make decisions about the overall scope, vision and direction of the project.
* Make decisions about strategic collaborations with other organizations or individuals.
* Make decisions about specific technical issues, features, bugs and pull requests. They are the primary mechanism of guiding the code review process and merging pull requests.
* Make decisions about the Services that are run by The Project and manage those Services for the benefit of the Project and Community.
* Make decisions when regular community discussion doesn’t produce consensus on an issue in a reasonable time frame.

Council membership
------------------

The Council will be initially formed from those who, as of mid 2018, have either been significantly active over the last two years, have promoted the use of Blosc inside other libraries that are actively used in the PyData Community, or are willing to put their experience (mainly in the field of data science) at the service of the project.

To become eligible for being a Steering Council Member an individual must be a Project Contributor who has produced contributions that are substantial in quality and quantity, and sustained over at least one year. Potential Council Members are nominated by existing Council members and voted upon by the existing Council after asking if the potential Member is interested and willing to serve in that capacity.

When considering potential Members, the Council will look at candidates with a comprehensive view of their contributions. This will include but is not limited to code, code review, infrastructure work, mailing list and chat participation, community help/building, education and outreach, design work, etc. We are deliberately not setting arbitrary quantitative metrics (like “100 commits in this repo”) to avoid encouraging behavior that plays to the metrics rather than the project’s overall well-being. We want to encourage a diverse array of backgrounds, viewpoints and talents in our team, which is why we explicitly do not define code as the sole metric on which council membership will be evaluated.

If a Council member becomes inactive in the project for a period of one year, they will be considered for removal from the Council. Before removal, inactive Member will be approached by the BDFL to see if they plan on returning to active participation. If not they will be removed immediately upon a Council vote. If they plan on returning to active participation soon, they will be given a grace period of one year. If they don’t return to active participation within that time period they will be removed by vote of the Council without further grace period. All former Council members can be considered for membership again at any time in the future, like any other Project Contributor. Retired Council members will be listed on the project website, acknowledging the period during which they were active in the Council.

The Council reserves the right to eject current Members, other than the BDFL, if they are deemed to be actively harmful to the project’s well-being, and attempts at communication and conflict resolution have failed.

Conflict of interest
--------------------

It is expected that the BDFL and Council Members will be employed at a wide range of companies, universities and non-profit organizations. Because of this, it is possible that Members will have conflict of interests. Such conflict of interests include, but are not limited to:

* Financial interests, such as investments, employment, or contracting work, outside of The Project that may influence their work on The Project.
* Access to proprietary information of their employer that could potentially leak into their work with the Project.
* An issue where the person privately gains an advantage from The Project resources, but The Project has no gain or suffers a disadvantage.

All members of the Council, BDFL included, shall disclose to the rest of the Council any conflict of interest they may have. Members with a conflict of interest in a particular issue may participate in Council discussions on that issue, but must recuse themselves from voting on the issue. If the BDFL has recused his/herself for a particular decision, they will appoint a substitute BDFL for that decision.

Private communications of the Council
-------------------------------------

Unless specifically required, all Council discussions and activities will be public and done in collaboration and discussion with the Project Contributors and Community. The Council will have a private mailing list that will be used sparingly and only when a specific matter requires privacy. When private communications and decisions are needed, the Council will do its best to summarize those to the Community after eliding personal/private/sensitive information that should not be posted to the public internet.

Changing the Governance Documents
=================================

Changes to the governance documents are submitted via a GitHub pull request to The Project's governance documents GitHub repository at https://github.com/Blosc/governance. The pull request is then refined in response to public comment and review, with the goal being consensus in the community. After this open period, a Steering Council Member proposes to the Steering Council that the changes be ratified and the pull request merged (accepting the proposed changes) or proposes that the pull request be closed without merging (rejecting the proposed changes). The Member should state the final commit hash in the pull request being proposed for acceptance or rejection and briefly summarize the pull request. A minimum of 80% of the Steering Council must vote and at least 2/3 of the votes must be positive to carry out the proposed action (fractions of a vote rounded up to the nearest integer). Since the BDFL holds ultimate authority in The Project, the BDFL has authority to act alone in accepting or rejecting changes or overriding Steering Council decisions.
