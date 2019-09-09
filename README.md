# Sort Visualizer in React: Part 1 - Bubble Sort

This is Part 1 of the series, "Sort Visualizer in React". Recently, I've been working on hobby projects that combine computer science concepts with React. Sorting is one such concept that we learn as sophomores in college. I saw a sort visualizer being built in processing.js by The Coding Train YouTube. I thought it'd be a fun idea to build a visualizer in React, so here we are.

You can find the link to the repo [here](https://github.com/ashwanth1109/bubble-sort-visualizer)

The commits are organized in a series of steps that are shown below.

### Commit 1: Creating the react app, nano style

While `create-react-app` is my favourite choice for building production apps, I find it too bloated for my quick hobby projects. I was looking for alternatives when I came across [this article](https://hackernoon.com/create-react-app-is-way-too-bloated-5db07c3511) by Adrian Li, whose thoughts I could resonate with. I found a pretty cool alternative in `nano-react-app` which provides a simpler react app with the Parcel bundler (which has none of the configuration decisions that Webpack needs you to think about). You can also check out [this article](https://medium.com/@francesco.agnoletto/i-didnt-like-create-react-app-so-i-created-my-own-boilerplate-190a7dd5d74) on medium for another alternative.

To create & run our app, we simply run:

```
npx nano-react-app bubble-sort-visualizer
cd bubble-sort-visualizer
yarn && yarn start
```

And there you have it folks. Our no-nonsense minimalist react app.
