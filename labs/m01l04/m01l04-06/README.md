# m01l04-06 · A domain allow list rule group

**Lesson:** [Security Landing Zones & Centralized Egress Inspection](https://learnsome.tech/learn/cloudsecurity-course/m01l04) (lesson 1.4, module 1: Multi-Account Cloud Architecture & Isolation) · Free  
**Check:** Read along

## Goal

You can describe the baseline a security landing zone gives every new account, review Kubernetes control plane and kubelet flags against CIS benchmark expectations, and explain what a centralised domain allow list really inspects and how it can be bypassed.

## Files

- [`starter/egress-domain-allowlist.json`](starter/egress-domain-allowlist.json): the listing from the lesson
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Read `starter/egress-domain-allowlist.json` alongside the lesson.
2. Follow it the way the lesson builds it:
   - Lines 1–4: a stateful rule group
   - Lines 5–10: home net
   - Lines 11–19: the targets

## How to check

**Read along.** It is a listing to read alongside the lesson, not a program to run.

There is nothing to check: `./check m01l04-06` says so and moves on.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/cloudsecurity-course/m01l04) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
