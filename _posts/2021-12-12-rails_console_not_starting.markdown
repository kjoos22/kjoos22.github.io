---
layout: post
title:      "Rails Console Not Starting"
date:       2021-12-13 03:11:28 +0000
permalink:  rails_console_not_starting
---


The Rails console is a very powerful and very important tool when working with the Ruby on Rails framework. The console is bbuilt upon [IRB](https://github.com/ruby/irb) and funcitons much in the same way. Within the console you can perform many different actions which can be helpful for troubleshooting, testing out ideas, or even changing data directly in your database without having to use your Rails app at large. When testing ideas, the Rails console can be launched using the ```--sandbox``` flag. This enables you to test code without actually changing any data.

For those unaware, the Rails console can be accessed from your terminal with either:

```
rails console
```

or 

```
rails c
```

However, what happens if you invoke the ```rails c``` command and you begin to see output indicating the Rails console is loading, but it never actually loads? This issue is caused by the gem [Spring](https://github.com/rails/spring). Spring is a gem for Rails that speeds up development by keeping your application running in the background. It is a [known issue](https://github.com/rails/spring/issues/396) with Spring that it will hang at times, and in my experience has arisen when introducing additional gems into a Rails project's gemfile. 

There are two simple solutions to deal with this issue. The first one is to just remove the Spring gem from your project, and update your gemfiles accordingly. While this will certain fix the issue, what if you want the benefits of Spring but also need to use the Rails console? Luckily there is a command that will shut down Spring and enable loading of the Rails console. 

Use
```
spring stop
```

then launch your Rails console and there should be no issue. If the issue arises again, use the ```spring stop``` command once more and proceed accordingly. 
