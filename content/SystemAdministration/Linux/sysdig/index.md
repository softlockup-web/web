---
title: "Debugging Linux Kernel with sysdig"
description: "Learn how to use sysdig to debug Linux Kernel issues"
date: 2024-07-12T12:00:00+01:00
author: "Samuel Matildes"
authorURL: "https://github.com/samatild"
tags: ["linux", "sysadmin", "kernel", "debug", "sysdig"]
iconvendor: "lucide"
icon: "scan-search"
iconcolor: "#ff9580"
---
---

# Introduction

Sysctl is a powerful tool used to check kernel calls at runtime. You can debug kernel calls as sysctl comes with a rich library of LUA scripts that we call chisels.

On this article we are going to cover:
- How to install sysdig
- How to use sysdig to debug kernel issues at runtime
- How to capture sysdig scripts as pcap files

# Installation

Source: https://github.com/annulen/sysdig-wiki/blob/master/How-to-Install-Sysdig-for-Linux.md

## Automatic Installation  
To install sysdig automatically in one step, simply run the following command. This is the recommended installation method. For step-by-step manual installation, see the guide below. To install sysdig from the source code, see the instructions [here](How to Install sysdig from the Source Code).

```
curl -s https://s3.amazonaws.com/download.draios.com/stable/install-sysdig | sudo bash
```

## Manual Installation 

Please follow the official instructions for the [Manual Installation](https://github.com/annulen/sysdig-wiki/blob/master/How-to-Install-Sysdig-for-Linux.md#manual-installation)

# Usage

## Listing Chisels

To list available chisels, you can use the following command:

```bash
sysdig -cl

```
