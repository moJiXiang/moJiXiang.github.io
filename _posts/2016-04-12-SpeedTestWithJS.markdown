---
layout: post
title: "Speed Test With JavaScript"
date: 2016-04-124
categories: video cdn
---

### 原理

#### Ping

This test sends HTTP requests to the selected server, and measures the time it takes to get a response.

#### Download Speed

1. Your computer downloads small binary files from the web server to the client, and we measure that download to estimate the connection speed.

2. Based off this result, we choose how much data to download for the real test.Our goal is to pick the right amount of data that you can download in 10 seconds, ensuring we get enough for an accurate result but not take too long.

3. Prevent caches from throwing off results by appending random strings to each download.

4. Once we start downloading, we use up to four HTTP threads to saturate your connection and get an accurate measurement.

5. Received 30 times per second.

6. Then aggregated into 20 slices(each being 5% of the samples).

7. Discard the fastest 1-% and slowest 30% of the slices.

8. The remaining slices are averaged together to determine the final result.
