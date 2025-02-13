---
slug: create-a-python-virtualenv-on-ubuntu-1610
deprecated: true
author:
  name: Christopher Piccini
  email: cpiccini11@gmail.com
description: "This guide will show you how to create a Python virtual environment on your Ubuntu 16.10 Linode."
keywords: ["python", "python virtual environment", "virtualenv"]
tags: ["python","ubuntu"]
license: '[CC BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0)'
aliases: ['/development/python/create-a-python-virtualenv-on-ubuntu-1610/','/development/create-a-python-virtualenv-on-ubuntu-1610/']
modified: 2017-08-14
modified_by:
  name: Linode
published: 2017-08-13
title: "Create a Python Virtual Environment on Ubuntu 16.10"
contributor:
  name: Christopher Piccini
  link: https://twitter.com/chrispiccini11
external_resources:
- '[virtualenv Documentation](http://virtualenv.pypa.io/)'
audiences: ["beginner"]
languages: ["python"]
relations:
    platform:
        key: python-virtual-env
        keywords:
            - distribution: Ubuntu 16.10
---

![Create a Python Virtual Environment on Ubuntu 16.10](python-ve-u16-title.jpg "Create a Python Virtual Environment on Ubuntu 16.10")

## What is a Python Virtual Environment?

A Python Virtual Environment - or `virtualenv` - is a tool to create an isolated Python environment on your Linode. This can be extremely powerful as you can create a virtual environment and install all Python executables/packages to it, leaving no dependencies outside of your created virtual environment.

The purpose of this tutorial is to allow you to create and run Python virtual environments in your Ubuntu 16.10 Linode.

## Before You Begin

1.  This guide uses `sudo` wherever possible. Complete the sections of our [Securing Your Server](/docs/guides/set-up-and-secure/) to create a standard user account, harden SSH access and remove unnecessary network services.

2.  Update your system:

        sudo apt update

## Install Python Virtualenv

1.  To install Python's virtual environment:

        sudo apt install virtualenv

## Create New Directory in Home

1.  Navigate to your users home directory:

        cd

2.  Create a directory named *python-environments*:

        mkdir python-environments

3.  Navigate in the newly created directory:

        cd python-environments

## Create a Virtual Environment in Python 3

1.  Create a virtual environment in Python 3 with the environment name of *env*:

        virtualenv -p python3 env

2.  Validate that environment is installed with python3:

        ls env/lib

## Activate Environment

Activate the newly created virtual environment (the name of the working environment appears in parentheses):

    source env/bin/activate
    (env) testuser@localhost:~/python-environments$

Now that the environment is active, you can install executables and packages only to this virtual environment.

## Deactivate Environment

To deactivate an active virtual environment:

    deactivate

Congratulations! You have created an isolated, Python Virtualenv on your Linode.
