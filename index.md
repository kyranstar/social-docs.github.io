---
title: Home
layout: home
---

# OpenSocial 

OpenSocial is a permissionless and composable app store for social networks - personalized communities, unique algorithms, and data from any corner of the internet.

**Why do we need this?**

Social is broken. Centralized social media algorithms are becoming more and more damaging, inducing mass addiction, polarization, and engagement farming. There are a few main causes for this:

1. No Autonomy Over Your Digital Sphere

In today's world, we have very little control over the content we see on the internet. While there are a few controls that let us modulate the flow of information such as disliking or muting, these often don't work and indirectly address the individual issues we have. Every person should be in complete control of the content that forms their digital sphere.

2. Misaligned Incentives

Social media platforms are funded by ads, meaning that the longer and more engaged you are on their platform, the more money they make. This feedback loop pushes them to optimize to make content more addictive. 

3. The Social Event Horizon

Creating a social media platform is *really* hard, due to the "cold-start problem." This is when your network has no worth to join since it has no users, making it hard to grow when your network is small. This issue itself stifles innovation, since every new social network idea has to raise millions of dollars to escape the event horizon, which then makes the founders beholden to VCs.

Fortunately, something new has changed in the past few years with the rise of decentralized social media. Decentralized social media are effectively databases of social media content which are decentralized - meaning no single person or organization can censor the data, and the data is completely open and accessible. Since the data is accessible by anyone, this means that any type of application can be built composably on this data. This unlocks innovation, allowing a single developer to create a social media algorithm that rivals the status quo.

However, decentralized social does not fully solve the problem. In the case of this single developer, it still might be difficult for them to reach users. Their friends and family might try it, but without significant ad-spend, it may be difficult to hit any significant amount of revenue, even if people love it.  If anybody can create an app on top of decentralized social, why can't we have an app store?

OpenSocial's mission is to empower developers to rival social media companies, make the black box of "the algorithm" crystal clear, and to unlock radical change in the way algorithms form our digital world.

**How does it work?**

Our social media algorithms are built up of lego building blocks called Components, each of which is an API hosted by someone. Some examples might include a database of Farcaster posts, a web scraper, or a ML ranking model. These components can be created by anyone, as long as they implement the Component REST API. Once created, every component gets published to the smart contract registry to allow anyone to use it.

Then, using our custom DSL for defining social platforms, anybody can design a social network using any of the available components. 

**Examples**

1. Anna loves Farcaster, but everytime she goes on it past a certain time at night, she sees scary posts and can't sleep. So, she takes an out-of-the-box farcaster feed on OpenSocial, adds a rule that after 9pm the filter "only_fuzzy_cute_things" applies, and creates her new feed.

**Future Featrues**
1. Exclusive communities
2. Groupchats
3. Customizable frontends

## Payment Model

Eventually, all contributors who write components or algorithms will get paid for their usage automatically, potentially through microtransactions. 

## Algorithm DSL (TODO)

## Component API (TODO)

#### Get Schema

<details>
 <summary><code>GET</code> <code><b>/get_schema/</b></code> <code>(returns the component schema)</code></summary>

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | None      |  required | object (JSON or YAML)   | N/A  |


##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`                | `{"code": "200", "body": {}}`                                |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |
> | `405`         | `text/html;charset=utf-8`         | None                                                                |

##### Example cURL

> ```javascript
>  curl -X POST -H "Content-Type: application/json" --data @post.json http://localhost:8889/
> ```

</details>

#### Compute

<details>
 <summary><code>POST</code> <code><b>/compute/</b></code> <code>(overwrites all in-memory stub and/or proxy-config)</code></summary>

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | input      |  required | object (JSON or YAML)   | input, following the schema  |


##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `200`         | `application/json`                | `Configuration created successfully`                                |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |
> | `405`         | `text/html;charset=utf-8`         | None                                                                |

##### Example cURL

> ```javascript
>  curl -X POST -H "Content-Type: application/json" --data @post.json http://localhost:8889/
> ```

</details>

----

[^1]: [It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site).

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
