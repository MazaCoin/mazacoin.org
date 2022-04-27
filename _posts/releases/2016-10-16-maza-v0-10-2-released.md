---
layout: post
title: "MAZA v0.10.2 Released"
date: 2016-10-16T12:44:33-07:00
category: releases
tags: feature content
image: /img/mazaqt-splash.png

---


<mark>edited 26 January 2022</mark><br>
<mark>This version has been deprecated.</mark><br>
<b><em>Please download the <a href="/releases/2022/01/13/maza-v0-16-3-released/">latest release</a></em></b><br>
<br>


# MAZA v0.10.2 

MAZA-qt and mazad v0.10.2 are now available. 

[Downloads](/download) are available via IPFS & IPFS Web Gateways
 
 - changes Mazacoin & MZC to MAZA
 -  provides a clean rebase onto bitcoin upstream code
     - removes previous Zetacoin base

## Important Upgrade note

Please take this time to backup your existing wallet.dat to a safe place

Those updating from older clients will need to remove the existing peers.dat file, see examples below

This release will change the default directory names from ```mazacoin``` to ```maza``` in all cases
Starting the new client will create a new directory. If you would like you can 
  - move the blockchain data from your old directory to the new directory
  - move your wallet.dat from the old directory to the new directory

You may also move the directory prior to starting you new client:

**Linux**

```bash
  mv ~/.mazacoin ~/.maza
  rm ~/.maza/peers.dat
  mv ~/.maza/mazacoin.conf ~/.maza/maza.conf
```

**OSX**

```bash
  mv ~/Library/Application\ Support/Mazacoin ~/Library/Application\ Support/Maza
  rm ~/Library/Application\ Support/Maza/peers.dat
  mv ~/Library/Application\ Support/Maza/mazacoin.conf ~/Library/Application\ Support/Maza/maza.conf
```


Windows

```powershell
  xcopy  %APPDATA%\Mazacoin %APPDATA%\Maza\ /E
  del  %APPDATA%\Maza\peers.dat
  ren  %APPDATA%\Maza\mazacoin.conf   %APPDATA%\Maza\maza.conf
```

## Downloading via IPFS

While we strive to keep our websites and other services as secure as possible, we
simply cannot keep them as secure as the MAZAchain, or its cousin [IPFS, the 
Interplanetary File System](https://ipfs.io). For this reason, we now provide all of our 
downloads, and signed official sources via IPFS.

**Please see our docs on [How to Download MAZA via IPFS](/docs/2016/10/16/downloading-maza-via-ipfs/)**

## Binaries, SHA sums, gpg signatures will be made available on:
[MAZA on IPFS](https://ipfs.io/ipfs/QmeFphaDUMjMhqih5w54g5mvqKzNMibPJJ8DNehhWtaVME)

MAZA is downloaded from IPFS either with a native IPFS client on your machine (safest) 
or by way of a Web Gateway. 

See our [Download](/download/) page for links and more details. 

## All binaries are gpg signed Please check hashes & signatures!

GPG fingerprint: DEF8 9BAC 042C 094F 3BA8  09A7 0750 81C3 91DC 22D1
Rob Nelson (Release Signing Key) <release-signing@guruvan.net>

To verify a gpg signature:

```console
my_buildmachine:$ cd ~/Directory_with_download
my_buildmachine:$ gpg --recv-keys 91DC22D1
my_buildmachine:$ gpg -k --fingerprint  91DC22D1
pub   4096R/91DC22D1 2016-10-11
      Key fingerprint = DEF8 9BAC 042C 094F 3BA8  09A7 0750 81C3 91DC 22D1
uid       [  full  ] Rob Nelson (Release Signing Key) <release-signing@guruvan.net>
sub   4096R/17BA4334 2016-10-11
sub   4096R/93AEC55F 2016-10-11

my_buildmachine:$ gpg --verify MAZA_v0.10.2_release-IPFS-hashes.sig
gpg: assuming signed data in 'MAZA_v0.10.2_release-IPFS-hashes'
gpg: Signature made Tue Oct 11 10:57:11 2016 PDT using RSA key ID 93AEC55F
gpg: Good signature from "Rob Nelson (Release Signing Key) <release-signing@guruvan.net>" [full]
```

