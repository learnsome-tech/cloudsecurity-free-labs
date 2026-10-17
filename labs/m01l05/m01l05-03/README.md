# m01l05-03 · Tracing packets hop by hop

**Lesson:** [Cloud Network Isolation: VPC Peering & PrivateLink](https://learnsome.tech/learn/cloudsecurity-course/m01l05) (lesson 1.5, module 1: Multi-Account Cloud Architecture & Isolation) · Free  
**Check:** Graded

## Goal

You can trace a packet through peered VPC route tables, spot CIDR overlaps that block peering, and choose between peering and PrivateLink by what each one exposes.

## Files

- [`starter/route.py`](starter/route.py): the listing from the lesson
- [`starter/routes.json`](starter/routes.json)
- [`expected.txt`](expected.txt): the output the check compares with
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l05/m01l05-03/starter`
2. Read `route.py` the way the lesson builds it:
   - Lines 1–6: loads the tables
   - Lines 7–11: the lookup function
   - Lines 12–18: the trace function
   - Lines 19–22: three packets
3. Run it: `python3 route.py`.
4. Check it from the repository root: `./check m01l05-03`.

## Expected output

```text
vpc-app to 10.2.4.20: vpc-app > vpc-hub > delivered
vpc-app to 10.3.9.15: vpc-app > vpc-hub > dropped
vpc-hub to 10.3.9.15: vpc-hub > vpc-data > delivered
```

## How to check

`./check m01l05-03` copies `starter/` into a scratch directory and runs `python3 route.py` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

It passes when the output matches `expected.txt` by the site's rules, within the limits. Standard output is compared line by line; spaces at the end of a line and blank lines at the end do not count. If that differs, standard output followed by standard error is compared with Python traceback frames and blank lines set aside, so a lesson that shows an error passes when your program prints the same error. A pass here is a pass on the site.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/cloudsecurity-course/m01l05) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
