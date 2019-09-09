# Sort Visualizer in React: Part 1 - Bubble Sort

This is Part 1 of the series, "Sort Visualizer in React". Recently, I've been working on hobby projects that combine computer science concepts with React. Sorting is one such concept that we learn as sophomores in college. I saw a sort visualizer being built in processing.js by The Coding Train YouTube. I thought it'd be a fun idea to build a visualizer in React, so here we are.

You can find the link to the repo and the tutorial [here](https://github.com/ashwanth1109/bubble-sort-visualizer)

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

### Commit 2: Let's host our app on github pages

The next thing I usually do is host my app on github pages so that people can find it online. For those of you who want to know how to host on github pages, you can read on. The rest can skip to the next section.

#### Step 1: Install gh-pages

Github pages has been an easy-to-use and convenient solution for any front-end only hosting needs one might have. You simply install the `gh-pages` package from npm.

```
yarn add gh-pages
```

#### Step 2: Add the homepage attribute

Next you need to add the homepage attribute in your `package.json` file to set up the target endpoint (free from github) for hosting. In my case it is,

```
"homepage": "https://ashwanth1109.github.io/bubble-sort-visualizer"
```

In your case, you can use `https://your-github-id-here.github.io/your-repo-name-here`

#### Step 3: Add the deploy scripts

In your `package.json` add the scripts for `deploy` and `predeploy`. Note that you also have to update your build script from the nano-react-app config to add the public-url flag along with your project folder name.

```json
{
  "scripts": {
    "start": "parcel index.html",
    "build": "parcel build index.html --public-url /bubble-sort-visualizer/",
    "predeploy": "yarn build",
    "deploy": "gh-pages -d dist"
  }
}
```

The predeploy script runs before your deploy script and builds your code for production. The deploy script hosts it on your target endpoint.

#### Step 4: Deploy

Now run the deploy command,

```
yarn deploy
```

You will now find your app in your target endpoint. You can find my app hosted at https://ashwanth1109.github.io/bubble-sort-visualizer/.
