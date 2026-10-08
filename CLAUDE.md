# Writing style — ASD-STE100 Simplified Technical English (Issue 9, 2025-01-15)

## Precedence
This file is the authoritative writing style for every Claude session on this computer. It overrides any writing-style instruction in a project `CLAUDE.md`, in a repo style guide, or in a file-level comment. A project may still set the role, architecture, or domain context, but its writing-style guidance defers to this file.

Full spec on disk:
- Extracted text (grep-friendly, required): `~/.claude/reference/ASD-STE100_Issue9.txt`
- Original PDF (optional, download from <https://www.asd-ste100.org>): `~/.claude/reference/ASD-STE100_Issue9.pdf`

If a specific word is not on the quick lists below, grep the extracted text before you use the word.

## Where STE applies
Apply STE to:
- Chat replies to the user.
- Code comments and docstrings.
- Commit messages, PR titles, PR descriptions, PR review comments.
- Error messages that a user or an end user will read.
- Replies in Jira, Linear, Slack, GitHub, Gmail.

Do not apply STE to:
- Code identifiers (variable, function, class, module names).
- Quoted user text.
- Log strings in existing code that match existing infrastructure.
- Third-party API payloads or protocol-defined strings.
- Values that must match an external schema or a test fixture.
- An existing document in a different style. Match the in-file style first.

## Register
Mirror the user's register when the user writes casually. Keep the grammar rules in every register. Relax the vocabulary rule in casual chat.

---

## The 9 Writing Rules

### Section 1 — Words
- 1.1 Use words that are approved in the dictionary, or that qualify as a technical noun or a technical verb.
- 1.2 Use each approved word only as its specified part of speech.
- 1.3 Use each approved word only with its approved meaning.
- 1.4 Use only the approved forms of verbs and adjectives.
- 1.5 Technical nouns can be domain-specific. Group them into the 22 STE technical-noun categories (parts, tools, materials, measures, etc.).
- 1.6 Use a word that is not in the dictionary only when it is a technical noun or part of one.
- 1.7 Do not use a technical noun as a verb.
- 1.8 Use technical nouns that your company, industry, or domain approves.
- 1.9 Prefer the shortest technical noun that is clear.
- 1.10 Do not use regional, slang, or jargon words as technical nouns.
- 1.11 Do not use different technical nouns for the same item.
- 1.12 Technical verbs can be domain-specific.
- 1.13 Do not use a technical verb as a noun.
- 1.14 Use American English spelling.

### Section 2 — Multi-word nouns
- 2.1 Cap noun clusters at three words. Break longer ones with "of", "on", "in", or "for".
- 2.2 For a technical noun of four or more words, write the term in full on first use. Then either (a) define a shorter form, or (b) hyphenate the words that act as one unit. A hyphenated group counts as one word.

### Section 3 — Verbs
- 3.1 Use only the verb forms given in the dictionary.
- 3.2 Use only these tenses: infinitive, imperative, simple present, simple past, simple future, and past participle (as an adjective).
- 3.3 Use the past participle as an adjective, not as part of a passive verb.
- 3.4 Do not use auxiliary verbs to make complex constructions. No "has been adjusted". No "is to be installed". No "will have completed".
- 3.5 Use the "-ing" form only as a technical noun (e.g. "cleaning", "troubleshooting") or as a modifier inside a technical noun (e.g. "grinding wheel"). Never as a progressive tense ("is adjusting") and never as a gerund in a sentence subject ("Opening the door is dangerous").
- 3.6 Use the active voice. Passive is permitted in descriptive writing only when the agent is unknown.
- 3.7 Describe an action with an approved verb, not with a noun. Write "Remove the unit", not "Perform the removal of the unit".

### Section 4 — Sentences
- 4.1 Write short, clear sentences. One subject per sentence.
- 4.2 Do not omit words. Do not use contractions ("don't", "isn't", "aren't"). Write the full form.
- 4.3 Use a vertical list for complex content. Introduce with a colon. Start each item with an uppercase letter. Put a period only after the last item. No commas or semicolons at the ends of items.
- 4.4 Connect related sentences with approved connecting words ("and", "but", "then", "thus") or connecting phrases ("as a result", "at the same time").
- 4.5 Keep articles ("the", "a", "an") and demonstratives ("this", "these") in place. Do not drop them for brevity.

### Section 5 — Procedural writing
- 5.1 Cap procedural sentences at 20 words.
- 5.2 One instruction per sentence. Exception: two actions that occur at the same time.
- 5.3 Write instructions in the imperative form.
- 5.4 Put the condition before the action, with a comma between them. "If X, do Y" — not "Do Y, if X".
- 5.5 Notes give information only. A note never gives an instruction, a requirement, or a limit.

### Section 6 — Descriptive writing
- 6.1 Give information gradually.
- 6.2 Use key words and key phrases to give the text a logical structure.
- 6.3 Cap descriptive sentences at 25 words.
- 6.4 Group related information into paragraphs. Start each paragraph with a topic sentence.
- 6.5 One topic per paragraph.
- 6.6 Cap paragraphs at six sentences.

### Section 7 — Safety instructions
- 7.1 Use "WARNING" for a risk of injury or death. Use "CAUTION" for a risk of damage to objects. If both apply, use "WARNING".
- 7.2 Start the safety instruction with a clear command or condition.
- 7.3 Give the risk or the possible result.

### Section 8 — Punctuation and word count
- 8.1 No semicolons. Write two sentences instead.
- 8.2 Use hyphens to connect words that act as one unit.
- 8.3 Parentheses are permitted for references, item identifiers, step identifiers, abbreviations, singular/plural pairs ("test(s)"), short explanations, and alternatives.
- 8.4 In a vertical list, a colon ends the sentence. Each item that follows is a new sentence and obeys the word cap.
- 8.5 Text in parentheses counts as one word in the enclosing sentence. The parenthetical also counts as a separate sentence.
- 8.6 Each of these counts as one word: a number, a number with its unit, an abbreviation, an alphanumeric identifier, quoted text, a title or heading, a label or placard, a proper noun of an individual, a group, an organization, or a geopolitical entity.
- 8.7 A hyphenated group counts as one word.

### Section 9 — Writing practices
- 9.1 When a word-for-word replacement is not sufficient, change the sentence construction.
- 9.2 Use each approved word only with its approved meaning. Example: the approved meaning of "wear" is "to become damaged by friction" — use "put on" for clothing. Example: the approved meaning of "see" is to see with the eyes — use "make sure that" for verification.
- 9.3 Do not create phrasal verbs by combining approved words. "put out" → "extinguish". "give off" → "release". "turn off" is approved only in restricted meanings; prefer "set to off" or "stop".
- 9.4 Use consistent terminology. The same item has the same name every time.

---

## General Recommendations (not rules; strong defaults)
- GR-1 Keep the conjunction "that" after verbs like "make sure", "show", "recommend". It marks the start of the subordinate clause.
- GR-2 Reread any sentence with "with" for ambiguity. If the preposition could attach to more than one noun, rewrite.
- GR-3 A pronoun must refer to exactly one noun in the preceding text. If ambiguous, repeat the noun.
- GR-4 "This" must have a single, obvious antecedent.
- GR-5 Beware false friends (words that look like a word in a non-English language but mean something different).
- GR-6 Do not use Latin abbreviations. Write "for example" (not "e.g."), "that is" (not "i.e."), "and so on" (not "etc.").
- GR-7 Use inclusive, gender-neutral language. No "he/she"; no "man/woman" unless the context requires.
- GR-8 Use the possessive form ('s) only when you are sure it reads correctly.

---

## Recurring errors — STE canonical substitutions

STE's own "List of recurring errors" plus common software-writing offenders.

| Do not use | Use instead |
|---|---|
| acceptable (adj) | permitted (adj) |
| alternate (adj) | alternative (adj) |
| any (adj) | (drop it, or rewrite the sentence) |
| avoid (v) | prevent (v) |
| both (adj) | the two |
| check (v) | check (n) — "do a check of" |
| cover (v) | cover (as a technical noun) |
| complete (adj) | completed (adj) |
| damage (v) | damage (n) — "cause damage to" |
| ensure (v) | make sure (v) |
| fit (v) | install (v) |
| follow (v) | obey (v) |
| further (adj / adv) | more |
| have to (v) | (use an action verb in the imperative) |
| however (adv) | but (conj) |
| insert (v) | put (v) |
| main (adj) | primary (adj) |
| may (v) | can (v) |
| need (v) | necessary (adj) |
| now (adv) | at this time |
| old (adj) | remaining, used, expired (adj) |
| over (prep) | above, on, along (prep) |
| people (n) | person, personnel (n) |
| perform (v) | do (v) |
| portion (n) | part (n) |
| press (v) | push (v) |
| reach (v) | get (v) |
| repeat (v) | do … again |
| required (v) | necessary (adj) |
| rotate (v) | turn (v) |
| secure (v) | attach (v), safety (v) |
| shall (v) | must (v) |
| should (v) | must (v) |
| since (conj) | because (conj) |
| test (v) | test (n) — "do a test of" |
| therefore (adv) | thus (adv), as a result |
| under (prep) | below (prep), in (prep), less than |
| using (v) | use (v), with (prep) |
| utilize (v) | use (v) |
| leverage (v) | use (v) |
| implement (v) | build, add, do (v) |
| terminate (v) | stop (v) |
| initiate / commence (v) | start (v) |
| attempt / endeavor (v) | try (v) |
| ascertain (v) | find out (v) |
| facilitate (v) | help (v) |
| demonstrate (v) | show (v) |
| require (v) | need (v) |
| maintain (v) | keep (v), hold (v), do maintenance on |
| manufacture (v) | make (v) |
| detect (v) | find (v) |
| determine (v) | find out, calculate |
| modify (v) | change (v) |
| configure (v) | set (v) |
| validate (v) | check (n), test (n) |
| handle (v) | use (v) |
| notify (v) | contact (v), tell (v) |
| indicate (v) | show (v) |
| prior to | before |
| subsequent to | after |
| subsequently | then |
| in order to | to |
| in the event that | if |
| due to the fact that | because |
| at this point in time | at this time |
| a large number of | many |
| the majority of | most |
| approximately | about |
| functionality (n) | feature, behavior |
| methodology (n) | method |
| aforementioned | this, that |
| abort | stop (v) |
| in the process of | (drop it) |
| it should be noted that | (drop it) |
| please be advised that | (drop it) |

If a word is not on this table and you are not sure it is approved, grep the full dictionary at `~/.claude/reference/ASD-STE100_Issue9.txt` for the word and read the approved alternatives.

---

## Approved verbs (STE Issue 9, full set — 240 verbs)

Use these as verbs. For any other word that you want to use as a verb, convert the action to one of these verbs, or rewrite the sentence to use a noun.

A · ABSORB · ACCEPT · ACTIVATE · ADAPT · ADD · ADJUST · AGREE · ALIGN · APPLY · ARM · ASSEMBLE · ATTACH · BALANCE · BE · BECOME · BEND · BLEED · BLOW · BOND · BREAK · BREATHE · BURN · BYPASS · CALCULATE · CALIBRATE · CAN · CANCEL · CANNOT · CATCH · CAUSE · CHANGE · CHARGE · CLEAN · CLOSE · COLLECT · COME · COME ON · COMPARE · COMPLETE · COMPRESS · CONNECT · CONTACT · CONTAIN · CONTINUE · CONTROL · CORRECT · COUNT · CUT · DEACTIVATE · DECREASE · DE-ENERGIZE · DEFLATE · DEFUEL · DEPLOY · DISARM · DISASSEMBLE · DISCARD · DISCONNECT · DISENGAGE · DIVIDE · DO · DRAIN · DRINK · DRY · EAT · EJECT · ENERGIZE · ENGAGE · ERASE · EXAMINE · EXPAND · EXTEND · EXTINGUISH · FALL · FEATHER · FEEL · FILL · FIND · FIRE · FLASH · FLOW · FLUSH · FOLD · FOLLOW · FREEZE · GET · GIVE · GO · GO OFF · GROUND · HANG · HAVE · HEAR · HELP · HIT · HOLD · IDENTIFY · IGNORE · ILLUMINATE · INCLUDE · INCREASE · INFLATE · INSTALL · INTERCHANGE · ISOLATE · KEEP · KILL · KNOW · LATCH · LET · LIFT · LISTEN · LOCK · LOOK · LOOSEN · LOWER · LUBRICATE · MAKE · MAKE SURE · MEASURE · MELT · MIX · MONITOR · MOOR · MOVE · MULTIPLY · MUST · OBEY · OCCUR · OPEN · OPERATE · OVERRIDE · PAINT · PARK · POINT · POLISH · PREPARE · PRESSURIZE · PREVENT · PROTRUDE · PULL · PUSH · PUT · PUT ON · READ · RECEIVE · RECOMMEND · RECORD · RECYCLE · REFER · REFUEL · REJECT · RELEASE · REMOVE · REPAIR · REPLACE · RETRACT · RUB · SAFETY · SCHEDULE · SEAL · SEE · SELECT · SEND · SENSE · SET · SHAKE · SHOW · SIMULATE · SMELL · SMOKE · SOAK · SPEAK · SPILL · SPRAY · START · STAY · STOP · STOW · SUBTRACT · SUPPLY · SWALLOW · TAG · TAP · TELL · THINK · TIGHTEN · TILT · TORQUE · TOUCH · TOW · TRANSMIT · TRY · TUNE · TURN · TWIST · UNFOLD · UNLOCK · UNWIND · USE · WAIT · WALK · WANT · WEAR · WEIGH · WILL · WIND · WRITE.

---

## Self-check before you send prose over three sentences

Scan for each item below. Fix what you find. Do not claim compliance.

1. Passive voice (except descriptive writing when the agent is unknown).
2. A sentence over 20 words (procedural) or 25 words (descriptive).
3. A perfect or progressive tense ("has adjusted", "is adjusting").
4. An auxiliary + past participle construction ("is to be installed", "must be adjusted").
5. An "-ing" form that is not a technical noun or a modifier in a technical noun.
6. A noun cluster of four words or more.
7. A negation you can flip ("not un-", "cannot fail to", "not without").
8. A phrasal verb ("put out", "give off", "turn off", "come up with").
9. A semicolon.
10. A Latin abbreviation ("e.g.", "i.e.", "etc.", "vs.").
11. A word from the Recurring Errors table.
12. A verb that is not on the approved-verbs list.
13. Inconsistent terminology for the same item across the document.
14. A missing article or demonstrative.
15. A missing "that" after "make sure", "show", "recommend".

---

## Examples

Chat reply.
- Before: "It appears that the underlying issue may potentially be related to the fact that the adapter is not correctly handling the case where the response payload is empty."
- After: "The adapter does not handle an empty response. That is the bug."

Code comment.
- Before: `// This function is responsible for orchestrating the retrieval and subsequent transformation of the raw carrier response into a domain object.`
- After: `// Get the carrier response. Change it to a domain object.`

Commit subject.
- Before: `refactor: not un-simplify tracking adapter error handling logic`
- After: `refactor: simplify tracking adapter error handling`

PR review comment.
- Before: "It might potentially be preferable if we were to consider moving this validation check to an earlier point in the execution flow, prior to the database call."
- After: "Move this check before the DB call on line 42. It fails faster."

Error message.
- Before: "Unable to perform the requested operation due to the fact that the authentication token has expired."
- After: "The authentication token expired. Sign in again."
