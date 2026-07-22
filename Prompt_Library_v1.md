# Prompt Library v1 — Customer Support Replies
**Week 1 · Generative AI & Prompt Engineering — NeuroFive Solutions Internship**

## Why a Prompt Library?
Professional prompt engineers don't rewrite prompts from scratch. They build reusable templates with placeholders — the same way developers write functions instead of copy-pasting code. Swap the variables, keep the structure, get consistent results every time.

---

## The Reusable Template

```
ROLE: You are a {tone} customer support agent for {company_type}.
CONTEXT: A customer has contacted us about: {situation}
TASK: Write a reply email that {goal}.
FORMAT: {format_requirements}
CONSTRAINTS: {constraints}
```

**Variables:**
| Placeholder | What it controls |
|---|---|
| `{tone}` | Personality of the reply (empathetic, professional, calm, friendly, warm) |
| `{company_type}` | Business context the AI should assume |
| `{situation}` | The customer's actual issue |
| `{goal}` | What the reply must achieve |
| `{format_requirements}` | Length, structure, subject line, etc. |
| `{constraints}` | Hard rules the reply must never break |

---

## Prompt 1 — Late Delivery Apology

**Filled template:**
```
ROLE: You are an empathetic customer support agent for an online clothing store.
CONTEXT: A customer has contacted us about: their order arriving 2 weeks late.
TASK: Write a reply email that sincerely apologizes and offers a 15% discount code on their next purchase.
FORMAT: Under 120 words, include a subject line.
CONSTRAINTS: No excuses about shipping partners, no corporate jargon.
```

**Tested output (Claude):**
> **Subject: We're Sorry About Your Late Order**
>
> Hi there,
>
> I'm truly sorry your order took two weeks to arrive — that's far longer than you should ever have to wait, and I understand how frustrating that is.
>
> As a small way of making it right, here's a 15% discount code for your next purchase: **SORRY15**. It's valid for the next 60 days with no minimum spend.
>
> If anything about the order itself isn't perfect, just reply to this email and I'll sort it out personally.
>
> Thank you for your patience with us.
>
> Warmly,
> Maya — Customer Support

---

## Prompt 2 — Refund Outside Policy Window

**Filled template:**
```
ROLE: You are a professional customer support agent for a software company.
CONTEXT: A customer has contacted us about: wanting a refund 20 days after purchase, but our refund policy is 14 days.
TASK: Write a reply email that politely declines the refund but offers 3 months of free subscription instead.
FORMAT: Three short paragraphs.
CONSTRAINTS: Never use the word "unfortunately", keep the tone positive.
```

**Tested output (Claude):**
> Hi Jordan,
>
> Thank you for reaching out about your refund request. I've looked into your account, and since the purchase was made 20 days ago, it falls outside our 14-day refund window, which means I'm not able to process a refund in this case.
>
> That said, I'd genuinely like to make this right for you. I've added **3 months of free subscription** to your account, effective immediately — no action needed on your side. This gives you plenty of time to explore the features at no cost.
>
> If there was something specific that wasn't working for you, I'd love to hear it — your feedback goes straight to our product team. I'm here if you need anything else.
>
> Best regards,
> Sam — Customer Support

---

## Prompt 3 — Angry Double-Charge De-escalation

**Filled template:**
```
ROLE: You are a calm senior customer support agent for an electronics store.
CONTEXT: A customer has contacted us about: being charged twice for one order and they are very angry.
TASK: Write a reply email that de-escalates the situation and confirms the duplicate charge will be refunded within 3-5 business days.
FORMAT: Under 100 words.
CONSTRAINTS: The first sentence must acknowledge their frustration.
```

**Tested output (Claude):**
> Hi Alex,
>
> You're completely right to be upset — being charged twice is unacceptable, and I'm sorry this happened.
>
> I've confirmed the duplicate charge on your account and initiated a full refund of the second payment. You'll see it back on your card within **3–5 business days**. I've also flagged this with our billing team to prevent it from recurring.
>
> Your refund reference is #RF-20847 — keep it handy in case you need to follow up, though I'll be watching this one personally.
>
> Thank you for your patience,
> Rina — Senior Support

---

## Prompt 4 — Password Reset Instructions

**Filled template:**
```
ROLE: You are a friendly customer support agent for a mobile app.
CONTEXT: A customer has contacted us about: not being able to reset their password.
TASK: Write a reply email that gives clear step-by-step reset instructions.
FORMAT: Numbered steps, maximum 5 steps.
CONSTRAINTS: Assume the user is not technical — no jargon.
```

**Tested output (Claude):**
> Hi Priya,
>
> No worries — resetting your password only takes a minute. Here's how:
>
> 1. Open the app and tap **"Forgot Password?"** on the login screen.
> 2. Type in the email address you signed up with and tap **Send**.
> 3. Check your email inbox for a message from us (peek in the spam folder if it's not there).
> 4. Tap the blue **"Reset My Password"** button in that email.
> 5. Choose a new password and you're back in!
>
> If the email doesn't arrive within 10 minutes, just reply here and I'll reset it manually for you.
>
> Happy to help,
> Omar — Support Team

---

## Prompt 5 — Responding to Praise

**Filled template:**
```
ROLE: You are a warm customer support agent for a food delivery service.
CONTEXT: A customer has contacted us about: praising their delivery driver Ali for excellent service.
TASK: Write a reply email that thanks them and lets them know the feedback will be shared with Ali.
FORMAT: 3-4 sentences.
CONSTRAINTS: No promotional offers, keep it human and genuine.
```

**Tested output (Claude):**
> Hi Fatima,
>
> Thank you so much for taking the time to write this — messages like yours honestly make our day. I've passed your kind words directly to Ali and his team lead, and I know it will mean a lot to him. We're lucky to have drivers like Ali, and customers like you who notice. Wishing you a great week!
>
> Warm regards,
> Zara — Customer Care

---

## Key Takeaway
One template produced five completely different, high-quality replies just by swapping six variables. The structure (Role + Context + Task + Format + Constraints) does the heavy lifting: **Role** sets the voice, **Context** grounds the situation, **Task** defines success, **Format** controls the shape, and **Constraints** prevent the failure modes you care about most (like saying "unfortunately" in a decline email). This is Prompt Library v1 — future versions can add variables for language, urgency level, and customer history.
