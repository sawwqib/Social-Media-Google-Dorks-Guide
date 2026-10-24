
# 🔎 Social Media & Google Dorks Guide

<p align="center">
  <img src="https://img.shields.io/badge/OSINT-Public%20Research-blue?style=for-the-badge" alt="OSINT Public Research">
  <img src="https://img.shields.io/badge/Search-Operators-purple?style=for-the-badge" alt="Search Operators">
  <img src="https://img.shields.io/badge/Focus-Educational-green?style=for-the-badge" alt="Educational">
</p>

<p align="center">
  A detailed collection of search operators for social media research, code discovery, document searches, OSINT, geographic searches, and authorized security auditing.
</p>

---

## 📑 Table of Contents

- [🌐 Social Media Dorks](#-social-media-dorks)
  - [Instagram](#-instagram)
  - [Twitter / X](#-twitter--x)
  - [Facebook](#-facebook)
  - [LinkedIn](#-linkedin)
  - [TikTok](#-tiktok)
  - [Reddit](#-reddit)
  - [Other Social Platforms](#-other-social-platforms)
- [💻 Code, Development & Repositories](#-code-development--repositories)
- [📄 File & Document Dorks](#-file--document-dorks)
- [🧭 OSINT & People-Finding Dorks](#-osint--people-finding-dorks)
- [🛡️ Security Exposure Checks](#️-security-exposure-checks)
- [📍 Geographic & Social Combinations](#-geographic--social-combinations)
- [⚙️ Google-Only Extras](#️-google-only-extras)
- [🌍 Other Search Engines](#-other-search-engines)
- [🧰 Advanced Search Filters](#-advanced-search-filters)
- [🚀 Practical Search Examples](#-practical-search-examples)
- [📘 Common Operators Explained](#-common-operators-explained)
- [⚠️ Responsible Use](#️-responsible-use)

---


# 🌐 Social Media Dorks

Social media dorks use search operators to find publicly indexed profiles, posts, communities, videos, and topic pages.

**Placeholders:** Replace `username`, `keyword`, `cityname`, and other example values with your own search terms.

## 📸 Instagram

| Search Query | What It Does |
|---|---|
| `site:instagram.com "username"` | Finds Liked posts of a Instagram user. |
| `site:instagram.com/p/ keyword` | Finds indexed Instagram post URLs related to a keyword. |
| `site:instagram.com inurl:explore/tags/ keyword` | Searches indexed Instagram hashtag pages. |
| `site:instagram.com "followers" "following" keyword` | Finds pages containing follower and following text alongside a keyword. |
| `site:instagram.com -inurl:p -inurl:reel keyword` | Searches Instagram results while excluding URLs containing post and reel paths. |

## 🐦 Twitter / X

| Search Query | What It Does |
|---|---|
| `site:twitter.com "keyword"` | Finds indexed Twitter pages mentioning a keyword. |
| `site:x.com inurl:status keyword` | Finds indexed X post URLs related to a keyword. |
| `site:x.com -inurl:status -inurl:photo keyword` | Excludes URLs containing status and photo paths. |
| `site:twitter.com "bio" "keyword"` | Finds indexed pages containing both terms. This does not guarantee a match inside the profile bio itself. |

## 👥 Facebook

| Search Query | What It Does |
|---|---|
| `site:facebook.com inurl:profile.php` | Finds indexed Facebook profile URLs using the `profile.php` format. |
| `site:facebook.com inurl:groups keyword` | Finds indexed Facebook group pages related to a keyword. |
| `site:facebook.com "keyword" -inurl:posts` | Finds matching Facebook pages while excluding URLs containing `posts`. |

## 💼 LinkedIn

| Search Query | What It Does |
|---|---|
| `site:linkedin.com/in "job title" "city"` | Finds indexed profiles mentioning a job title and city. |
| `site:linkedin.com/in "keyword" "university"` | Finds profiles containing a keyword and university name. |
| `site:linkedin.com/company keyword` | Finds indexed LinkedIn company pages. |
| `site:linkedin.com/posts keyword` | Finds indexed LinkedIn posts related to a keyword. |

## 🎵 TikTok

| Search Query | What It Does |
|---|---|
| `site:tiktok.com/@ username` | Finds indexed TikTok profile pages associated with a username. |
| `site:tiktok.com inurl:video keyword` | Finds indexed TikTok video pages related to a keyword. |

## 👽 Reddit

| Search Query | What It Does |
|---|---|
| `site:reddit.com/r/subreddit keyword` | Finds indexed pages in a particular subreddit that match a keyword. Replace `subreddit` with the community name. |
| `site:reddit.com inurl:comments keyword` | Finds indexed Reddit discussion pages. |
| `site:reddit.com "keyword" site:reddit.com -inurl:wiki` | Searches indexed Reddit pages for a keyword while excluding wiki URLs. The repeated `site:` condition is redundant but preserves the original query. |

## ▶️ Other Social Platforms

| Search Query | What It Does |
|---|---|
| `site:youtube.com/watch keyword` | Finds indexed YouTube video pages. |
| `site:youtube.com inurl:channel keyword` | Finds indexed YouTube channel pages. |
| `site:youtube.com/c/ username` | Searches for older-style custom YouTube channel URLs. |
| `site:pinterest.com/pin keyword` | Finds indexed Pinterest pins related to a keyword. |
| `site:tumblr.com tagged keyword` | Searches indexed Tumblr tag pages. |
| `site:medium.com "keyword" -inurl:tag` | Finds indexed Medium pages containing a keyword while excluding tag URLs. |
| `site:quora.com keyword` | Finds indexed Quora questions and answers. |
| `site:substack.com keyword` | Finds indexed Substack publications and articles. |
| `site:threads.net @username` | Finds indexed Threads pages mentioning a handle. |
| `site:bsky.app keyword` | Finds indexed Bluesky pages mentioning a keyword. |

---

# 💻 Code, Development & Repositories

These queries help locate public source-code pages, repositories, issues, programming discussions, and package listings.

| Search Query | What It Does |
|---|---|
| `site:github.com "keyword"` | Finds GitHub pages containing an exact phrase or keyword. |
| `site:github.com inurl:blob keyword` | Finds indexed GitHub file pages. |
| `site:github.com inurl:issues keyword` | Finds GitHub issue pages related to a keyword. |
| `site:github.com "filename.py"` | Finds GitHub pages mentioning a Python filename. |
| `site:gitlab.com keyword` | Finds indexed GitLab pages matching a keyword. |
| `site:stackoverflow.com "error message"` | Finds Stack Overflow discussions containing a particular error message. |
| `site:stackoverflow.com/questions keyword` | Finds indexed Stack Overflow question pages. |
| `site:bitbucket.org keyword` | Finds indexed Bitbucket pages related to a keyword. |
| `site:npmjs.com keyword` | Finds npm package pages and related content. |
| `site:pypi.org keyword` | Finds Python packages and project pages on PyPI. |

### 💡 Example

```text
site:github.com "TypeError"
site:github.com inurl:issues "authentication"
site:stackoverflow.com "ModuleNotFoundError"
site:github.com "filename.py"
```

These queries search indexed content. For more precise code searches, use GitHub's built-in code search and filters.

---

# 📄 File & Document Dorks

The `filetype:` operator can help locate indexed documents in particular formats.

| Search Query | What It Does |
|---|---|
| `filetype:pdf "keyword"` | Finds indexed PDF files containing a keyword or phrase. |
| `filetype:xlsx "budget" site:gov` | Searches government-domain results for Excel files mentioning budget. |
| `filetype:pptx "keyword"` | Finds indexed PowerPoint presentations. |
| `filetype:csv "keyword"` | Finds indexed CSV files related to a keyword. |
| `filetype:docx "confidential"` | Searches indexed Word documents containing the word confidential. |
| `filetype:sql "INSERT INTO"` | Finds indexed SQL files containing SQL insert statements. |
| `filetype:env "DB_PASSWORD"` | Searches for indexed environment files containing database-password text. |
| `filetype:log "keyword"` | Finds indexed log files containing a keyword. |
| `filetype:bak keyword` | Finds indexed backup files related to a keyword. |
| `filetype:json "api_key"` | Finds indexed JSON files containing the phrase `api_key`. |
| `filetype:xml "keyword"` | Finds indexed XML files matching a keyword. |

> ⚠️ These searches may return sensitive material accidentally exposed by a website. Do not use or share private credentials or confidential data.

---

# 🧭 OSINT & People-Finding Dorks

OSINT stands for **Open-Source Intelligence**. It involves gathering and analyzing publicly available information for legitimate research.

| Search Query | What It Does |
|---|---|
| `"@gmail.com" site:linkedin.com/in "keyword"` | Finds indexed LinkedIn pages containing an email pattern and keyword. |
| `"firstname lastname" (resume OR cv) filetype:pdf` | Finds indexed resumes or CVs matching a name. |
| `intext:"@company.com" site:github.com` | Finds GitHub pages containing a particular company email domain. |
| `site:docs.google.com "keyword"` | Finds indexed Google Docs pages containing a keyword. |
| `site:drive.google.com filetype:pdf keyword` | Finds indexed Google Drive PDF results matching a keyword. |
| `site:calendar.google.com` | Searches for indexed pages on the Google Calendar domain. |
| `site:pastebin.com "keyword"` | Finds indexed Pastebin pages containing a keyword. |
| `site:scribd.com "keyword" filetype:pdf` | Searches indexed Scribd results for matching PDF content. |
| `site:trello.com "keyword"` | Finds indexed Trello pages containing a keyword. |
| `site:notion.site keyword` | Finds indexed Notion pages matching a keyword. |

### 🔍 Example: Public Professional Research

```text
site:linkedin.com/in "software developer" "London"
site:github.com "Python" "developer"
"firstname lastname" (resume OR cv) filetype:pdf
```

Use these techniques for appropriate public research. Do not use them to expose private personal information, track someone invasively, or access information they have not made public.

---

# 🛡️ Security Exposure Checks

These queries are commonly discussed in defensive security research and search-engine reconnaissance.

**Only assess domains you own or have explicit permission to test.**

| Search Query | What It Does |
|---|---|
| `intitle:"index of" "parent directory"` | Finds indexed pages resembling directory listings. |
| `intitle:"index of" mp3` | Searches indexed directory listings for MP3-related results. |
| `intitle:"index of" .git` | Searches for indexed directory listings mentioning Git metadata. |
| `intitle:"index of" backup` | Finds indexed directory listings containing backup-related text. |
| `inurl:admin intitle:login` | Finds pages with `admin` in the URL and `login` in the page title. |
| `inurl:".env" intext:"DB_"` | Searches for indexed URLs resembling environment files with database-related text. |
| `inurl:phpinfo.php` | Finds indexed pages with `phpinfo.php` in their URLs. |
| `intitle:"Dashboard" inurl:login` | Finds login URLs with Dashboard in the page title. |
| `"Welcome to nginx" site:example.com` | Finds pages on a specified domain displaying the default Nginx welcome text. |
| `inurl:wp-content/uploads filetype:pdf` | Finds indexed PDF files under WordPress upload paths. |

### 🧰 Authorized Website Audit Examples

Replace `example.com` with a domain you own or are authorized to assess.

```text
site:example.com intitle:"index of"
site:example.com filetype:sql
site:example.com inurl:phpinfo.php
```

### 🔐 Security Notes

- A search result does not automatically mean a website is vulnerable.
- Search engines may display outdated or incomplete information.
- Do not attempt to log in to systems without permission.
- Do not download, use, or distribute exposed secrets.
- Report confirmed exposures responsibly to the website owner.

---

# 📍 Geographic & Social Combinations

Combine place names, topics, and platforms to locate relevant publicly indexed pages.

| Search Query | What It Does |
|---|---|
| `site:instagram.com "near" "cityname" keyword` | Finds Instagram pages mentioning a proximity term, city, and keyword. |
| `site:twitter.com "cityname" "keyword" -inurl:status` | Finds indexed Twitter pages mentioning a city and keyword while excluding status URLs. |
| `site:linkedin.com/in "cityname" "keyword"` | Finds LinkedIn profiles mentioning a city and keyword. |
| `site:foursquare.com keyword cityname` | Finds indexed Foursquare pages related to a keyword and city. |
| `site:tripadvisor.com keyword cityname` | Finds TripAdvisor pages related to a topic and location. |

### Example

```text
site:linkedin.com/in "web developer" "Delhi"
site:tripadvisor.com restaurants "Paris"
site:instagram.com "near" "Mumbai" photography
```

Search results depend on the terms used and what the search engine has indexed. They do not verify someone's current location.

---

# ⚙️ Google-Only Extras

Some operators in this section are legacy features or have limited support in modern Google Search.

| Search Query | What It Does |
|---|---|
| `cache:example.com` | Legacy cached-page operator. Google's old cache feature is no longer supported. |
| `related:example.com` | Attempts to find related websites. Support may be limited or unavailable. |
| `define:word` | Searches for a word's definition. |
| `imagesize:1920x1080 keyword` | Attempts to search for images of particular dimensions. Support may vary. |
| `daterange:2459000-2460000 keyword` | Legacy Julian-date range operator. Generally not supported in modern Google Search. |
| `source:keyword` | Legacy Google News source operator. Support may vary. |
| `site:example.com before:2024-01-01` | Searches for pages dated before January 1, 2024. |
| `site:example.com after:2025-01-01` | Searches for pages dated after January 1, 2025. |

### 📅 Date-Based Examples

```text
site:example.com after:2025-01-01
site:example.com before:2024-01-01
```

Date filters may rely on search-engine date interpretation rather than the exact publication date. Verify important dates on the original page.

---

# 🌍 Other Search Engines

Search syntax differs between search engines. Not every operator works everywhere.

## 🔵 Bing

| Operator | What It Does |
|---|---|
| `site:` | Restricts results to a website or domain. |
| `filetype:` | Searches for specific document formats. |
| `intitle:` | Searches for terms in page titles. |
| `inbody:` | Searches page-body text where supported. |
| `language:` | Filters results by language where supported. |
| `loc:` | Restricts results by location where supported. |

## 🦆 DuckDuckGo

DuckDuckGo supports several common search operators, but behavior can differ from Google.

| Operator | What It Does |
|---|---|
| `site:` | Restricts results to a website. |
| `filetype:` | Searches for particular file formats where supported. |
| `"exact phrase"` | Searches for a phrase as written. |
| `-term` | Excludes a term where supported. |

## 🔴 Yandex

| Operator | What It Does |
|---|---|
| `site:` | Restricts results to a website. |
| `mime:` | Filters by document type where supported. |
| `title:` | Searches page titles where supported. |
| `host:` | Restricts results to a host where supported. |

## 🐙 GitHub Search

GitHub's own search interface provides repository-aware filters.

| Filter | What It Does |
|---|---|
| `user:` | Restricts results to a specific user. |
| `org:` | Restricts results to an organization. |
| `repo:` | Searches within a particular repository. |
| `path:` | Filters results by repository path. |
| `language:` | Filters code by programming language. |
| `filename:` | Searches for a particular filename. |
| `extension:` | Filters files by extension where supported. |

### Example

```text
repo:owner/project language:python
org:organization-name filename:README.md
user:username extension:js
```

Check each platform's official search documentation for its current supported syntax.

---

# 🧰 Advanced Search Filters

## 🐦 X Advanced Search

| Filter | What It Does |
|---|---|
| `from:` | Filters posts by author. |
| `to:` | Filters posts addressed to an account. |
| `since:` | Sets the beginning date for a search. |
| `until:` | Sets the ending date for a search. |
| `filter:images` | Finds posts containing images. |
| `min_faves:100` | Looks for posts with at least 100 likes where supported. |

### Example

```text
from:username since:2025-01-01
keyword filter:images
keyword min_faves:100
```

## 👽 Reddit Search

| Filter | What It Does |
|---|---|
| `subreddit:` | Restricts results to a particular subreddit. |
| `author:` | Filters posts by author. |
| `title:` | Searches post titles. |
| `selftext:` | Searches the text of self-posts. |
| `flair:` | Filters posts by flair. |

### Example

```text
subreddit:learnpython keyword
author:username
title:help
flair:Question
```

Filter availability and syntax can change. Use each platform's built-in search documentation when a query does not behave as expected.

---

# 🚀 Practical Search Examples

## 1. 🔎 Find a Public Footprint by Handle

### Search outside Instagram

```text
"@handle" -site:instagram.com
```

**Purpose:** Searches for the handle while excluding Instagram results.

### Search multiple platforms

```text
"handle" (github OR linkedin OR twitter)
```

**Purpose:** Looks for matching public pages across multiple platforms.

### Search indexed PDFs

```text
"handle" filetype:pdf
```

**Purpose:** Finds indexed PDF files mentioning the handle.

---

## 2. 💼 Find Public Professional Information

### Search GitHub pages for a company domain

```text
site:github.com "keyword" intext:"@company.com"
```

**Purpose:** Finds indexed GitHub pages containing a company email domain and a keyword.

### Search LinkedIn profiles by role

```text
site:linkedin.com/in "company name" "engineer"
```

**Purpose:** Finds indexed professional profiles mentioning a company and an engineering role.

---

## 3. 🛡️ Audit Your Own Website

### Check indexed directory listings

```text
site:example.com intitle:"index of"
```

**Purpose:** Searches for indexed pages resembling directory listings on your domain.

### Check indexed SQL files

```text
site:example.com filetype:sql
```

**Purpose:** Searches for indexed SQL files associated with your domain.

### Check URLs resembling environment files

```text
site:example.com inurl:".env"
```

**Purpose:** Searches indexed URLs resembling environment files.

> These queries are only preliminary checks. They do not replace a proper security audit, and they should only be used on domains you own or have permission to assess.

---

# 📘 Common Operators Explained

| Operator | Meaning | Example |
|---|---|---|
| `site:` | Limits results to a site or domain. | `site:github.com python` |
| `filetype:` | Searches for a particular file type. | `filetype:pdf tutorial` |
| `inurl:` | Looks for text in a URL. | `inurl:login` |
| `intitle:` | Looks for text in a page title. | `intitle:dashboard` |
| `intext:` | Looks for text in page content. | `intext:"contact us"` |
| `"..."` | Searches for an exact phrase. | `"web development"` |
| `-` | Excludes a term or supported condition. | `python -java` |
| `OR` | Searches for either of multiple terms where supported. | `developer OR engineer` |
| `before:` | Searches for pages dated before a specified date where supported. | `before:2025-01-01` |
| `after:` | Searches for pages dated after a specified date where supported. | `after:2025-01-01` |

## 🧠 Search Tips

1. Use quotation marks when searching for an exact phrase.
2. Combine `site:` with a keyword to narrow the domain.
3. Use `filetype:` when you need a specific document format.
4. Use `-term` to remove unwanted results.
5. Try different search engines when results are incomplete.
6. Verify information on the original page.
7. Remember that indexed results can be outdated or inaccurate.

---

# ⚠️ Responsible Use

This repository is intended for **education, legitimate OSINT, public information research, and authorized defensive security work**.

- ✅ Search publicly available information for legitimate purposes.
- ✅ Audit websites and repositories you own or are authorized to test.
- ✅ Report accidental data exposure responsibly.
- ❌ Do not attempt unauthorized access to accounts or systems.
- ❌ Do not use or distribute exposed passwords, API keys, or private records.
- ❌ Do not use these techniques to harass, stalk, or expose private information about people.

Search operators do not bypass authentication or guarantee access to private information. They only help filter what a search engine has indexed.

---

# 📌 Important Disclaimer

Search-engine syntax and behavior change over time. Some queries may return no results, and some operators may be unsupported or deprecated.

**A search result is not proof of a vulnerability, ownership, identity, or current location.** Verify findings through appropriate, authorized methods.

---


<p align="center">
  <b>⭐ If this collection helps you, consider starring the repository!</b>
</p>

<p align="center">
  Made With ❤️ By <a href="https://sawwqib.rf.gd">Saqib.</a>
</p>
