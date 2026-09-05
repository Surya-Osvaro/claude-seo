# 08: Schema Markup & Meta Tag Generator

> Master templates for structured data (JSON-LD), CTR-optimized meta tags, and LinkedIn Open Graph markup for Osvaro blog posts.

---

## 1. Title Tag & Meta Description Specifications

### Meta Title Tag
* **Length:** 50–60 characters maximum (prevents SERP truncation).
* **Keyword Placement:** Target primary keyword must appear within the first 40 characters.
* **Brand Suffix:** Append `| Osvaro` at the end.
* *Example:* `Immigration Casework Automation: Firm Benchmark | Osvaro` (56 chars)

### Meta Description Tag
* **Length:** 140–155 characters.
* **Core Elements:**
  1. Primary keyword included naturally.
  2. The specific operational pain point solved.
  3. Action-oriented value proposition.
* *Example:* `Discover how high-volume UK immigration law firms cut casework bottlenecks by 40% using automated workflows and client intake systems. Read the Osvaro guide.` (160 chars)

### Open Graph / Social Sharing (Critical for LinkedIn)
Because senior solicitors and legal tech leaders discover content on LinkedIn:
* `og:title`: Clean, engaging statement (no trailing brand suffix needed).
* `og:description`: 2-sentence hook highlighting the operational outcome.
* `og:type`: `article`

---

## 2. Standard Article JSON-LD Schema

Place this script inside the `<head>` of each blog post HTML or Next.js metadata component:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BlogPosting",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://osvaro.com/blog/[article-slug]"
  },
  "headline": "[Article Title Under 110 Chars]",
  "description": "[Meta Description Text]",
  "image": "https://osvaro.com/images/blog/[cover-image].jpg",
  "author": {
    "@type": "Person",
    "name": "Surya Vardhan",
    "jobTitle": "Head of Operations & Systems",
    "url": "https://osvaro.com/about"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Osvaro",
    "url": "https://osvaro.com",
    "logo": {
      "@type": "ImageObject",
      "url": "https://osvaro.com/osvaro-logo.png"
    }
  },
  "datePublished": "2026-09-05T09:00:00+00:00",
  "dateModified": "2026-09-05T09:00:00+00:00"
}
</script>
```

---

## 3. FAQ Schema Markup (JSON-LD)

Generates clean entity understanding for AI models and search engines:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How does casework automation maintain SRA compliance?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Casework automation maintains SRA compliance by enforcing mandatory solicitor sign-offs at critical filing milestones and generating an immutable audit trail for all client communications and document verifications."
      }
    },
    {
      "@type": "Question",
      "name": "What is the typical time saving for high-volume immigration firms?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "High-volume UK immigration law firms typically experience a 35% to 40% reduction in casework cycle times, primarily by eliminating manual document chasing and redundant case management data re-entry."
      }
    }
  ]
}
</script>
```

---

## 4. BreadcrumbList Schema

Assists search engines in understanding site hierarchy:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://osvaro.com"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Blog",
      "item": "https://osvaro.com/blog"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "[Article Title]",
      "item": "https://osvaro.com/blog/[article-slug]"
    }
  ]
}
</script>
```

---

## 5. Pre-Publish Validation Checklist

- [ ] All schema URLs are absolute (`https://osvaro.com/...`), not relative.
- [ ] No placeholder text left inside `@id`, `headline`, or `datePublished`.
- [ ] Title tag is between 50–60 characters.
- [ ] Meta description is between 140–155 characters.
- [ ] JSON-LD parses cleanly with zero syntax errors (valid JSON).
