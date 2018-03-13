---
layout: post
title:  "WebVR with A-Frame"
date:   2018-03-12 19:29:00 -0700
categories: VR
excerpt: "Using A-Frame to build a solar system in WebVR - the struggle of simplicity and challenge of positioning"
---

This week's one hour hour challenge used A-Frame, a web framework for building VR experiences. From [A-Frame's Website](https://aframe.io), the framework is described as a tool to "Make WebVR with HTML and Entity-Component. Works on Vive, Rift, Daydream, GearVR, desktop."

**Why A-Frame?**
We first heard about A-Frame at a React Boulder meetup last month. The idea being able to build VR with only HTML and a CDN sparked our interest. A-Frame uses [Web VR](https://webvr.info/), "an open specification that makes it possible to experience VR in your browser." It is super easy to get started.

**Technology:**
- A-Frame CDN
- WebVR
- HTML

**How to Get Started:**
There is NO setup. Just add the CDN via script tag.
{% highlight html %}
<script src="https://aframe.io/releases/0.8.0/aframe.min.js"></script>
{% endhighlight %}
[A-Frame Docs](https://aframe.io/docs/0.8.0/introduction/)

**What Next?**
We followed the [Hello WebVR](https://aframe.io/examples/showcase/helloworld/) example and quickly pivoted to building a solar system. In retrospect, it may have been a more productive hour if we attempted an easier <a-scene>, but we are not known to shy away from a challenge.

[Check out our finished product](aframe-hour.surge.sh)

Impressed? I know, we weren't either...

Pros:
- Intuitive
- Very easy to get started
- Docs are full of full examples

Cons:
- Too much magic - This made debugging very challenging since we didn't understand the problem we were solving in the first place
- Mostly fidgeting (rather than "coding") to get the positioning of entities correct. We really just changed numbers and hex values.
- Position was challenging to understand. Perhaps this comes from our rudimentary understanding of Physics? Regardless, we struggled to understand basics concepts like how changing x, y, and z in position="x y z" altered the entity.

Reflections:
- Large focus on design, UI/UX. Confirmation that we are not front-end developers... (not yet at least :) growth mindset!)
- This would be cool for games!!
- Didn't feel like coding because it only involved adding html attributes and fidgeting with numbers. It would be more fun if we incorporated JS (with React) - something so we could play with state, interact with the dom, etc.
- What would our simple solar system look like on a headset?

Would we use it again?
The short answer... No
Not because the tech isn't awesome - it truly is.
Mostly because A-Frame's huge pluses seem to fall in the category of simplifying game developing and VR for the novice and those pluses aren't personal pluses.

All in all, it was a fun hour. Wish I could have gotten Saturn's ring to be round though...

[A-Frame Hour](aframe-hour.surge.sh)
