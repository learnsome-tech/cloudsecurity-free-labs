# m01l03-03 · Does a statement match a request?

**Lesson:** [Service Control Policies & Guardrail Architecture](https://learnsome.tech/learn/cloudsecurity-course/m01l03) (lesson 1.3, module 1: Multi-Account Cloud Architecture & Isolation) · Free  
**Check:** Read along

## Goal

You can predict whether a service control policy stack allows an API call by applying explicit deny first and then the allow-at-every-level rule, and design guardrails that enforce data residency without locking out your own platform team.

## Files

- [`starter/statement.py`](starter/statement.py): the listing from the lesson
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Read `starter/statement.py` alongside the lesson.
2. Follow it the way the lesson builds it:
   - Lines 1–5: six operators
   - Lines 6–14: the holds function
   - Lines 15–22: the applies function

## How to check

**Read along.** It is a listing to read alongside the lesson, not a program to run.

There is nothing to check: `./check m01l03-03` says so and moves on.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/cloudsecurity-course/m01l03) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
