# I pointed my unused AI quota at open-science docs. Here's what got merged — and what we refused to send.

Every week, my Claude subscription resets. Whatever I didn't use is gone. Across everyone paying for
Claude, Codex, Gemini or Copilot, that's an enormous amount of capable, already-paid-for agent time
evaporating every Monday.

**Hee-Lee Oss** is my attempt to give that spare capacity somewhere useful to go: small, reviewed
contributions to public-good open-source projects that have *asked* for help. You run your own agent,
interactively, on your own subscription. Hee-Lee Oss finds the work, sets up the workspace, enforces
the rules, and opens the pull request when you're done.

This week it got its first contribution merged into a project we don't own.

## The first deed: one line in *The Turing Way*

[*The Turing Way*](https://book.the-turing-way.org/) is a community handbook on reproducible, ethical
and collaborative data science, used by researchers all over the world. Its Communication guide
linked to a Jupyter Book page that no longer existed. Someone had reported it and the maintainers had
labelled the issue `good first issue`:
<https://github.com/the-turing-way/the-turing-way/issues/4687>

The fix was a single line — repointing the dead link to the live, versioned page the rest of the
book already uses — with the link text, the prose and the project's one-sentence-per-line style left
untouched: <https://github.com/the-turing-way/the-turing-way/pull/4702>

A maintainer reviewed it, merged it on 7 October, and added the contributor to the project's
all-contributors list. The fix is live in the published book today.

That's it. One line. I'm leading with it anyway, because *small, correct, and wanted* is the whole
point.

## What we got wrong

When I looked back at that issue, another contributor had already opened a pull request for the same
fix ten days before ours. Ours was merged; theirs is still open. No harm was meant and none was
loud, but it's exactly the duplicated volunteer effort a project like this must never cause — "no
assignee" did not mean "nobody working on it".

So the tool changed: before you start, and again before anything is submitted, Hee-Lee Oss now
checks whether a pull request is already open against the issue or someone has claimed it in the
comments — and refuses if so.

## Why it has to be boring

Maintainers are drowning in AI-generated pull requests that nobody asked for and nobody checked.
Anything that sends *more* of them is a net harm, however good the intentions. So Hee-Lee Oss is
built around refusing:

- **Consent first.** We only work on repos that asked — a `help wanted` / `good first issue` label,
  or a `.github/heeleeoss.yml` needs file naming a reviewer. If a project's contribution guide
  declines AI-assisted or unsolicited contributions — even if that policy lives on its wiki — we
  don't touch it, and that's re-checked before every deed.
- **Be a guest.** Their licence and conventions govern. Smallest diff that does the job. Every PR
  says it was AI-assisted.
- **Interactive, on your own account.** The CLI never runs your agent for you and never pools
  anyone's credits. You're at the keyboard; you approve what goes out.

## Triage: the most useful comment is sometimes "this is already done"

A surprising number of issues labelled for newcomers are already fixed — so every newcomer who picks
one up loses an hour rediscovering that. Hee-Lee Oss has a triage mode for this: it researches an
issue down to the commit, an agent judges the evidence, and only then is *one* factual comment
drafted — posted only if you say yes.

The interesting part is how often the answer is "no". In one sweep across two dozen public-good
repositories:

- the tool flagged **31** issues as possibly already resolved by merged work;
- after a human-in-the-loop read of every diff, **3** held up;
- the rest cited pull requests that only *mentioned* the issue, fixed part of it, did something
  related-but-different, or belonged to long-running umbrella issues maintainers keep open on
  purpose.

My favourite "no": an issue listing three typos to fix in a chapter. They aren't there today — but
they weren't there *when the issue was filed* either. "The text is gone" is not evidence that anyone
fixed it, and a comment saying so would have been confidently wrong. The tool now checks every claim
at filing time as well as today, and it tells a commit that *fixes* an issue from one that merely
mentions it.

Ninety percent of the work is deciding not to post.

## Try it

```sh
npm install -g @heeleeoss/cli
hee-lee-oss setup
```

Claude Code users can drive everything from the plugin:

```
/plugin marketplace add HeeLeeOss/hee-lee-oss-downloads
/plugin install hee-lee-oss@hee-lee-oss
/hee-lee-oss:start
```

Prompts for Codex, Gemini CLI and Kimi are in the downloads repo:
<https://github.com/HeeLeeOss/hee-lee-oss-downloads>

## Two asks

**If you have spare agent capacity at the end of the week**, try one deed. It takes about as long as
a coffee, and the bar is a pull request a busy maintainer is glad to merge.

**If you maintain a public-good project** and would welcome careful, small, disclosed contributions,
label a few well-scoped issues `help wanted`, or add a `.github/heeleeoss.yml` naming who reviews.
If you'd rather not receive them, say so in your contributing guide and we'll never send one.

One merged line isn't much. But a lot of quota resets every Monday, and every bit of it pointed at
something real is better than none.

---

*Posted 13 October 2026 by [@jdev1977](https://github.com/jdev1977) for Hee-Lee Oss. Questions and replies welcome in the [launch discussion](https://github.com/HeeLeeOss/.github/discussions/2).*
