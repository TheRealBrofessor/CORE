---
title: OSINT Trails
area: learning-trails
question: A viral post claims something outrageous with a screenshot as proof — how do I actually check it?
difficulty: beginner
status: draft
created: 2026-07-04
last_reviewed: 2026-07-04
sources:
tags:
  - learning-trail
  - osint
  - verification
---

# Question

A post is going around with a screenshot "proving" something outrageous. How do I actually check whether it's real before I believe or share it?

# Why It Matters

This is the single most common real-world OSINT scenario most people encounter — not investigating a target, just deciding whether to trust something already in front of them.

# Path Followed

Started at [[Verification_Methods]] for the overall framework, then [[Search_Operators]] to search for the exact text in the screenshot (`"exact phrase"` search) to find the original source rather than trusting the screenshot at face value. Used [[Source_Ranking]] to judge whether the original source was primary or just another re-share. Because the claim involved an image, also checked [[Image_OSINT]] for reverse-image-search technique.

# Source Path

IFLA's *How To Spot Fake News* guidance (via [[Source_Ranking]]'s Sources section) on tracing claims to their origin.

# Answer

Screenshots are trivially easy to fabricate or edit, and a viral repost is not independent corroboration even if thousands of accounts share it — it's often the same single unverified origin. The exact-phrase search traced the claim back to a much less dramatic (and in this example type, often already-debunked or missing) original context. The general lesson: a screenshot alone is never sufficient verification; trace it to its primary source before trusting or sharing it.

# What This Unlocks

A repeatable, fast habit (the [[Source_Verification_Checklist]]) for the next viral claim, instead of starting from scratch each time.

# Next Questions

How do I check whether an image itself has been altered, beyond just checking whether the claim text is accurate?
