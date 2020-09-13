# [When to use microservices](https://www.youtube.com/watch?v=GBTdnfD6s5Q&t=48s)

- [Transcript](https://gotopia.tech/bookclub/episodes/moving-to-microservices-with-sam-newman-and-martin-fowler)
- we focus on the tech tool, not the thing the tech things let you do
 - what is thing to give you
- more options to scale up apps
- independenent deployability
- limit the "blast radius" of failure


Our industry tends to focus on tech instead of outcome. One should use microservices as a means to obtain a desired outcome rather than for the sake of using a new technology.

- Microservices are not an on/off switch.
- Microservices are distributed system.
- A single process monolith architecture is not distributed... but actually it is... e.g. reading data from database..


Microservices shouldn't be the default option. If you think a service architecture could help, try it with one of the modules from a very simple monolith typology and let it evolve from there.

1. 0 downtime independent deployability, e.g. SaaS business where you can't afford downtime
2. Isolation of processing around data, e.g. health industries, GDPR... data partitioning
3. Enable a higher degreee of organizational autonomy - distribute responsibilities into teams to reduce the amount of coordination with the rest of the organization.


- independent deployability
- data partitioning
- reflect organizational structure - independent teams

Distributed monolith

1. Create a deployment mechanism
2. Look for pattern, e.g. a collection microservices often being changed together

How to do it
- Use Jira to tie a commit to a piece of work
- Look back at the stories completed and the commits
- Map the commits to the services those stories have impacted
- Decider
  - merge those services back together again
  - look at different ways to slice and dice them

With a smaller interface to the rest of the world, it's easier to make sure that any change you made inside the boundary won't affect the interface.

Challenge - people won't know what information hiding really means.

You can avoid a distributed monolith by:
- Create deployment mechanism
- Looking for patterns and deciding how to deal with theam.

Be aware! People don't know that info hiding really means!

Easier to limit impact of each release with microservices.

There is nothing more complicated than a distributed system.

We should strive for independent deployment because
- easier to limit the impact of of each release when using microservices
- as the team size increase it gets exponentially harder to coordinate a deployment


We tend to violate monolith by not respecting the modules. Breaking them into services makes it harder to do so.



