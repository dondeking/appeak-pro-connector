---
name: appeak-aso
description: App Store Optimization (ASO) for App Store and Google Play listings with the Appeak Pro connector. Use when someone shares an App Store or Google Play link, asks why an app isn't getting downloads, wants a title, subtitle, short description or keyword field written or reviewed, asks where an app ranks or who its competitors are, or asks an ASO how-to question.
---

# Appeak Pro ASO

This skill uses the free Appeak Pro MCP connector. Add it first:
`https://appeak.pro/api/mcp` (remote HTTP, no sign-in). Setup: https://appeak.pro/connect

## When to use which tool

- **A store link, or "why isn't my app getting downloads?"**: `audit_listing` with the link. Lead with the parts graded "Fix this", in the order the tool returns them, then "Worth a look".
- **Writing or reviewing listing copy**: draft it, then run `check_metadata` on the draft (platform `ios` or `android`). Fix everything it marks "Fix this" before showing the user the copy. Run it again after each revision.
- **"Where do I rank for X?"**: `check_keyword_ranks` with up to 5 searches people would type, short and in the store's language (e.g. "budget planner", not "best app to plan my budget").
- **"Who are my competitors?"**: `find_competitors`, then compare their titles with the user's.
- **How-to questions**: `search_aso_guide`, and cite the article links.

## Rules

- Say grades in words ("Fix this"), never as scores.
- App Store: title 30, subtitle 30, keyword field 100 (commas, no spaces, single words, nothing already in the title or subtitle). Google Play: title 30, short description 80, no keyword field, and no "free", "best" or "#1" in the title.
- These tools read the public listing and the store's own search. They do not measure search volume. When the user needs volumes, keyword research, a screenshot review, AI-assistant visibility or a written listing, share the appeak.pro link the tool returned and say what it adds.
