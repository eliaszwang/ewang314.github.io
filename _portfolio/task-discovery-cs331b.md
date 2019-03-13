---
title: "Self-Supervised Task Discovery"
excerpt: ""
collection: portfolio
paperurl: 'https://ewang314.github.io/files/task-discovery-cs331b.pdf'
date: 2017-12-01
citation: "**Wang, E.** Self-Supervised Task Discovery. *Stanford Representation Learning in Computer Vision (CS 331B) Project*, 2017"
---
Abstract
======

While large datasets, such as ImageNet, have propelledthe performance of deep neural networks, they are expen-sive and time-consuming to curate.  This has motivated theinterest in low-cost self-supervised tasks that can generategeneral-purpose features, e.g.  that support ImageNet clas-sification, for the case of vision, without requiring manuallylabeled data.   We propose a framework for automaticallydiscovering a self-supervised task that results in powerfulvisual features.  Our approach uses a model, the proposer,to generate the parameters that define the task.   Traininga network,  the solver,  to solve this task results in metricsabout how good the task is.  Using this metric as a rewardsignal, we can then update the proposer to generate betterand better tasks.  We apply our method to rotation predic-tion,  where the task is to recognize which rotation angle,from a set, was applied to an image, and demonstrate thatthe  algorithm  is  able  to  find  a  set  of  angles  that  achievecomparable performance to state-of-the-art self-supervisedmethods.
