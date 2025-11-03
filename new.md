---
title: "Automating Net Worth Certificates: How I’m Solving a CA Office Bottleneck"
summary: I can't believe we’ve been manually drafting these for so long
time: 1716243156
---

If you’ve worked in a CA office, you know the Net Worth Certificate routine. It’s not hard, but it’s repetitive. The client sends their PAN card, Aadhaar card, and a list of assets—land, gold, bank balances, maybe some liabilities. We open Word, copy-paste from an old template, fill in the numbers, generate a UDIN, print it on the letterhead, sign it, stamp it, scan it, and save it somewhere on the system.

It works, but it’s fragile. One missed detail, one typo, one misplaced file—and you’re backtracking through folders or redoing the draft.

So I decided to fix it.

## The Idea: Let AI Do the Heavy Lifting

I wanted a system that could take care of the grunt work. Something that could:

- Read PAN and Aadhaar card screenshots and extract the relevant data  
- Auto-fill a Net Worth Certificate template (the one we use every day)  
- Create a folder for the client and save everything there  
- Let us input asset and liability details through a clean interface  
- Generate the final document on our letterhead  
- Accept the signed scan and archive it back in the same folder  

Basically, I wanted to turn a 30-minute task into a 3-minute one.
To make this happen, I built a **self-hosted web app** that runs locally on the system or server we use in the office.

## OCR for PAN and Aadhaar

The first bottleneck was data entry. Every time a client sends a PAN or Aadhaar screenshot, someone has to manually type in the name, PAN number, and address. So the self-hosted web app has a bullt-in OCR functionality—so when we upload a PAN or Aadhaar card screenshot, it instantly extracts the relevant data like name, PAN number, and address without any manual typing.

No more typos. No more back-and-forth.

## Auto-Folder Creation

Once the PAN is read, the system creates a folder structure like this:
