# Pharo 13 + Hyalinos – Installation Guide

This document explains how to install and run **Hyalinos** on top of **Pharo 13** using **Pharo Launcher** on Linux, macOS and Windows.

You can choose between two approaches:

1. **Prebuilt image** – Install Pharo Launcher and drop in a prepared Pharo 13 image with Hyalinos already installed.
2. **Fresh setup** – Install Pharo Launcher, create a new Pharo 13 image, and install Hyalinos using Metacello.

Prerequisites: Install Pharo Launcher

The recommended way to manage Pharo images and VMs is **Pharo Launcher**. It is available for Linux, macOS and Windows from the official Pharo website https://pharo.org/download

## Option 1 – Use a prepared Pharo 13 image with Hyalinos preinstalled
- Start Pharo Launcher.
- Download an image archive that already contains Hyalinos from [here](https://github.com/hyalinos/icpc/tree/main/images) and unzip it.
- In pharo Launcher click on 'Import' button.
- Choose option 'Import image into Pharo Launcher' and accept. If Pharo Launcher doesn’t show it immediately: Close and reopen Pharo Launcher
- Launch image from the list of images in the launcher.

When the image opens, Hyalinos is already installed and configured. No Metacello step is needed for end users in this scenario.

## Option 2 – Create a new Pharo 13 image and install Hyalinos via Metacello

### Create a Pharo 13 image from Pharo Launcher
- Start Pharo Launcher.
- Click on the 'New' button.
- Choose 'Pharo 13.0' template and click on 'Create image'
- Give the image a name, e.g. Hyalinos13.
- When image is created, click on it the laucher and click on 'Launch'

Pharo will open with a clean Pharo 13 environment.

### Install Hyalinos using Metacello
- Open a Playground by choosing in Browse menu (right-click) → Playground or press Meta+O+P (can depend on keyboar settings).
- Paste a Metacello installation script:

```smalltalk
Metacello new
    baseline: 'Hyphe';
    repository: 'github://hyalinos/hyphe:main';     
  load.
```

Metacello will:

Download Hyalinos and its dependencies, load it into the current Pharo image. Download from Mycelium files with precalculated type results and install them into local storage (%image_folder%/data). When it finishes without errors, Hyalinos is installed and ready.

- Save the image by pressing Shift + Meta + S.

The current image now contains Hyalinos. Next time, simply open Pharo Launcher, select that image, and Launch it – Hyalinos will already be there.
