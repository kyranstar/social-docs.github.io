---
title: Home
layout: home
---

# OpenSocial 

OpenSocial is a permissionless and composable app store for social networks - personalized communities, unique algorithms, and data from any corner of the internet.

**Why do we need this?**

Social is broken. Centralized social media algorithms are becoming more and more damaging, inducing mass addiction, polarization, and engagement farming. There are a few main causes for this:

1. Misaligned Incentives

Social media platforms are funded by ads, meaning that the longer and more engaged you are on their platform, the more money they make. This feedback loop pushes them to optimize to make content more addictive. 

2. The Social Event Horizon

Creating a social media platform is *really* hard, due to the "cold-start problem." This is when your network has no worth to join since it has no users, making it hard to grow when your network is small. This issue itself stifles innovation, since every new social network idea has to raise millions of dollars, which then makes the founders beholden to VCs.

Fortunately, something new has changed in the past few years with the rise of decentralized social media. Decentralized social media are effectively databases of social media content which are decentralized - meaning no single person or organization can censor the data, and the data is completely open and accessible. Since the data is accessible by anyone, this means that any type of application can be built composably on this data. This unlocks innovation, allowing a single developer to create a social media algorithm that rivals the status quo.

However, decentralized social does not fully solve the problem. In the case of this single developer, it still might be difficult for them to reach users. Their friends and family might try it, but without significant ad-spend, it may be difficult to hit any significant amount of revenue, even if people love it.  If anybody can create an app on top of decentralized social, why can't we have an app store?

OpenSocial's mission is to empower developers to rival social media companies, make the black box of "the algorithm" crystal clear, and to unlock radical change in the way algorithms form our digital world.

**How does it work?**

Our social media algorithms are built up of lego building blocks called Components, each of which is an API hosted by someone. Some examples might include a database indexing Farcaster posts, a web scraper, or a ML ranking model. These components can be created by anyone, as long as they implement the Component Rest API. Once created, every component gets published to the smart contract registry to allow anyone to use it.

Then, using our custom DSL for defining social platforms, anybody can design a social network using any of the available components. 

## Payment Model

Eventually, all contributors who write components or algorithms will get paid for their usage automatically, potentially through microtransactions.

## Algorithm DSL (TODO)

## Component API (TODO)

#### Get Schema

<details>
 <summary><code>GET</code> <code><b>/</b></code> <code>(overwrites all in-memory stub and/or proxy-config)</code></summary>

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | None      |  required | object (JSON or YAML)   | N/A  |


##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `201`         | `text/plain;charset=UTF-8`        | `Configuration created successfully`                                |
> | `400`         | `application/json`                | `{"code":"400","message":"Bad Request"}`                            |
> | `405`         | `text/html;charset=utf-8`         | None                                                                |

##### Example cURL

> ```javascript
>  curl -X POST -H "Content-Type: application/json" --data @post.json http://localhost:8889/
> ```

</details>

#### Compute

<details>
 <summary><code>POST</code> <code><b>/</b></code> <code>(overwrites all in-memory stub and/or proxy-config)</code></summary>

##### Parameters

> | name      |  type     | data type               | description                                                           |
> |-----------|-----------|-------------------------|-----------------------------------------------------------------------|
> | None      |  required | object (JSON or YAML)   | N/A  |


##### Responses

> | http code     | content-type                      | response                                                            |
> |---------------|-----------------------------------|---------------------------------------------------------------------|
> | `201`         | `text/plain;charset=UTF-8`        | `Configuration created successfully`                                |
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
