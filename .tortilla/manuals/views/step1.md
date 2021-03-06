# Step 1: Introduction

[//]: # (head-end)


In this tutorial we gonna go through the basics on how to write a native add-on to NodeJS using C++, one of the platform's most powerful capabilities of which most web/JS developers now a days are not even familiar with.

For somewhat there is a vacuum which got created around C++ in the recent years, people are so scared from a low-level back-end programming, why should they even deal with memory allocation dilemmas when there are all these interpretation languages like Python, Ruby, and JavaScript who can do that for us? Well folks, once you will realize that all these single web-page application third-party libraries and frameworks are all recycled and repetitive, and you will start doing some real shit by optimizing some heavy-ass machine algorithms, you will realize that **performance is critic**, a title which doesn't really suit NodeJS, with all the love and respect. So why do I even bother making this tutorial? Because people are unaware of many features in the programming world, and the beauty of algorithmics. And why am I even approaching NodeJS developers? Because they have the biggest, most-popular community of all, they have a lot to learn, but they are very open minded, and that's the most important thing. You don't have to be a C++ developer not at all, but if I can at least catch a small part of your attention I will be overwhelmed.

We will create a very small and simple module which calculates the distance between two dots, it can do it either synchronously or asynchronously. The algorithm for calculating the distance between a given `pointA` and `pointB` in a 2D [Cartesian coordinate system](https://en.wikipedia.org/wiki/Cartesian_coordinate_system) looks like this:

    √[(pointAX - pointBX)^2 + (pointAY - pointBY)^2]

Probably not too complicated, kicks me back to the glamorous days in high-school. If put in JavaScript it should take around 10 seconds right? Well in a native NodeJS add-on it should be a bit longer. Of-course when it comes to small logics you shouldn't make too much effort, because it will consume more power only converting all JS objects into C++ native structures. But imagine you would like to run a [blob-detection](https://en.wikipedia.org/wiki/Blob_detection) algorithm and you would like to calculate the [center of mass](https://en.wikipedia.org/wiki/Center_of_mass) of multiple blobs, in C++ it would be much faster, especially when using [shaders](https://en.wikipedia.org/wiki/Shader). Anyways that's not the point of this tutorial, the point is that you will be provided with the necessary tools so next time if you would like to write some heavy logic, you will know how to do it.

We will start with a brief introduction for Google's [v8 engine](https://en.wikipedia.org/wiki/V8_(JavaScript_engine)) and some practical examples on how to use it, this will help us getting start, and then we will write our add-on. Let's begin then shall we?


[//]: # (foot-start)

[{]: <helper> (navStep)

| [< Intro](https://github.com/DAB0mB/node-distance-addon/tree/master@1.1.1/README.md) | [Next Step >](https://github.com/DAB0mB/node-distance-addon/tree/master@1.1.1/.tortilla/manuals/views/step2.md) |
|:--------------------------------|--------------------------------:|

[}]: #
