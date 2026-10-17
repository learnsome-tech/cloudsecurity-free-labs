# m01l04-03 · A control plane manifest that fails the CIS benchmark

**Lesson:** [Security Landing Zones & Centralized Egress Inspection](https://learnsome.tech/learn/cloudsecurity-course/m01l04) (lesson 1.4, module 1: Multi-Account Cloud Architecture & Isolation) · Free  
**Check:** Checker

## Goal

You can describe the baseline a security landing zone gives every new account, review Kubernetes control plane and kubelet flags against CIS benchmark expectations, and explain what a centralised domain allow list really inspects and how it can be bypassed.

## Files

- [`starter/kube-apiserver.yaml`](starter/kube-apiserver.yaml): the listing from the lesson
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l04/m01l04-03/starter`
2. Read `kube-apiserver.yaml` the way the lesson builds it:
   - Lines 1–11: static pod manifest
   - Lines 12–14: anonymous auth
   - Lines 15–19: token auth file
3. Edit `kube-apiserver.yaml` and check it: `kubeconform -strict -summary kube-apiserver.yaml`.
4. Check it from the repository root: `./check m01l04-03`.
5. The site offers these commands for this lab; the first is the default, and the only one graded. Run another with `./check m01l04-03 --command=<id>`:
   - `validate` (Validate): `kubeconform -strict -summary kube-apiserver.yaml`
   - `verbose` (Validate each resource): `kubeconform -strict -verbose -summary kube-apiserver.yaml`

## How to check

`./check m01l04-03` copies `starter/` into a scratch directory and runs `kubeconform -strict -summary kube-apiserver.yaml` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

This is a checker lab: it validates the manifest against the Kubernetes JSON schemas the site uses, in strict mode (unknown fields are errors). Kinds without a schema there, such as custom resources, are reported as skipped. The site shows the checker's report without grading; `./check` passes when the checker finds no errors.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/cloudsecurity-course/m01l04) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
