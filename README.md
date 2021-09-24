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
- The web app will look and feel like a modernized version of JFLAP. Sort of similar to Drawio, or Miro, or Figma. Those kinds of apps would be what we are aiming for.
- It will have a big canvas on which you can build your network of nodes.
- You will be able to drag nodes around the page.
- Floating sidebar with options
- You can run state machines with different inputs, generate random inputs, walk through execution of the machine as it processes an input.

## BACKEND
- We will create multiple web services for the app, in a microservice-style architecture.
- The core services will be deployed on a Kubernetes cluster running on AWS or Azure.
- We will make use of other cloud services such as Lambda Functions, message queues, databases, and more
- There will be lots of cloud and devops work to do
- We will explore how to containerize services, how to deploy and scale these services, how to coordinate communication between services, and more
- We will make use of Infrastructure as Code (IaaC) tools like Terraform and Ansible.
- We will write helm charts for our kubernetes projects, in order to easily deploy them.

---


## Description:

### PROJECT MACHINIST

The project is a state-machine simulator like JFLAP (http://www.jflap.org/).  Basically, it is a better version of JFLAP. It will be a web-based tool written with a modern tech-stack, and with some enhanced features on top of simulating state-machines.

What JFLAP does is provide you with an automata editor that you can use to build a state machine. Once you build your machine, you can run different input tapes through the machine. It has a few other interesting features for experimenting with automata.

So this tool, which is tentatively called MACHINIST, would have the following non-exhaustive list of major features:

- **Visual state machine editor**
    - This part is similar to JFLAP, but nicer looking, more user-friendly
    - The controls in JFLAP are very clunky - you get used to it, but there is a lot of room for improvement in the state machine editor
    - Feature Idea: group edit a state machine. Share a link with your colleagues and work on the machine together online. Similar to Miro or Google Docs where you can all edit at the same time.
- **State machine simulation**
    - Same as JFLAP, but nicer + user friendly, it would have easier ways to add your inputs than the JFLAP tool (add through the UI, via file)
    - Step through features for debugging a state machine, inspecting the machine as it runs
    - JFLAP does this well, but again it is quite clunky to use
- **Cloud-connected**
    - Machines can be saved in cloud storage or exported as a file.
    - Share a state machine with your colleagues (generate a share link, send a share email, etc.)
- **Import machines from jflap**
    - JFLAP has a file format for storing state machines, you can import a machine in that format.
- **Hackerrank style educational problems**
    - Hackerrank-style problem sets where you are shown a problem description and then need to create a state machine that solves the problem
    - Similar to these kinds of problems: https://www.hackerrank.com/domains/algorithms
    - Can have points, badges, etc. for solving problems
- **Export state machines in different file formats, or as high quality JPEG, PNG, PDF, etc.**
- **Auto-generate inputs for testing a state machine**
    - The app would have some utilities for creating input strings that you can use to test state machines
    - Also, when you are solving state machine problems, the tool will test your machine with many inputs to determine correctness and whether or not to award a point for that problem.

Basically, it would be a cloud-based JFLAP-like online state machine platform.

Here is a link to a short brief on the project idea, and the likely tech stack:
https://github.com/mechanosoft/machinist
