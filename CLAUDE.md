# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a GitHub profile repository for [@trinhminhnhat](https://github.com/trinhminhnhat). It contains no application code — only a profile `README.md`, static icon assets, and a GitHub Actions workflow.

## Repository Structure

- `README.md` — GitHub profile page rendered on the user's GitHub profile. Uses raw GitHub URLs to reference icons in `images/icons/`.
- `devcard.png` — Auto-updated daily by the `daily-devcard` workflow via the `dailydotdev/action-devcard` action.
- `images/icons/` — SVG/WebP badge icons referenced in `README.md` via absolute raw GitHub URLs (`https://raw.githubusercontent.com/trinhminhnhat/trinhminhnhat/main/images/icons/`).
- `.github/workflows/daily-devcard.yml` — Runs daily at midnight UTC, on push to `main`, or manually. Commits an updated `devcard.png` using the `USER_ID` repository secret.
- `.github/dependabot.yml` — Keeps GitHub Actions versions up to date (weekly schedule).

## Key Notes

- Icon references in `README.md` use the `main` branch URL.
- The `USER_ID` secret must be set in GitHub repository settings for the devcard workflow to function.
- There is no build system, package manager, linter, or test suite in this repository.
