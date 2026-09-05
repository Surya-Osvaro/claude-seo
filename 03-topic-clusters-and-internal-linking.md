# 03: Topic Clusters & Internal Linking Architecture

> Build topical authority and seamless crawl paths for Osvaro without keyword cannibalization or orphan pages.

---

## 1. The Hub & Spoke (Pillar-Cluster) Model

Search engines and AI models evaluate topical authority as a cohesive cluster, not isolated articles.

```
                  ┌──────────────────────────────┐
                  │      PILLAR PAGE (HUB)       │
                  │ "UK Immigration Law Ops &    │
                  │     Workflow Automation"     │
                  └──────────────┬───────────────┘
                                 │
         ▲                       │                       ▲
         │ (Contextual Link)     ▼ (Contextual Link)     │
┌────────┴─────────┐    ┌────────┴─────────┐    ┌────────┴─────────┐
│     SPOKE 1      │    │     SPOKE 2      │    │     SPOKE 3      │
│ "Automating      │◄──►│ "Reducing Visa   │◄──►│ "Scaling Fee-    │
│ Sponsor Licence  │    │ Document Chasing │    │ Earner Capacity  │
│ Compliance"      │    │ Time"            │    │ Without Hiring"  │
└──────────────────┘    └──────────────────┘    └──────────────────┘
         │                       │                       │
         └───────────────────────┼───────────────────────┘
                                 ▼
                  ┌──────────────────────────────┐
                  │      MONEY / SERVICE PAGE    │
                  │  "Osvaro Operational Audit"  │
                  └──────────────────────────────┘
```

### Roles:
1. **The Pillar Page (Hub):**
   * High-level, authoritative 2,500–4,000 word guide covering the entire subject broadly.
   * Links down to every Spoke article.
2. **The Spoke Pages (Clusters):**
   * Highly specific 1,200–2,000 word tactical guides targeting long-tail keywords.
   * Every Spoke links back to the parent Pillar Page.
   * Spokes link horizontally to related Spokes.
   * Every Spoke includes a contextual CTA linking to an Osvaro product/service page.

---

## 2. Internal Linking Rules for Blog Posts

Every new Osvaro blog post **must adhere to these 5 rules**:

1. **The 3-Link Minimum:**
   * **1 Link Up:** Link to the parent Pillar page in the first 300 words.
   * **1–2 Links Across:** Link to related blog posts (horizontal clusters).
   * **1 Link Down (Conversion):** Link to the relevant Osvaro solution/audit booking page.
2. **Descriptive Anchor Text (Strict):**
   * ❌ **Never use:** "click here", "read more", "this post", "website".
   * ❌ **Never over-optimize:** Do not use exact-match keyword 10 times in anchor text.
   * ✅ **Use natural contextual phrases:** "our guide to [immigration casework automation]", "reducing [client document response times]".
3. **Link Placement Hierarchy:**
   * High-priority contextual links should be placed in the **body copy**, not buried only in the footer or conclusion. Links higher in the body pass stronger relevance signals.
4. **No Orphan Pages:**
   * Whenever publishing a new post, update 2 older, related Osvaro articles to link to the new post within 48 hours of publishing.
5. **Cannibalization Check:**
   * Ensure two articles never target the identical primary keyword. If Article A targets "immigration case management software", Article B must target "immigration case management workflow automation".

---

## 3. Blog Post Internal Link Checklist

Before publishing any draft:
- [ ] Includes link to the relevant pillar page with descriptive anchor text.
- [ ] Links to at least 2 relevant existing Osvaro articles.
- [ ] Contains a clear contextual CTA linking to Osvaro's consultation/audit page.
- [ ] No broken links or placeholder URLs (`href="#"`).
- [ ] External links open in `target="_blank"` with `rel="noopener noreferrer"`.
