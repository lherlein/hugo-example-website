---
title: "BrightSign Developer Blog"
chapter: false
weight: 1
---

![](poweredByPurple.jpg)

# Dev Blog! 2-20-2024

Welcome to the BrightSign developer blog! This is the first entry in what we hope is a long standing developer relations effort. We are planning for this to be the developer's "one-stop-shop" for everything brightsign related, including news related to our CDK, CLI, typescript enablement, and developer focused example efforts (to name a few). 

A little over a year ago, BrightSign created the "Partner Engineering" (PE) Team. Headed up by [Ben Hastings](https://www.linkedin.com/in/bendhastings/), the team's goal is to expand engineering resources and help to not only BrightSign's partners, but also developers around the globe. Ben's vision and well crafted team are helping BrightSign with multiple projects meant to increase available resources and ease of development. As mentioned above, these efforts include a BrightSign CLI, an open source CDK,typescript enablement and full fledged code examples pertaining to working with a BrightSign player. 

## The CLI

About 6 months ago, BrightSign released the first version of the [localDWS API CLI](https://www.npmjs.com/package/@brightsign/bsc). The localDWS APIs are REST APIs that allow for control of any player on the local network ([docs](https://brightsign.atlassian.net/wiki/spaces/DOC/pages/1172734089/Local+DWS+APIs)). The `player-cli`, also known as `bsc`, exposes command line commands and arguments that form and send the proper REST request to attain the required behavior. Since its release, the CLI has gotten continued use from the community, drastically increasing ease of development for BrightSign users around the world. With BrightSign's continued effort and diligence on this task, users will soon be able to accomplish everything they could from the Diagnostic Web Server from the command line!

## The CDK

The PE team is working on a BrightSign Cloud Development Kit (CDK). Usage of this kit will allow users to consume parts (or all) of the npm package that handle interactions with bsn.cloud, from within your script. Have you wanted to make bsn.cloud requests from within your node automation program? Maybe edit permissions of users on your network automatically and en bulk, from a script? Well, with the CDK you can do that and much more. Unfortunately, the kit is not yet released, and a timeline cannot be definitively released. However, the team is hard at work in order to get this out to developers as fast as possible.

Wrapping the CDK will be the second version of the CLI. Not only will v2.0 of the CLI have expanded cloud capability, but the formatting and layout will be significantly improved as well.

## Typescript Support

A parallel effort with the CDK is providing typescript support for any BrightSign interaction. 

## Developer's Cookbook

Github repo with example repos