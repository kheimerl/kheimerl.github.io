# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A static HTML academic personal website for Kurtis Heimerl, Associate Professor at UW CSE. Hosted at kurti.sh / kheimerl.github.io. No build system, no framework — just hand-edited HTML/CSS.

## Structure

- `index.html` — main page (bio, news, students, teaching, service, publications list)
- `minimal.css` — single stylesheet for the entire site
- `pubs/` — publication PDFs and an older standalone publications page (`pubs/index.html`)
- `press/` — press coverage HTML
- `images/` — photos used on the site
- `jquery-*.min.js`, `jquery.tmpl.min.js` — vendored jQuery (used for templating on the main page)
- `cv.pdf`, `ResearchStatement.pdf`, `TeachingStatement.pdf` — linked documents

## Editing

No build step. Edit `index.html` directly and open it in a browser to preview. The CNAME file sets the custom domain to `kurti.sh`.

## Conventions

- Publications in `index.html` follow a consistent `<p class="pub">` pattern with `<span class="pubtitle">` / `<a class="pubtitle">`, `.pubauth`, `.pubvenue`, `.publinks`, and optionally `.pubaward` spans.
- News items use `<p class="newsitem">` with a `<p class="newsdate">` pair.
- Teaching entries use `<li class="course">`.
- The page uses jQuery templating (`jquery.tmpl`) to render publication entries from inline `<script type="text/x-jquery-tmpl">` templates — new pubs should follow the existing template data pattern in `index.html`.
