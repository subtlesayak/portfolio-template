# Generative Engine Optimization Checklist

GEO means making your public site easy for search engines and AI answer tools to understand. It does not guarantee that an AI tool will mention your site, but it gives crawlers clearer names, summaries, links, and context.

## Before Publishing

1. Replace every `https://your-domain.example` value in these files:
   - `robots.txt`
   - `sitemap.xml`
   - `llms.txt`
   - the `<head>` metadata in each HTML page
2. Replace `Your Name`, `Your Role`, and placeholder social links.
3. Edit your homepage and About page descriptions so they say what you actually do.
4. Give each project a clear title, short description, tools/tags, and thumbnail.
5. Keep project descriptions concrete: role, problem, process, tools, outcome.
6. Remove example projects or clearly label them as examples.
7. Run `node tools/validate-content.js` before publishing.

## Public Files Added For Discoverability

- `robots.txt` tells crawlers the site is public and points them to the XML sitemap.
- `sitemap.xml` lists important pages and project detail pages.
- `llms.txt` gives AI tools a concise Markdown overview of the site.
- HTML meta tags, Open Graph tags, Twitter card tags, and JSON-LD help pages carry useful titles, descriptions, and identity context.

## Write For Humans First

AI tools summarize what is already there. The best GEO improvement is still a clear portfolio:

- Use specific project names.
- Say what your role was.
- Mention tools only when they matter.
- Add outcomes, constraints, or learning points.
- Keep the About page honest and current.

## Privacy Check

Everything in `llms.txt`, `sitemap.xml`, and HTML metadata is public. Do not put private phone numbers, hidden emails, client secrets, private client names, or unpublished work in these files.
