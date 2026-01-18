<h1 align="center">iGPT - Email Intelligence API for agents & workflow automation</h1>

<p align="center">
  <a href="https://www.igpt.ai/">
    <img src="assets/hero-8153f6e0.gif" alt="iGPT" width="100%" />
  </a>
</p>


<p align="center"><em>Threads • Attachments • Decisions • Follow-ups</em></p>

<p align="center">
  <a href="https://www.igpt.ai/"><img src="https://img.shields.io/badge/Website-111827?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website" /></a>
  <a href="https://docs.igpt.ai/"><img src="https://img.shields.io/badge/Docs-e7a910?style=for-the-badge&logo=book&logoColor=white" alt="Docs" /></a>
  <a href="https://igpt.ai/hub/playground/"><img src="https://img.shields.io/badge/Playground-0066cc?style=for-the-badge&logo=play&logoColor=white" alt="Playground" /></a>
  <a href="https://www.igpt.ai/pricing/"><img src="https://img.shields.io/badge/Pricing-0d6efd?style=for-the-badge&logo=stripe&logoColor=white" alt="Pricing" /></a>
</p>

<p align="center">
  <a href="https://www.igpt.ai/">
    <img src="assets/logo-8153f6e0.png" alt="iGPT" width="96" />
  </a>
</p>

---

### What iGPT is

Most “work context” lives in email - long threads, scattered approvals, buried attachments.

**iGPT is an API that turns that email context into reliable, automation-ready output**:
- Summaries you can trust
- Action items you can run
- Decisions you can log
- Follow-ups you can trigger

---

### What you can build (email-first)

- ✅ **Action items** with `owner` + `due_date` (schema-enforced)
- 🧾 **Decision logs** + approval timelines across threads
- 🚨 **Risk & blocker detection** (what’s stuck, who’s waiting)
- 📎 **Attachment-aware answers** (PDFs, docs, spreadsheets referenced in email)
- 🔁 **Follow-up automation** (missing replies, stale threads, next steps)

---

### Quick start (Node.js)

```bash
npm install igptai
````

```js
import IGPT from "igptai";

const igpt = new IGPT({ apiKey: process.env.IGPT_API_KEY });

// Connect a datasource (per user)
const auth = await igpt.connectors.authorize({
  service: "spike",
  scope: "messages",
  user: "user_123"
});

console.log("Authorize:", auth.url);

// Recall: ask with email context
const res = await igpt.recall.ask({
  user: "user_123",
  input: "List open action items from this week's email threads. Include owner + due date."
});

console.log(res);
```

---

### SDKs

* **Node.js SDK**: `npm install igptai`
* **Python SDK**: `pip install igptai`

---

### Why developers use iGPT

* **Schemas, not prompt parsing** → get strict JSON output you can execute
* **Cited context** → audit and verify answers back to source messages/files
* **Streaming support** → build live UIs and agent pipelines
* **No-throw SDK design** → errors returned as `{ error: string }`

---

### Links

* Website: [https://www.igpt.ai/](https://www.igpt.ai/)
* Docs: [https://docs.igpt.ai/](https://docs.igpt.ai/)
* Playground: [https://igpt.ai/hub/playground/](https://igpt.ai/hub/playground/)
* Pricing: [https://www.igpt.ai/pricing/](https://www.igpt.ai/pricing/)
* Book a demo: [https://www.igpt.ai/contact-sales/](https://www.igpt.ai/contact-sales/)
* Contact: [hello@igpt.ai](mailto:hello@igpt.ai)

