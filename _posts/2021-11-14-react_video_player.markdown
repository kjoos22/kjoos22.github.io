---
layout: post
title:      "React Video Player"
date:       2021-11-15 01:31:42 +0000
permalink:  react_video_player
---


Have you ever been working on a React project and wanted to embed a video from a 3rd party source directly onto your page? There is a straightforward and easy to use component that will let you do just that, [ReactPlayer](https://github.com/CookPete/react-player). ReactPlayer has support for embedding content from a variety of sources, including file paths, YouTube, Facebook, Twitch, SoundCloud, Streamable, Vimeo, Wistia, Mixcloud, DailyMotion and Kaltura, and more. 

To get started:

```
$ npm install react-player
```
or
```
$ yarn add react-player
```

Then, be sure to import ReactPlayer in the appropriate file:

```
import ReactPlayer from 'react-player'
```

Then set up your component as you would any other React component, and within your *return* include:

```
<ReactPlayer url='https://www.youtube.com/watch?v=dQw4w9WgXcQ />
```

If you are only ever using media from a single source, you can reduce your bundle size by importing the specific [config key](https://github.com/CookPete/react-player#config-prop):

```
import ReactPlayer from 'react-player/youtube'
```
But be aware that this will no longer support media from other sources.

Additionally, there are a plethora of [options](https://github.com/CookPete/react-player#props) that can be set via props, such as auto-play:

```
<ReactPlayer
     url='https://www.youtube.com/watch?v=dQw4w9WgXcQ
		 playing={true}
		 muted={true}/>
```
Note: Since Chrome 66, released in 2018, videos must be muted in order to auto play.

While ReactPlayer is powerful and gives you a lot of flexibility with options, it is also very easy to get running with and can have media embedded in your project within a few minutes.


