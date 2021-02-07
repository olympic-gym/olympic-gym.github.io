---
layout: post
title:  "Slack Windows artifacts"
date:   2021-02-07 00:10:35 +0200
subtitle: "Analyzing Slack Windows artifacts"
background: "/img/bg1.png"
---

## Table of Content

* [Overview Analysis process](#technical)
* [important artifacts](#technical)
   * [Dummy](#reverse-engineering-and-malware-analysis)
* [Analyzing artifacts](#technical)
* [References](#references)

## Overview Analysis Process
I used "Process monitor" to be able to monitor "slack.exe" for the files and registry key it writes.   
The full installer file is a sfx archive that contains:   
   1. Nuget "slack-4.12.2-full.nupkg" package   
   2. "RELEASES" text contains (version, sha1hash and Nuget package name)   
   3. .NET "Update" executable that verifies and installes the package   
   4. "background.gif" animation of slack logo   

## Important artifacts

