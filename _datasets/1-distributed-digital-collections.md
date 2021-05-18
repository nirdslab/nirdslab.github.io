---
layout: dataset
title: Distributed Digital Collections
permalink: /dataset/distributed-digital-collections
---

## Description
The ACM maintains a list of the conference proceedings (http://dl.acm.org/proceedings.cfm), which we retrieved on 9/27/2014 and used as our starting point.
Then we followed each hyperlink to a metadata page that displayed basic information for each corresponding conference and workshop, which in turn allowed us to extract the external URLs.
As a result of this procedure, we were able to extract 6086 URLs – out of which 2001 were unique.
Approximately 75% of the page requests resulted in a response code indicating success (200), which means that no problems were found when trying to fulfill the request.
The remaining pages were mostly divided among page not found (404) responses and timeouts.
We then proceeded to inspect and categorize the 1489 pages that were retrieved with a 200 HTTP response code.
We categorized these pages into three categories by evaluating the relationship between the anchor text and the corresponding retrieved page.
As a result of this categorization, we found that 917 pages were “clearly correct” and 528 were incorrect.
Additionally, we were unable to evaluate 44 pages because their contents didn’t provide us enough information to make an accurate assessment.
These pages could have been placed into the “incorrect” category, but we decided to use an additional category to make our experiment as transparent as possible.

### Index of Dataset
- c: correct 917
- b: blank 140
- e: error 17
- d: deceiving pages - malicious intent 43
- h: directory listings - hello world pages:  18
- k: kind of correct - changed years 197
- l: different language 31
- n: not sure 44
- s: domain for sale - takeover 17
- r: redirects 29
- u: university pages 36

## Copyright Notice
Copyright © 2017 Sampath Jayarathna.
All rights reserved.

Permission is hereby granted, without written agreement and without license or royalty fees, to use this dataset, provided that the dataset is cited in the bibliography as:

- Sampath Jayarathna, and Faryaneh Poursardar. "Change detection and classification of digital collections." In 2016 IEEE International Conference on Big Data (Big Data), pp. 1750-1759, 2016.
- Luis Meneses, Sampath Jayarathna, Richard Furuta, and Frank Shipman. "Analyzing the Perceptions of Change in a Distributed Collection of Web Documents." In Proceedings of the 27th ACM Conference on Hypertext and Social Media, pp. 273-278, 2016.

IN NO EVENT SHALL THE AUTHORS BE LIABLE TO ANY PARTY FOR DIRECT, INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES ARISING OUT OF THE USE OF THIS DATASET AND ITS DOCUMENTATION, EVEN IF THE AUTHORS HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

THE AUTHORS SPECIFICALLY DISCLAIMS ANY WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE. THE DATASET PROVIDED ON AN "AS IS" BASIS, AND THE AUTHORS HAVE NO OBLIGATION TO PROVIDE MAINTENANCE, SUPPORT, UPDATES, ENHANCEMENTS, OR MODIFICATIONS.

## Links
- Download Dataset [Here](https://nirds.cs.odu.edu/~sampath/dataset/Distributed_Digital_Collections_dataset.zip)