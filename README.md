# Written submission: Software Engineer, Machine Learning Systems

Pranav T P

## 1. Tell us about a problem you couldn't leave alone. What did you build to fix it?

I got a bit stuck on something I kept noticing. Creators run their entire business out of a handful of apps that don't talk to each other. Stats over here, brand emails over there, invoices in some spreadsheet, a content calendar floating around somewhere. And they spend so much of their week just holding it all together. I honestly couldn't let it go, so I started building Creuno by myself, a workspace for creators with a way to find sponsorships too.

The advice part is what really got me. Most AI tips are the same for everybody. "Post more often." Great, but that means nothing if you've got a small audience that loves one specific thing. So I built a coach that only looks at your own numbers, your own posts and your own past deals. Nobody else's data touches it. That mattered to me because it's someone's income, and if they don't trust the tool, they just won't open it.

It's in beta right now. You can go from a brand saying yes, to sending the invoice, to getting paid, to wrapping it up, and you can share a media kit when someone asks for one.

## 2. Tell us about a time you had to understand an unfamiliar system that wasn't behaving as expected. How did you get to the bottom of it?

When I joined PROLIM I was dropped into a setup the team had already built around Kafka. Events from the factory floor were flowing through it, and I was building the services on top. Then one job, the one that adds up each shift's numbers, was just painfully slow, and nobody really knew why.

I did what everyone does. I guessed. Threw an index at it. Nothing changed, which was kind of humbling, because it meant I was poking at something I didn't actually understand.

So I slowed down and watched what the database was doing for every request. It wasn't one big slow thing. The job kept asking for the same little bits again and again, one at a time, and saving results the same annoying way. Death by a thousand tiny trips.

After that the fix was almost boring. Stop repeating the lookups, bundle the reads and writes together, add an index that fit how it actually searched. It ended up running in well under half the time. Now I look before I touch anything.

## 3. Describe a real coding task where AI tools helped you move faster. Where did you have to step in and think for yourself?

I use AI tools all the time now, mostly to get through the boring stuff faster. On Sentinel, a tool that checks whether servers follow a protocol, they helped me skim a huge pile of docs, make sense of code I'd never touched, and draft rules and tests way quicker than I could alone.

But there were a couple of moments where I had to stop and think for myself. I'd been telling people the tool caught everything. Then I looked at what that was based on, and it was a set of cases I'd written myself, so of course it did well. When I tried it on a bigger batch of broken examples made automatically, it missed some. So I changed what I said to match what was true. That stung a little.

Another time a rule needed a limit, a point past which it should complain. The easy move was to pick a number. But it would've been a number I couldn't defend, so I made the person using it set their own, and the rule just says "not applicable" until they do.

So that's how I work. Let the tools go fast, then I check anything that matters.

## 4. Describe the extent to which you have experience with production systems.

All my internships were on stuff real people actually used. At PROLIM it was software factory workers relied on every shift, so if I got something wrong, someone at a machine couldn't log their work. At LiRC Tek it was a freight system taking in really messy documents, and dispatchers acted on what came out, so it had to be right. At SparkFX it was a product for community staff, and one community's information could never leak into another's.

And I've got my own thing running too. Creuno is live, and it's just me. There's nobody to pass a problem to. When something breaks, I'm the one who notices, fixes it, and works out how to stop it happening again.

Honestly, that's taught me to care about the unexciting parts. What happens when something fails, how you even find out, how you undo a bad change. I haven't been on call for some giant system and I won't pretend I have. But I've shipped real things, watched them, and fixed them when they went wrong.

## 5. How many years of relevant experience do you have?

About a year, spread over three internships, all on real systems with real users, plus the software I run on my own. Not enough to have strong opinions about tabs versus spaces, but plenty to have been humbled by a slow database.
