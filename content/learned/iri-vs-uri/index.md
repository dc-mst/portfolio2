---
title: IRI vs. URI and why are they not very common
summary: IRI is an extension of URI that allows for non-ASCII characters
date: 2023-05-15
tags: [ Internet, Fun Facts ]
---

URI stands for Uniform Resource Identifier, and IRI stands for Internationalized Resource Identifier. While they are similar, there is a slight difference between the two.

URI is a generic term that encompasses both Uniform Resource Locators (URLs) and Uniform Resource Names (URNs). URLs are commonly used to locate resources on the internet and often include a network location (e.g., http://portfolio.devcrumbs.com) along with the specific path to the resource. URNs, on the other hand, are persistent identifiers that are independent of the resource's location and can be used to identify a resource even if it has moved.

IRI, on the other hand, is an extension of URI that allows for international characters and non-ASCII characters to be used in the identifier. It was introduced to support non-English languages and characters in web addresses. IRIs are encoded using UTF-8, which enables the use of characters from various scripts, including Chinese, Arabic, Cyrillic, and many others.

## Why IRI is not very common on the Internet?

Backward compatibility poses significant challenges, and there is a strong consensus to avoid disrupting the functioning of the Internet. A typical HTTP request involves traversing numerous layers of software and hardware, making it uncertain whether IRIs (Internationalized Resource Identifiers) will be supported at each stage. In order to ensure compatibility with the current URI (Uniform Resource Identifier) infrastructure, IRIs are typically converted to URIs using percent-encoded ASCII values before transmission. Essentially, this involves employing the encodeURIComponent function.


