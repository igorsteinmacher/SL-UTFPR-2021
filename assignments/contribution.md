# Contribution to an Open Source Software Project

**GROUP ASSIGNMENT**

**Deadline**: MULTIPLE (KEEP YOUR EYES OPEN)

You are requested to make a significant contribution to an Open Source Software project. You will need to interact with the community and the existing code base. You MUST make a code contribution. You may start with a small contribution on documentation or translation to learn the process (although, this is not required).

The first step towards that end is choosing a project. There are a couple of them that I anticipate that can accomodate some of you:

* [Jabref](http://www.github.com/Jabref/Jabref) - Citation Manager. Mainly developed in Java. JabRef people are enthusiastic about applying MVVM to their project. It is a good learning experience, and will certainly help the community. Use the wiki as a starting point for development. In addition there is an example on the JavaFX stuff regarding the MVVM pattern. Here [https://github.com/JabRef/jabref/wiki/Code---JavaFX]. The community is aware that you are working on this course.
* [KDE Cantor](https://edu.kde.org/cantor/) - Music Education project. Mainly developed in C++ and Qt/QML. Filipe Saraiva is a maintainer and I have personal contact with him.
* [animint2](https://github.com/tdhock/animint2) Dr. Toby Hocking is the primary maintainer of the animint2 R package for animated interactive data visualization and he had a student working on a few new features https://github.com/rstats-gsoc/gsoc2020/wiki/Animated-interactive-ggplots#gsoc-coding-project-new-animint2-features this summer. Some things had not been concluded and help would be greatly appreciated. For example the "updating of axes/legends after changing the currently displayed data subset" should be possible for a group.
* [R](https://www.r-project.org/) - The R project for statistical computing is a widely used free/open-source software package for data science. There are literally millions of users, but the R core team consists of only 20-30 members, so there are many outstanding bugs. The ones which the core team needs help wit are listed here https://bugs.r-project.org/bugzilla/buglist.cgi?keywords=HELPWANTED and you should ask for help on their email list https://stat.ethz.ch/pipermail/r-devel/
* [Data.tables](https://github.com/Rdatatable/data.table) - One of the most highly used R packages is "data.table" for efficient data reading / writing / manipulation / processing. Dr. Toby Hocking recommends that the students try to close some data.table issues, starting with those labeled beginner-task https://github.com/Rdatatable/data.table/labels/beginner-task -- this is a really widely used R package but their small dev team is not able to keep up with all the issues.
* [LiPD](https://github.com/nickmckay/lipd-utilities) - LiPD is short for Linked PaleoData. LiPD files are the data standard for storing and exchanging data amongst paleoclimate scientists. The package will help you convert your existing paleoclimate observations into LiPD files that can be shared and analyzed. The project is maintained at NAU by Dr. Nicholas P. McKay.


At the end of the term, it is expected that you have one or more contributions submitted, peer-evaluated (in classroom), reviewed by project members, and accepted. Here are overall steps and dates (more details to come).

**EVERYTHING PRODUCED DURING THE COURSE NEED TO BE PEER-REVIEWED BY ANOTHER GROUP BEFORE THE FINAL SUBMISSION**

| Step                                                        | Expected deliverable                                         | Deadline  |
| ----------------------------------------------------------- | ------------------------------------------------------------ | ------- |
| Checkpoint 0                                                | **Stand up presentation (5-7 minutes)**<br>Decision about project and plan on steps towards contribution | Oct-02  |
| Checkpoint 1                                                | **Presentation<br>**\* Present the task(s) details + progress report<br>* First impressions/guidelines availability<br>* Architectural analysis of the software (document) |  |
| Checkpoint 2                                                | **Group+instructor presentation**<br>Progress report         |  |
| Final submission (tentative)                                | Start to care about submitting your last patches to the project |  |
| Checkpoint 3                                                | Final presentation (group + instructor)<br>*can be done during office hours* |   |
| Contribution to Open Source ([Final report](#Final-Report)) | Summary of the contribution process (I recommend to be written on-the-fly to avoid forgetting things) | |

*IN CASE THE PROJECT IS HOSTED ON GITHUB*: The group will need to curate a fork of the project in which they will work. All commits need to become a Pull-request in this fork to train the students on the git use and also in the GitHub use. To do so, it is recommended that you create a central fork, and each student in the group create a "sub-fork". Whenever there is a pull request ready for reviewing, the instructor (me) will assign another group to proceed with the peer review (giving them a specific deadline to do so -- be prepared to do it within the week). After receiving the OK from the peer-reviewing group, you can go ahead and create a pull request against the other project.


*IN CASE THE PROJECT IS HOSTED **OUTSIDE** GITHUB*: The group will need to curate a clone of the project in which they will work.  Whenever there is a patch ready for reviewing, the instructor (me) will assign another group to proceed with the peer review (giving them a specific deadline to do so -- be prepared to do it within the week). After receiving the OK from the peer-reviewing group, you can go ahead and submit it the way the project wants it.


### Final Report

Each group will write up a document describing the contribution process of an existing large open source project, based on investigating the publicly available information about this project. This is the final deliverable of the project and can contain problems faced during the process, how did you apply your knowledge,and what kind of new skills the group acquired during this journey. It needs to present and overview of the project and the task, followed by the details of your contribution process.
