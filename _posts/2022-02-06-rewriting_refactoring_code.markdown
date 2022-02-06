---
layout: post
title:      "Rewriting/Refactoring Code"
date:       2022-02-06 21:55:25 +0000
permalink:  rewriting_refactoring_code
---


I believe rewriting code is an essential part to maintaining a clean, efficient, and readable codebase, especially as a project continues to grow in scope and size. Sometimes the rewriting is just to keep things consistent (variable, function/method, class names, etc.), especially if there are multiple contributors on a project, or to improve the formatting of the code. Other times the rewriting is essential to bring current logic in line with features and/or code that has been added since the original code was written. 

My approach to rewriting code is always to spend time reading first to make sure I fully understand what the code is currently doing. This makes sure that you don't assume one thing as you make your way through the code, only to have that assumption invalidated by code that you haven't yet reviewed (or you forgot existed) elsewhere in the codebase. Once I feel I have a firm grasp on the codebase, I brainstorm ideas on how that could be streamlined (both for current use and if there are any planned code expansions that I am aware of), then finally I implement said ideas.

One of the major things to consider when brainstorming potential re-writes is efficiency. Perhaps your original implementation wasn't the most efficient option possible, and you have since learned some lessons that make that apparent to you and there is room for improvement. Othertimes, what was an efficient implementation at the time may no longer be so, especially as scope and/or size has expanded. Sometimes functionality that was written in one place has since been written into its own method because it is now used multiple times. Finding the instance of the original code and instead calling the dedicated method is just one example of refactoring.


