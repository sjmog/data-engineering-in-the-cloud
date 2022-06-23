# Data Engineering Program

This is an overview of how to use Seta, Spore, and Forage to run a standalone data engineering program that scales from complete beginner to pretty challenging.

## Overview

The basic goal: learners must get a dashboard showing, in as real-time as possible, some calculations and metadata about a bunch of high-throughput application databases.

The dashboard ([Forage](https://github.com/sjmog/forage)) contains several charts, which start simple, and get more complex in a variety of open-ended ways.

> Each learner can have their own dashboard on Forage, so can have their progress tracked individually.

Learners are given three levels of challenge:

1. To get Forage chart(s) displaying correct summary data no more than an hour old.
2. The same – but no more than a minute old.
3. The same – but up to the second.

Learners can tackle charts them in any order, tackle them partially, spend the whole time making one single chart work every second, or split the responsibilities for tackling them among a team.

It's expected that learners will have to:

1. Do a data audit on the country databases, figuring out what all the columns mean (with the help of the [resources](./resources)), and how to handle the slightly messy data.
2. Retro-engineer the data structures needed to make the Forage charts work, with the help of the [specifications](./specifications).
3. Construct an appropriate analytical database structure to supply the data, and make it available via a single, poll-able endpoint.
4. Figure out how to batch- or stream-process data from the application databases into their relevant analytical databases.

## Technical stuff

There are three main applications involved:

1. [Seta](https://github.com/sjmog/seta), which is a tool that sets up the application databases and deploys a configurable traffic simulator,
2. [Spore](https://github.com/sjmog/spore). You can use Spore to turn up the traffic speed, slow it down, empty databases, and so on.
3. [Forage](https://github.com/sjmog/forage) is a dashboard system. Each learner has an account, and simply has to supply 6 URLs to the 6 charts on their dashboard. These URLs are polled every second, displaying data in an interesting way.

## Getting started

At the beginning of the module:
1. Use [Seta](https://github.com/sjmog/seta) to set up application databases and a Spore.
2. Set each learner up with an account on [Forage](https://github.com/sjmog/forage). (Even if they're working in a team).
3. Share the database URIs and Forage account details with the learners.
4. Set the learners off with an informative kickoff making the goal clear, and helping them get started with the first graph.

### Roadmap ✔️ All done!

1. Seta: Set up a bunch of application databases with the right tables. ✔️
2. Harvest: Play with the remote data. ✔️
3. Spore: Start an application which pumps a configurable stream of data into the databases, simulating survey submissions from around the world. ✔️ And allows you to manage the contents of those databases. ✔️
4. Forage: A dashboard with some charts that expect data in a certain format and will poll a given endpoint for it. ✔️