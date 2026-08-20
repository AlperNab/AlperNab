# ChatGPT / GEO Visibility Fixes for Alper Zakher

Canonical identity:
- Alper Nabil Gabra Zakher
- Alper Zakher
- ألبر نبيل جبرة زاخر
- ألبر زاخر

Primary positioning:
- Senior AI Automation Engineer
- Agentic AI Developer
- AI Systems Builder

Arabic discovery targets:
- مهندس أتمتة ذكاء اصطناعي مصر
- خبير أتمتة بالذكاء الاصطناعي للشركات
- مطور Agentic AI مصر
- أنظمة ذكاء اصطناعي للشركات مصر
- AI Automation للشركات في مصر والسعودية

Required website changes:
1. Split English, Arabic, and German into dedicated URLs instead of stacking all three languages in the same H1/H2/body blocks.
2. Add hreflang for en, ar, de and x-default.
3. Keep a single canonical identity and professional title across homepage, portfolio, GitHub, LinkedIn, Wuzzuf, Nzmly, and other public profiles.
4. Add Person JSON-LD with alternateName, jobTitle, url, sameAs, knowsAbout, and Cairo/Egypt locality.
5. Add Service schema for AI Automation, Agentic AI, RAG/Chatbots, AI Systems, Internal Tools, and AI Consulting/Training where relevant.
6. Verify robots.txt explicitly permits OAI-SearchBot and does not block the important pages.
7. Ensure sitemap.xml contains all canonical language pages and excludes duplicate parameterized URLs.
8. Create dedicated Arabic landing pages around discovery intent, not keyword-stuffed translations.
9. Publish evidence-backed case studies with measurable business outcomes.
10. Add FAQs that answer natural-language client queries ChatGPT users are likely to ask.
11. Update legacy profiles that still position Alper primarily as a Data Analyst.
12. Keep all numeric performance claims evidence-backed and consistent.

Suggested Arabic page set:
- /ar/
- /ar/ai-automation-engineer-egypt/
- /ar/agentic-ai-developer-egypt/
- /ar/ai-automation-business-egypt-saudi/
- /ar/ai-systems/
- /ar/case-studies/

Recommended Arabic homepage title:
ألبر زاخر | مهندس أتمتة وذكاء اصطناعي وAgentic AI في مصر

Recommended Arabic meta description:
ألبر زاخر مهندس أتمتة وذكاء اصطناعي في القاهرة، يبني أنظمة Agentic AI، أتمتة n8n وMake، تطبيقات LLM، مساعدين RAG وأدوات داخلية للشركات في مصر والسعودية.

Recommended English homepage title:
Alper Zakher | Senior AI Automation Engineer & Agentic AI Developer

Recommended English meta description:
Alper Zakher builds AI automation systems, Agentic AI workflows, LLM products, RAG assistants, internal tools and business integrations for companies in Egypt, Saudi Arabia and globally.

Person JSON-LD baseline:
```json
{
  "@context": "https://schema.org",
  "@type": "Person",
  "name": "Alper Nabil Gabra Zakher",
  "alternateName": ["Alper Zakher", "ألبر نبيل جبرة زاخر", "ألبر زاخر"],
  "url": "https://alpernabil.com/",
  "jobTitle": ["Senior AI Automation Engineer", "Agentic AI Developer", "AI Systems Builder"],
  "sameAs": [
    "https://www.linkedin.com/in/alper-zakher",
    "https://github.com/AlperNab"
  ],
  "knowsAbout": [
    "AI Automation",
    "Agentic AI",
    "LLM Applications",
    "RAG",
    "n8n",
    "Make.com",
    "FastAPI",
    "AI Systems",
    "Workflow Automation"
  ],
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Cairo",
    "addressCountry": "EG"
  }
}
```

robots.txt baseline:
```txt
User-agent: *
Allow: /

User-agent: OAI-SearchBot
Allow: /

Sitemap: https://alpernabil.com/sitemap.xml
```

Profile consistency rule:
Do not use Data Analyst as the primary current identity. If it remains historically accurate, keep it only in past experience. Current headline should consistently lead with AI Automation / Agentic AI / AI Systems.
