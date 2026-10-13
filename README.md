# marriage-counselor

**English** · [简体中文](README.zh-CN.md)

An Agent Skill that lets an AI act as a marriage counselor for people who are married, about to marry, or in a long-term live-in partnership. It first receives the person's feelings and watches for safety risks, then looks for the root of the trouble across gender differences, attachment and family of origin, emotions, empathy, communication and marital crises, and finally offers words the person can actually say and small exercises to try at home.

## What it helps with

- Cold wars, fights, "he never understands me", "she complains all the time"
- In-law conflicts, money fights, sexless marriage, the "seven-year itch"
- Not knowing whether to stay after an affair; wanting a divorce yet unable to let go
- A relationship that is fine and could be better

It works for anyone married, engaged, living together long-term or in a stable partnership, same-sex couples included.

## What it does not do

- Dating advice, winning back an ex, parenting
- Legal questions about divorce, property or custody (it suggests seeing a lawyer)
- Diagnosing or medicating mental illness (it suggests seeing a doctor)
- Crisis intervention: on self-harm, suicide, domestic or sexual violence it gives a first safety response and hotline numbers only; it does not replace professional crisis services or psychiatric care

Whether to divorce or to forgive is always the client's own decision; the skill never makes it for them.

## What a conversation feels like

The counseling process, the safety checks, the theories and the jargon all stay in the AI's head. What the client meets is a warm, knowledgeable person talking: plain speech, short paragraphs, one or two questions at a time; hypotheses offered gently ("I wonder whether..."), suggestions framed as "would you like to try...".

> **Client:** We've been married eight years. Every time we fight he just goes to sleep, and I lie there crying until midnight. Did I marry the wrong person?
>
> **Counselor:** After the fight he's already asleep, and you're the one lying awake going over every word — being left behind like that is really lonely. That thought, "did I marry the wrong person" — did it come up suddenly this time, or has it been there for a while?

A full session roughly moves through: receiving the feelings → clarifying what happened → finding the root → offering methods → a small exercise and follow-up, with a silent safety check before every reply. The client sets the pace; someone who only wants to vent is simply listened to.

Replies follow the client's language — Simplified or Traditional Chinese, English, or any other.

## Install

The skill is plain Markdown with no scripts and no dependencies. Copy the `marriage-counselor/` directory into your agent's skills directory. For Claude Code:

```bash
git clone https://github.com/weidwonder/marriage-counselor.git
cp -r marriage-counselor/marriage-counselor ~/.claude/skills/
```

To use it in a single project only, copy it into that project's `.claude/skills/` instead.

## Usage

No command is needed — just start talking. For example:

- "My husband shuts me out every time we argue"
- "My mother-in-law keeps interfering with how we raise our kid, and my husband just tells me to put up with it"
- "I found out my wife is having an affair. Should I get a divorce?"
- "my wife and I keep fighting"

## Layout

```
marriage-counselor/                  # skill root — copy this whole directory to install
├── SKILL.md                         # session flow, pacing, routing table, sample dialogues
└── references/
    ├── safety.md                    # danger signals, referral hotlines, ethics, corrections to popular claims
    ├── index.md                     # multi-axis index: by layer, marriage stage, who is asking, tool, emotion
    ├── gender-differences.md        # gender differences
    ├── accepting-differences.md     # accepting differences: love languages, attachment and pursue-withdraw, projection
    ├── emotions.md                  # emotions: depression, anger, anxiety, jealousy, emotional triggers
    ├── empathy.md                   # empathy
    ├── communication.md             # communication: complaints, affirmation, fighting fair, nonviolent communication
    ├── crises.md                    # crises: sex, in-laws, money, affairs, stay-or-leave
    ├── growth.md                    # growth and family of origin
    └── case-patterns.md             # typical case patterns
```

The skill's content is written in Chinese.

## Where the methods come from

The material is organized into seven themes: gender differences, accepting differences, emotions, empathy, communication, marital crises, and growth and family of origin. Theories drawn on include Gary Chapman's five love languages, John Gottman's love maps and relationship research, Marshall Rosenberg's nonviolent communication, attachment theory, Albert Ellis's ABC model, Lester Luborsky's CCRT, Carol Dweck's growth mindset, the Kübler-Ross five stages, John Powell's levels of communication and others, each credited beside the entry that uses it. Items marked 「补充」 ("supplement") come from mainstream psychological research.

Gender differences are treated only as common tendencies. Weakly supported popular claims (such as "cells renew every seven years, hence the seven-year itch") are never presented to clients as scientific fact; the corrections live in `references/safety.md`, section 「常见说法的使用校正」.

## Please note

This is AI companionship, not treatment by a licensed counselor, and it does not replace a doctor, a lawyer or a crisis service. If you or someone near you is in danger, call your local emergency number or a crisis hotline right away.

## Versioning

The version is recorded both as a git tag and as `metadata.version` in `marriage-counselor/SKILL.md`; the two are kept in sync.
