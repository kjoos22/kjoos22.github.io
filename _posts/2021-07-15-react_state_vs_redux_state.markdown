---
layout: post
title:      "React State vs Redux State"
date:       2021-07-15 18:59:06 +0000
permalink:  react_state_vs_redux_state
---


Redux is a state management library, and can be used with any front-end library, including React. But React itself can also manage state, so why use Redux? What are the advantages, disadvantages, and differences between the two?

Redux state is contained in a global store, and can be accessed by any component that has access to the Redux store. Meanwhile React state is local to the component in question, can be passed down to a child component as props, and if it can be mutated by the child components it will also require a callback function to handle the change. 

So given those differences, when should one be used vs the other? When state doesn't need to persist beyond when the component it relates to unmounts, local state is probably the best choice. It is a more direct approach, and doesn't require making touches to other files in your project to execute. An example of this is the characters that a user is inputting into a field of a form, prior to submission.  If you need state to persist even when the component unmounts, then using the Redux state store is a more appropriate choice. While it is a more indirect approach and requires more steps to get it functioning, it will make passing around the data stored in the state easier. This is typically used for information that will be used throughout the lifecycle of a user's single interaction with your application. Additional use cases for the Redux state store are if unrelated components require access to the same state, or if your application requires the ability to track changes to state. It is worth noting that information that needs to be stored longer than these examples would benefit from being written to an associated database for long term storage.

Ultimately there are several factors to take into consideration when determining whether to use local state or the Redux state store, and you will often find yourself leveraging both within the same project depending on the specific situation. This makes it important to remember the state basics even when you're building a project that has implemented Redux, as there are clear advantages to not using the Redux state store in the right situation. 


