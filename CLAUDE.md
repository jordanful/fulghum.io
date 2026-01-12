# fulghum.io

Personal website for Jordan Fulghum. Static HTML files, no backend or build process.

## Publishing a new post

When you publish a new post:

1. Create the HTML file (copy structure from an existing post)
2. Add it to the list in `index.html`
3. Add an `<item>` to `feed.xml` with:
   - `<title>` - post title
   - `<link>` - full URL (https://fulghum.io/slug)
   - `<guid>` - same as link
   - `<pubDate>` - RFC 822 format (e.g., `Mon, 06 Jan 2025 00:00:00 GMT`)
   - `<description>` - post description from meta tags

## RSS feed

The RSS feed is at `/feed.xml`. RSS readers auto-discover it via the `<link rel="alternate">` tag in the HTML head (add this to new posts too):

```html
<link rel="alternate" type="application/rss+xml" title="RSS" href="/feed.xml">
```
