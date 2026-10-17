# m01l03-04 · Deny anywhere wins; allow must appear at every level

**Lesson:** [Service Control Policies & Guardrail Architecture](https://learnsome.tech/learn/cloudsecurity-course/m01l03) (lesson 1.3, module 1: Multi-Account Cloud Architecture & Isolation) · Free  
**Check:** Read along

## Goal

You can predict whether a service control policy stack allows an API call by applying explicit deny first and then the allow-at-every-level rule, and design guardrails that enforce data residency without locking out your own platform team.

## Files

- [`starter/decide.py`](starter/decide.py): the listing from the lesson
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Read `starter/decide.py` alongside the lesson.
2. Follow it the way the lesson builds it:
   - Lines 1–8: load reads policies
   - Lines 9–14: first pass
   - Lines 15–19: the second pass

## How to check

**Read along.** It is a listing to read alongside the lesson, not a program to run.

There is nothing to check: `./check m01l03-04` says so and moves on.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/cloudsecurity-course/m01l03) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
