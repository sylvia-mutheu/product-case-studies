# ResearchCollab

**Sector** AI, SaaS  
**Role** Product Manager

## The problem

An AI research platform for academic users: document parsing, semantic search, citation tracking, systematic literature review, and a virtual peer reviewer. The users are researchers, and researchers are judged on whether their citations are real.

## Constraints

- An audience with an unusually low tolerance for confident wrong answers
- Per-query model cost that scales badly if applied to the highest-volume step
- Outputs that need to be reproducible, because a literature review that returns different results on Tuesday is not a literature review

## What I owned

Product definition across the Research Agent, the Systematic Literature Review workflow, the Topic Explorer, the Knowledge Bank, the Note Editor and the Virtual Peer Reviewer. Requirements gathering, functional specifications, roadmap, and the reporting that settled prioritisation against usage data.

## The decision I would make again

The most useful architectural decision we made was the one that kept AI out of a path.

Retrieval and deduplication in the systematic literature review pipeline run as deterministic logic with no model calls at all. The reasoning is simple. A researcher handed a silently wrong citation list has no way to detect it. The failure is invisible at exactly the moment it does the most damage. Determinism also means the same query returns the same result set, which is what makes the output defensible in a methods section.

The model earned its place where the user can see the output and judge it: summarisation, drafting, and the peer reviewer, which critiques rather than rewrites so that authorship stays with the user.

That test, where is the output checkable by the person receiving it, is the one I now apply to every AI feature I scope.

## What this cost

Being disciplined about where AI belongs meant saying no to demos that would have looked more impressive. The deterministic pipeline is invisible when it works. Nobody screenshots it.
