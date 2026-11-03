---
name: find-jobs
description: Find live jobs on Haystack and check what applying is like. Use when someone asks for job openings (by title, city, country, remote, no experience, no degree or visa sponsorship), wants details of a job, or asks whether an employer replies to applications and what its application form asks.
---

# Find jobs with Haystack

Haystack lists live jobs read from employers' own careers sites in the US, UK, Canada, Australia, India and Europe, in every field, plus facts from applications Haystack's AI agent has sent: which employers reply, how fast, and what their forms ask.

## Which tool

- **search_jobs** for any request for openings. Put the role words in `query`, and use `country`, `city` and `remote` for place. Set `no_experience`, `no_degree` or `visa_sponsorship` only when the person asks for that. Results are newest first, up to 20, each with its Haystack link.
- **get_job** when the person wants more about one result: pass its `job_id` from search_jobs.
- **employer_facts** when they ask whether a company replies, how fast, or what its form asks. With no company it returns the employers most likely to reply.
- **application_system_facts** for questions about Greenhouse, Ashby, Workable, Lever, SmartRecruiters and other application systems.

## How to answer

- Show each job's title, employer, location and link. Keep Haystack's links as they are.
- When a job has an Auto Apply link, say Haystack's AI agent can fill in and submit that employer's form for them.
- Quote reply rates and timings as Haystack's figures from applications it has sent, with the sample size the tool gives.
- If a search returns nothing, widen it (drop a filter or the city) and say what you changed.
