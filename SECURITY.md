# Security and Disclosure Policy

This repository is a **sanitized educational portfolio** based on an authorized university lab assessment.

## What is intentionally excluded

The portfolio does not intentionally publish:

- active credentials or passwords;
- session cookies or access tokens;
- private keys;
- internal host addresses that are not necessary for understanding the work;
- database credentials;
- personally identifying user data from the assessed environment;
- copy-paste exploitation instructions against a live target.

Some original team repositories and historical commits may contain lab-only values that were used during the course exercise. Those values are **not duplicated here**.

## Scope of the findings

The findings in this repository apply to the specific **lab deployment and configuration** that was assessed. They should not be interpreted as a universal statement that every OJS installation has the same vulnerabilities.

Some SAST results identify security-sensitive code patterns rather than fully demonstrated exploit paths. Where exploitability was not proven end to end, this portfolio uses terms such as **potential** and explains the dependency on data flow and runtime context.

## Responsible use

Only test systems for which you have explicit authorization. The techniques and terminology documented here are intended for defensive security learning, assessment methodology, and portfolio review.

## Reporting a problem with this portfolio

If this repository accidentally exposes information that should not be public, please contact the repository owner through GitHub and identify the file/path that should be reviewed.

Do not open a public issue containing new credentials, secrets, or sensitive personal data.
