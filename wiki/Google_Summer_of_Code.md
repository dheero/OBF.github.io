---
title: Google Summer of Code
---

The O|B|F is applying for the first time for the [Google Summer of
Code](http://socghop.appspot.com/) (GSoC) program as an umbrella
organization for all O|B|F-affiliated projects.

On this page we are collecting ideas, possible projects, prerequisites,
possible solution approaches, mentors, other people or channels to
contact for more information or to bounce ideas off of, etc.

News
----

-   08 Mar 2009: The project ideas page (the page you are looking at) is
    ready for adding project ideas. *--[Lapp](User:Lapp "wikilink")*

Contact
-------

Our organization administrators are [Hilmar Lapp](User:Lapp "wikilink")
([hlapp@gmx.net](mailto:hlapp%40gmx%2enet)) and Mauricio Herrera Cuadra
([mauricio@open-bio.org](mailto:mauricio%40open-bio%2eorg)).

If you are a student interested in applying for a Google Summer of Code
project with our organization, please send any questions you have,
projects you would like to propose, etc to the developer mailing list of
the pertinent O|B|F project.

How do you know which project is pertinent and the address of its
developer mailing list? The projects under the O|B|F umbrella are listed
below, with home page and developer mailing lists. Each project idea
lists the O|B|F project it is a part of; look it up in the list below
and you have the information you need. If you want to propose your own
project idea and the project to which you would contribute isn't
obvious, send email to
[open-bio-l@open-bio.org](mailto:open-bio-l%40open-bio%2eorg).

Some of us also hang out regularly on IRC, see the list of O|B|F
projects below for information on which projects have a channel and the
name of the channel. *(If you do not have an IRC client installed, you
might find the [comparison on
Wikipedia](http://en.wikipedia.org/wiki/List_of_IRC_clients), the
[Google
directory](http://directory.google.com/Top/Computers/Software/Internet/Clients/Chat/IRC/),
or the [IRC Reviews](http://www.ircreviews.org/clients/) helpful. For
Macs, [X-Chat Aqua](http://en.wikipedia.org/wiki/X-Chat) works pretty
well. If you have never used IRC, try the [IRC
Primer](http://irchelp.org/irchelp/ircprimer.html) at [IRC
Help](http://irchelp.org/), which also has links to lots of other
material.)*

For applying, please make sure you read our [documentation on
information that students should know and guidelines we expect you to
follow](#What_should_prospective_students_know.3F "wikilink") *before*
you apply. We don't have a format template for application that you need
to adhere to, but we do ask that you include specific kinds of
information. What those are is documented under "[When you
apply](#When_you_apply "wikilink")."

Ideas
-----

*Note: if there is more than one mentor for a project, the primary
mentor is in **bold font**. Biographical and other information on the
mentors is linked to in the [Mentors section](#Mentors "wikilink").*

*Students: The below are only our project **ideas**, albeit well
thought-out ones. You are welcome to propose your own project if none of
those below catches your interest, or if your idea is more exciting to
you, provided it is still a contribution to one the O|B|F member
projects (see list below). Just be aware that we can't guarantee finding
an appropriate mentor, but if we like your proposal we will try.
Regardless of what you decide to do, make sure you read and follow the
[guidelines for
students](#What_should_prospective_students_know.3F "wikilink") below.*

### Write a NEXUS parser in C&

*This is a template for how the student project ideas could be
presented. Feel free to copy & paste & edit, and feel free to adjust the
format.*

Rationale : C& is an amp'ed-up programming language that has not been invented yet but in a few years will dominate the programming world. The best way to prevent broken non-compliant NEXUS parsers written in C& from appearing is to write a good one now.  
Approach : Re-implementations of NEXUS parsers inevitably tend to be broken or non-compliant. Hence, the best approach is to write a translator that translates a reference implementation to C&.  
Challenges : C& has not been invented yet, so a lot of assumptions will have to be made.  
Involved toolkits or projects : The [BioC&](http://www.biocamp.org) toolkit has much of the needed framework.  
Degree of difficulty and needed skills : Hard. The hardest part is probably inventing C&. Writing the parser itself should be medium, unless C& was ill-designed for writing parsers. Knowledge of the BioC& toolkit will obviously help, as well as knowing the NEXUS format.  
Mentors : Mike&, founder of BioC&  

Mentors
-------

-   Brad Chapman (MGH; Biopython)
-   [Mauricio Herrera Cuadra](bp:User:Mauricio "wikilink") (UNAM &
    Yahoo; backup org admin)
-   [Chris Fields](bp:User:Cjfields "wikilink") (U. Illinois,
    Chicago; BioPerl)
-   Mark Jensen (Fortinbras; BioPerl)
-   [Roger Hall](bp:User:Rogerhall "wikilink") (U. of Arkansas; BioPerl)
-   [Hilmar Lapp](User:Lapp "wikilink") (NESCent; org admin)
-   [Pjotr Prins](http://thebird.nl/pjwiki/wiki.pl) (BioLib)
-   Joshua Udall (BioPerl)
-   Jonathan Warren (Sanger Institute, UK; Biojava)
-   Scooter Willis (Scripps Florida; Biojava)

What should prospective students know?
--------------------------------------

### Before you apply

-   If you want to apply with your own idea, determine which O|B|F
    project you would be contributing to, and [contact
    us](#Contact "wikilink") early on so we can try to find a mentor.
-   Our scope for proposals that we will entertain is those extend one
    of affiliated toolkits. Project proposals that would create a new
    stand-alone piece of code are outside of our scope.
-   We are most interested in students who give us evidence that they
    have already or might develop a sustained interest in becoming
    future contributors to one (or more) of our projects.
-   [Ask us questions](#Contact "wikilink") about the project idea you
    have in mind.
-   Write a project proposal draft, include a project plan (see below),
    and [bounce those off of us](#Contact "wikilink").

Have I mentioned yet that you should [be in touch with
us](#Contact "wikilink") *before* you apply? The value of frequent and
early communication in contributing to a distributed and collaboratively
developed project can hardly be overemphasized. The same is true for
becoming part of a community, even if only temporarily.

### When you apply

When applying, (aside from the information requested by Google) please
provide the following in your application material.

1.  Why you are interested in the project you are proposing, uniquely
    suited to undertake it, and what do you anticipate to gain from it.
2.  Why are you interested in contributing to the O|B|F project that
    your work would be (or become) a part of? To what extent and in
    which ways do you anticipate to stay involved with the project?
3.  A summary of your programming experience and skills.
4.  Programs or projects you have previously authored or contributed to,
    in particular those available as open-source, including, if
    applicable, any past Summer of Code involvement.
5.  A project plan for the project you are proposing, even if your
    proposed project is directly based on one of the ideas above.
    -   A project plan in principle divides up the whole project into a
        series of manageable milestones and timelines that, when all
        accomplished, logically lead to the end goal(s) of the project.
        Put in another way, a project plan explains what you expect you
        will need to be doing, and what you expect you need to have
        accomplished, at which time, so that at the end you reach the
        goals of the project.
    -   Do not take this part lightly. A compelling plan takes a
        significant amount of work. Empirically, applications with no or
        a hastily composed project plan have not been competitive, and a
        more thorough project plan can easily make an applicant
        outcompete another with more advanced skills.
    -   A good plan will require you to thoroughly think about the
        project itself and how one might want to go about the work.
    -   We don't expect you to have all the experience, background, and
        knowledge to come up with the final, real work plan on your own
        at the time you apply. We do expect your plan to demonstrate,
        however, that you have made the effort and thoroughly dissected
        the goals into tasks and successive accomplishments that
        make sense.
    -   We strongly recommend that you bounce your proposed project and
        your project plan draft off of us, using either the pertinent
        developers mailing list or the IRC channel(s). Through the
        project plan exercise you will inevitably discover that you are
        missing a lot of the pieces - we are there to help you fill
        those in as best as we can.

6.  Your possibly conflicting obligations or plans for the summer during
    the coding period.
    -   Although there are no hard and fast rules about how much you can
        do in parallel to your Summer of Code project, we do expect the
        project to be your primary focus of attention over the summer.
        If you look at your Summer of Code project as a part-time
        occupation, please don't apply to us.
    -   That notwithstanding, if you have the time-management skills to
        manage other work obligations concurrent with your Summer of
        Code project, feel encouraged to make your case and support it
        with evidence.
    -   Most important of all, be upfront. If it turns out later that
        you weren't clear about other obligations, at best (i.e., if
        your accomplishment record at that point is spotless) it
        destroys our trust. Also, if you are accepted, don't take on
        additional obligations before discussing those with your mentor.
    -   One of the most common reasons for students to struggle or fail
        is being overstretched. Don't set yourself up for that - at best
        it would greatly diminish the amount of fun you'll have with
        your Summer of Code project.

### Other information

-   Our \[ 2009 application document\] with Google's questions and our
    answers
-   For questions of eligibility, see the [GSoC eligibility requirements
    for
    students](http://code.google.com/opensource/gsoc/2009/faqs.html#0_1_eligibility_83343977761348_13148542340972003).
    These requirements must be met on April 20, 2009.
-   There is also a [Google group for posting GSoC
    questions](http://groups.google.com/group/google-summer-of-code-discuss)
    (and receiving answers; note that you will need to sign up for
    the group) that relate to the program itself (and are not specific
    to our organization).
-   Students receive a stipend from Google if accepted. See the [Google
    SoC FAQ on
    payments](http://code.google.com/opensource/gsoc/2009/faqs.html#0_1_administrivia_842873138659_49145328697313184)
    for full documentation.

Reference Facts & Links
-----------------------

### Open-Bio projects involved

[BioPerl](bp:Main_Page "wikilink") :  

:\* [Information for new developers](bp:Becoming_a_developer "wikilink")

:\* [Mailing lists](bp:Mailing_lists "wikilink")

:\*\* [developers mailing
list](http://bioperl.org/mailman/listinfo/bioperl-l)

:\* IRC: \#bioperl on [Freenode](http://freenode.net)

[Biojava](http://www.biojava.org) :  

<!-- -->

[Biopython](http://www.biopython.org) :  

<!-- -->

[Bioruby](http://www.bioruby.org) :  

<!-- -->

[BioSQL](http://biosql.org) :  

<!-- -->

[BioLib](http://biolib.open-bio.org) :  

<!-- -->

[EMBOSS](http://emboss.sourceforge.net/) :  

### [Google Summer of Code 2009](http://socghop.appspot.com/)

-   Mentoring organizations apply between March 9-13, 2009. Accepted
    mentoring organizations will be published March 18. See [full set of
    timelines](http://code.google.com/opensource/gsoc/2009/faqs.html#0_1_timeline_5354032302481437_).
-   Google expects to accept around 150 mentoring organizations, a bit
    less than in 2008 (when they accepted 175). If the trend over the
    past years is any indication, this will be out of at least 3x as
    many organizations that apply.
-   Students apply between March 23-April 3, 2009. The [eligibility
    requirements for
    students](http://code.google.com/opensource/gsoc/2009/faqs.html#0_1_eligibility_83343977761348_13148542340972003)
    are in the GSoC FAQ.
-   [Development occurs
    on-line](http://code.google.com/opensource/gsoc/2009/faqs.html#0_1_development_where_91701355_4247830955169275),
    there is no requirement or expectation to travel, neither for
    students nor for mentors.

[Category:Summer of Code](Category:Summer_of_Code "wikilink")
