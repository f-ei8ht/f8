---
author: Saif Ali Khan
title: My Competitive Programming Setup
subtitle: ft. Sublime Text and Geany
date: 2025-01-19
Lastmod: 2025-01-19
description: Guide for competitive programming setup
categories:
  - programming
tags:
  - sublime
  - cpp
  - setup

readingSpeed: 20
readingSpeedMin: 50
readingSpeedMax: 100
---

This article offers a sample of my competitive programming setup syntax that can be used to submit, test or code around as well.

<!--more-->

## Prerequisites

Ensure that you have below listed things installed on your system.

- GCC (g++ for cpp)
- They are required to build and compile cpp programs.

## Install Sublime Text

Next you must install sublime text from their [official website](https://www.sublimetext.com).

### Setup for linux

I use 4189 build of sublime on arch by the way, you can download the latest one.

Follow the steps on this [page](https://www.sublimetext.com/docs/linux_repositories.html#pacman).

After downloading sublime text, download linter for c++ on sublime.
- SublimeLinter
- SublimeLinter-gcc 
- Make sure you have package control installed already.

Then add this in sublimlinter settings

```json
// SublimeLinter Settings - User
{
	"debug": true,
	"linters": {
		"SublimeLinter-gcc" : {
			"disable": false,
		}
	},
	"styles": [
		{
			"scope": "region.bluish markup.warning.sublime_linter",
			"types": ["warning"],
			"icon": "square",
			"mark_style": "solid_underline",
			"phantom": "{code}, {msg}, {linter}"
		},
		{
			"scope": "region.redish markup.warning.sublime_linter",
			"types": ["error"],
			"icon": "pointer",
			"mark_style": "squiggly_underline",
			"phantom": "{code}, {msg}, {linter}"
		}
	]
}
```