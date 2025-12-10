# Pharo 13 + Hyalinos – Installation Guide (Linux, macOS, Windows)

This document explains how to install and run **Hyalinos** on top of **Pharo 13** using **Pharo Launcher** on Linux, macOS and Windows.

You can choose between two approaches:

1. **Fresh setup** – Install Pharo Launcher, create a new Pharo 13 image, and install Hyalinos using Metacello.
2. **Prebuilt image** – Install Pharo Launcher and drop in a prepared Pharo 13 image with Hyalinos already installed.

---

## 1. Prerequisites: Install Pharo Launcher

The recommended way to manage Pharo images and VMs is **Pharo Launcher**. It is available for Linux, macOS and Windows from the official Pharo website https://pharo.org/download

## 2. Option 1 – Create a new Pharo 13 image and install Hyalinos via Metacello

### 2.1. Create a Pharo 13 image from Pharo Launcher
Start Pharo Launcher.

On the right side (Templates panel), choose the official Pharo 13 (64-bit) template (or the most recent Pharo 13 entry available).

Click Create Image / New.

Give the image a name, e.g. Hyalinos13.

Confirm. The new image will now appear in the Existing Images list.

(Exact template name can vary slightly depending on the Launcher version, but it will clearly mention Pharo 13.)

### 2.2. Launch the new image
In Pharo Launcher, select your new Hyalinos13 image in Existing Images.

Click Launch.

Pharo will open with a clean Pharo 13 environment.

### 2.3. Install Hyalinos using Metacello
In Pharo, open a Playground:

World menu (right-click) → Playground,
or press Ctrl+O, W / Cmd+O, W depending on key bindings.

Paste a Metacello installation script:

```smalltalk
Metacello new
    baseline: 'Hyphe';
    repository: 'github://hyalinos/hyphe:main';     
  load.
```

Metacello will:

Download Hyalinos and its dependencies, load it into the current Pharo image. Download from Mycelium files with precalculated type results and install them into local storage. When it finishes without errors, Hyalinos is installed and ready.

### 2.4. Save the image with Hyalinos
In Pharo, use World menu → Save and Quit (or your preferred save command).

The current image now contains Hyalinos.

Next time, simply open Pharo Launcher, select that image, and Launch it – Hyalinos will already be there.

## 3. Option 2 – Use a prepared Pharo 13 image with Hyalinos preinstalled
In this path, you:

Install Pharo Launcher (same as before).

Download an image archive that already contains Hyalinos.

Copy the .image and .changes files into the launcher’s images folder.

Launch that image via Pharo Launcher.

3.1. Download the prepared image
Get the archive of the prepared image from the images folder.

3.2. Unzip the prepared image


3.3. Copy the image into the Pharo Launcher images folder

3.4. Make Pharo Launcher see the image
Start / switch back to Pharo Launcher.

Click Refresh in the Existing Images panel if needed.

You should now see Hyalinos13 in the list.

If Pharo Launcher doesn’t show it immediately:

Close and reopen Pharo Launcher, or

In some older versions, use “Import Image…” (if available) and select the .image file inside the images folder.

3.5. Launch the preconfigured Hyalinos image
In Existing Images, select the Hyalinos13 image.

Click Launch.

When the image opens, Hyalinos is already installed and configured (according to how you prepared that image). No Metacello step is needed for end users in this scenario.