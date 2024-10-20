---
platform: ios
title: Identify Dependencies with Known Vulnerabilities by Scanning Dependency Managers Artifacts
id: MASTG-TEST-0215
type: [static]
weakness: MASWE-0076
---

## Overview

In this test case we are identifying dependencies with known vulnerabilities in iOS. Dependencies are integrated through dependency managers, and there might be one or more of them being used. We therefore need all of the relevant files created by them to analyse them with a SCA scanning tool.

## Steps

1. In order to do this in the most efficient way you would need to ask the developer(s) which dependency managers are being used and to share the relevant file(s) created by them. Follow @MASTG-TECH-0113 for on overview of the package managers and request for the relevant files.

2. Run a SCA analysis tool such as @MASTG-TOOL-0116 against the file(s) created by the dependency manager(s) and look for the use of vulnerable dependencies.

## Observation

The output should include the dependency and the CVE identifiers for any dependency with known vulnerabilities.

## Evaluation

The test case fails if you can find dependencies with known vulnerabilities.