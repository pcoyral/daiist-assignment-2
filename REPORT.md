# Assignment 2 Report

*Delete this italic guidance as you fill in each section. You'll be asked to
defend any of this without your code in front of you. Write only what you
can actually explain.*

- **Name**: Paul Coyral  
- **Student ID**: 19816
- **Email**: pcoyral.ieu2022@student.ie.edu
- **Group**: PPLEDBA 5A

## Business problem, and the cost of being wrong

*Reading the score from the broadcast scoreboard for a live betting data feed.
The costs are €150 per wrong score published, about €0.21 per missed reading and €0.05 per frame an operator reviews, roughly 730 to 1.
Each figure has a line explaining where it came from.
“Doing nothing” means today’s scouts, at €16.7 per 1,000 frames.*

## Dataset

*version v21 of the Roboflow project, with the link. It explains why the raw images were used instead of the latest version (v25’s flips mirror the scoreboard digits). It also explains why the frames with no scoreboard matter: they show where false alarms come from.*

## What the dataset's composition implies

*the split and class tables, and why the test numbers are thin. It also covers the 5 frames wrongly labelled “no scoreboard”, the tiny boxes (the reason for 960 px), and the test split sharing broadcasts with training.*

## Finetuning and baselines

*yolo11n reaches mAP50 0.93 against 0 for COCO zero-shot and predict-nothing, with the training settings and why yolo11s was dropped.*

## Per-class evaluation and failure modes

*the per-class table and confusion matrix. Team Points carries the result, Shot Clock is the weak class, and the dangerous mistakes are named (the Ohio State/Duke promo, a clock read as a score).*

## Cost matrix and operating point

*The sweep chooses 0.28 / 1.00, so nothing is published without a person yet.
It explains why publishing automatically at 0.85 loses (€6,678 per 1,000 frames).
The deciding assumption is review cost: break-even is about 4.3 s per review.
A sensitivity table shows how the choice moves when each assumption changes.*

## What a person still has to check

*23% of frames, about 36,000 reviews a day and 4.2 operators at the evening peak, against 12 scouts today. Priced against the alternatives, the design is about 30% cheaper than the scouts, but the uncertainty range overlaps theirs. The recommendation is a shadow-mode pilot alongside the scouts.*

## Limitations & next steps

*seven specific ones, each with a concrete next step.*

## Generative AI use disclosure

*Per the syllabus AI Policy: what you used and how, or "no AI content used."*
