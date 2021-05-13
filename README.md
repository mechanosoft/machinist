# PROJECT MACHINIST (BETTER JFLAP)

***I'm not married to this idea so if you guys have an interesting idea for a
project, it would be nice to brainstorm about it***

If you did 335 the state machine course, you probably used jflap jar to try out
state machines. So jflap is old swing java which looks ugly and doesn't feel
modern. My idea was to make a web based jflap tool in react. So the frontend
will be pretty juicy, and in React typescript similar to the frontend in 390.
But the backend will be microservices-style with probably serverless Lambda
Functions for most of the APIs.

It will have like HackerRank style problems to solve that get you points, get
you gold, silver badge etc. leaderboards and so on. profiles where you can save
your previous state machines, nice clean REST or GraphQL apis.

For reference, here is the JFLAP tool: <http://www.jflap.org/>

I used this bad boy for all of 335 last year. It's a really cool tool for
learning about state machines.

The nice thing about this idea for a project is that there is a real niche -
there is not a tool out there like this. I would have used this instead of JFLAP
during 335.


For the stack, here is what I was thinking (once again, I'm open to ideas):

## FRONTEND
- React w/ TypeScript
- Next.js (instead of Create React App like in 390)
- For styling: styled-components - this is a bit different than 390 where we
  used Material-UI's styling API (which is based on JSS - JavaScript objects as
  your styles instead of CSS)
- For component lib: either Material-UI (pretty good but looks a bit
  Android-ish) or Ant Design (Chinese library, very sophisticated looking
  components 🧐)
- For component lib, there is also: <https://semantic-ui.com/> which is quite
  pleasant to look at.

## BACKEND
- I recently discovered a really cool new framework for doing serverless
  functions; its called "Serverless Framework" (really uncreative name):
  <https://github.com/serverless/serverless>
- If you are not familiar, have a look at an AWS service called Lambda Functions
  (<https://docs.aws.amazon.com/lambda/latest/dg/welcome.html>).
- The lambda functions are sick tech, and they are much much cheaper and more
  scalable than running our own docker containers. Plus you can do them in any
  language you want.
- My recommendation: we use serverless as the first choice for any backend work,
  and then add on other types of deployments as needed.
- Otherwise we can always do the container thing with Amazon ECS or with
  Kubernetes.
- I wanted to do the backend microservice style.


