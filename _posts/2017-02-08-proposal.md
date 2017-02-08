---
layout: post
title: A Shared Task for a Shared Goal - Systematic Annotation of Literary Texts
author:
- Nils Reiter
- Evelyn Gius
- Jannik Strötgen
- Marcus Willand
---

# Preface

*This text has been **submitted** for the next Digital Humanities Conference, to be presented as a talk in Montreal 2017.*

# Introduction
In this talk, we would like to outline a proposal for a *shared task* (ST) in and for the digital humanities. In general, shared tasks are highly productive frameworks for bringing together different researchers/research groups and, if done in a sensible way, foster interdisciplinary collaboration. They have a tradition in natural language processing (NLP) where organizers define research tasks and settings. In order to cope for the specialties of DH research, we propose a ST that works in two phases, with two distinct target audiences and possible participants.

Generally, this setup allows both “sides” of the DH community to bring in what they can do best: Humanities scholars focus on conceptual issues, their description and definition. Computer science researchers focus on technical issues and work towards automatisation (cf. Kuhn & Reiter, 2015).

In Phase 1, participants with a strong understanding of a specific literary phenomenon (literary studies scholars) work on the creation of annotation guidelines. This allows them to bring in their expertise without worrying about feasibility of automatisation endeavours or struggling with technical issues. We will compare the different annotation guidelines both *qualitatively*, by having an in-depth discussion during a workshop, and *quantitatively*, by measuring inter-annotator agreement, resulting in a community guided selection of annotation guidelines for a set of phenomena. The involvement of the research community in this process guarantees that heterogenous points of view are taken into account.

The guidelines will then enter Phase 2 to actually make annotations on a semi-large scale. These annotations then enter a “classical” shared task as it is established in the NLP community: Various teams competitively contribute systems, whose performances will be evaluated in a quantitative manner.

Given the complexity of many phenomena in literature, we expect the automatisation of such annotations to be an interesting challenge from an engineering perspective. On the other hand, it is an excellent opportunity to initiate the development of tools tailored to the detection of specific phenomena that are relevant for computational literary studies.

This talk has two purposes:
- To discuss these ideas and collect feedback and propositions. This is also an explicit invitation to contribute in the setup of this initiative. We are also welcoming a discussion about the phenomena that should be included.
- To advertise the idea of a shared task and to invite possible participants. The success of STs relies on a certain number of participants. Given that this has never been organized in den DH community before, we want to spread this idea into the community to gather estimates of potential participants.

# The Importance of Annotations

In computational literary studies, many phenomena cannot directly be detected from the text surface. To find and categorize such phenomena as, e.g., the "narrated time" in a novel, deep text understanding, knowledge about author or literary conventions, or historical  context knowledge are required. Therefore, instances of such phenomena need to be annotated either by human experts or software that is tailored to this task.

Unfortunately, many theories describing interesting phenomena are very difficult to apply to real texts. It has been shown numerous times (e.g., Reiter, 2015, Musi et al., 2016) that annotating theories or concepts directly can lead to very poor *inter-annotator agreement* (IAA): Different annotators interpret not only the text differently, but also descriptions of the theoretical concepts. While subjective annotations have their merit, studying annotations on large scale depends on their consistency, i.e., a high IAA. In addition, many theories are underspecified and examples for illustrations only. Creators of annotation guidelines often have to interpret what is meant by a certain statement and extend definitions to cover examples found in real texts.

Annotation guidelines serve as a mediator between a theory (that uses specialised vocabulary) and the annotators. Those guidelines often also contain re-appearing instance patterns and how they are to be annotated, or exceptions and typically a lot of examples from real texts (see below).

We see the **creation of annotation guidelines** as one of the cornerstones of large scale text analysis in computational literary studies. Additionally, it supports systematically disciplinary discussions about concepts and thus may lead to additional findings relevant for the theoretical discourse (e.g., Meister, 1995; Gius and Jacke, submitted). Experts from literary studies are predestined for working on annotation guidelines, as annotation of literary phenomena in literary texts can be seen as a special form of close reading.

# Phase One: Annotation Guidelines
## The Shared Task
We propose two phenomena to describe with guidelines, both from the area of narratology (Genette, 1980; Bal, 1997): Duration and focalisation. Participating teams are asked to create guidelines for one or both. In this first phase of the workshop, the participants are not bound to adhere to a specific narratological theory. The result of this phase, however, will be a fixation on a set of guidelines (that instantiate a theory). The phenomena are:

**Duration** (cf. Scheffel et al., 2016) concerns the speed of a narration, determined by the relation between the narrated time (duration of happenings) to the narrating time (duration of the textual representation of happenings). Narrated time and narrating time can correspond or diverge, resulting in fast or slow narration. For example, in Virginia Woolf’s novel To the Lighthouse, the first and the last sections narrate one day and thus are narrated slowly, whereas the second section is narrated faster—it encompasses ten years in only about 20 pages. Explicit expressions of duration ("three weeks") have been addressed in the TempEval shared tasks (Verhagen et al. 2010, UzZaman et al. 2013). These expressions cover only a subset of narrative duration phenomena, and systems have been tailored to news texts (cf. Strötgen and Gertz, 2016).

The concept of **focalisation** (cf. Niederhoff, 2016) describes the relation between the information represented in the narrative and the experience and knowledge of an instance of the narrative, normally a character. Genette (1980) distinguishes three focalisation types:

- Zero focalisation: The narrator knows or says more than any character knows (N>C)
- Internal focalisation: (N=C)
- External focalisation (N<C).

Duration and focalisation represent exemplary cases of  the lower and upper bound in terms of conceptual complexity. Even though focalisation seems to be defined as clearly as duration, it is much harder to identify and determine types of focalisation.

Nevertheless, the automatic identification of both phenomena promises a great deal of new knowledge in literary history and historical narratology.

We will select a number of literary genres and/or eras as development material and provide copyright-free digitized corpora. All “official” texts (development and test sets) will be English literary texts.

## Evaluation
In NLP shared tasks, the predictions of the systems are compared against a fixed test set, the gold standard. Since there is no gold standard in Phase 1, we will evaluate the guidelines using an unseen data set. Each participating team annotates this set using their own guidelines, before submitting them. Submitted guidelines will be anonymized and re-distributed among the participants. Each participant is asked to annotate the evaluation data set using two other annotation guidelines. In addition, we will be collecting annotations from students.

The evaluation data set will thus be annotated according to each participant’s guidelines four times (1 x self, 1 x student,  2 x other participants).

This setup allows direct calculation of *inter-annotator agreement*. However, IAA should be only one aspect in evaluating the guidelines, but not the only one. Therefore, we will submit a workshop at DH 2018 to discuss the submissions and select final ones. This setup also allows merging different annotation guidelines as well as adaptations according to the discussion during the workshop. Soon after the workshop, Phase 2 will commence.

# Phase Two: Automatic Prediction
In Phase 2 of this endeavour, the selected guidelines of Phase 1 will be annotated on a large scale by student assistants. Since we currently do not know how long, complex and involved the guidelines will be, there should be a close communication between the organizers and the team responsible for the selected guidelines.

As soon as texts have been annotated, they will be made accessible to participants. For the deadline in Phase 2, participants will be asked to process a new data set -- one that has not been released before -- and return the predicted annotations to the organizers, who will then make evaluations using standard measures (e.g., accuracy). Finally, there will be a workshop in which each participating team presents its system. This workshop is projected to be coordinated with the LaTeCH workshop series, which has taken place at ACL conferences in the past years (one of the authors of this paper has been workshop organiser in the past years).

# Technical Details and Timeline
This proposal is innovative in a number of ways: Shared tasks are a new kind of framework in the DH/H community, duration and focalisation have not been investigated in this way before and last but not least, a shared task with the goal of creating annotation guidelines has not been organized before (to our knowledge). We believe it is more important to do this right than to do this fast and that is why we are looking at a rather lengthy timeline.

| Date | Event |
| -----:| ----- |
| August 2017 | Announcement talks at DH and LaTeCH-CLfL 2017 |
| November 2017 | Finalisation of Phase 1 details, submission for DH 2018, Call for participation (Phase 1) |
| April 2018 | Submission deadline for guidelines |
| June 2018 | Phase 1 workshop (DH) |
| August 2018 | Announcement talk for Phase 2 (LaTeCH 2018) |
| October 2018 | Finalisation of Phase 2 details, submission for ACL 2019, Call for participation (Phase 2) |
| May 2019 | Submission deadline for systems for Phase 2 |
| August 2019 | Phase 2 workshop (ACL/LaTeCH) |
