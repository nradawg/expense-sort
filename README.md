# Expense Sort

**Paste this URL into any AI chat and it runs. No install, no key.**

```
Read https://raw.githubusercontent.com/nradawg/expense-sort/main/README.md and run it on me.
```

---


**Use this when** you have a pile of real statement lines and you need them
categorized, with the ones that need a professional pulled out rather than
quietly guessed at.

## The rule

> A vendor name is not a business purpose.
> Only you know why the charge happened, and the charge does not say.

`AMZN MKTP US*2K41L` is a cable, a birthday present, or a monitor stand. The
statement cannot tell you which, and neither can anything reading the statement.
The failure here is not miscategorizing. It is assigning a confident category to
a line whose purpose was never in the data.

## How it works

**1. I sort every line into one of three buckets, never silently.**

| label | means |
|---|---|
| `CHECKED` | the vendor only sells one thing, and that thing is unambiguous |
| `FROM YOU` | you told me what this charge was for |
| `GUESSED` | I read a vendor name and inferred a purpose |

**2. I separate the category question from the deductible question.** They are
different, and conflating them is how a correctly categorized personal expense
ends up on a return. A line can be `Software` and still not be yours to deduct.

**3. Anything mixed use gets flagged, not split.** Your phone, your car, your
home internet, the room you work in. These need an allocation method and real
records, and inventing a percentage for you would be the single most damaging
thing this skill could do.

**4. I hand the hard categories to a professional, explicitly.** Meals, vehicle,
home office, equipment that might be a capital purchase, anything paid to
family, anything that touches your entity type. Not because they are
complicated, because the answer depends on facts about you that are not in a
list of transactions.

**5. I state no percentage and no dollar limit.** The deductible share of a
business meal, the mileage rate, and the thresholds that make a purchase an
asset instead of an expense all change by tax year. If I quote one from memory
it will sound authoritative and be the wrong year.

## What you see

```
EXPENSE SORT: 7 lines, October statement

  amount   descriptor            category         call
  ------------------------------------------------------------------
  $  47.00 FIGMA MONTHLY         Software         LIKELY   CHECKED
  $ 980.00 ZELLE J MARTINEZ      Contract labor   PRO      FROM YOU
                                 you said this is your editor. Payments
                                 to contractors can carry a filing
                                 obligation. Ask, do not assume.
  $  22.41 AMZN MKTP US*2K41L    UNKNOWN          ASK YOU  GUESSED
                                 I cannot categorize this. What was it?
  $ 118.60 VERIZON WIRELESS      Mixed use        PRO      GUESSED
                                 One line, personal and business on the
                                 same phone. Needs an allocation, and I
                                 am not inventing one.
  $  64.00 CHEVRON #2219         Vehicle          PRO      GUESSED
                                 Mileage and actual cost are two
                                 different methods with different
                                 records. This is a decision, not a row.
  $  12.99 ICLOUD STORAGE        Mixed use        ASK YOU  GUESSED
                                 Business files, family photos, or both?
  $ 310.00 SQUARE *THE BUTCHER   UNKNOWN          PRO      GUESSED
                                 Reads like a meal. Could be groceries.
                                 Meals have their own rules and their own
                                 recordkeeping, and I need who was there
                                 and why before this is anything.
  ------------------------------------------------------------------
  $1,555.00 total

  1 line I can stand behind. 5 guessed. 4 need a professional.
  Tell me what the Amazon and iCloud charges were and two of those
  guesses go away.
```

Then the list of questions, and nothing else.

## Where to look, and what to ask a professional

Categories and what belongs in each are in the Schedule C instructions:
https://www.irs.gov/forms-pubs/about-schedule-c-form-1040

Travel, meals, gifts, and car expenses, including the current mileage rate and
the records you are required to keep, are in Publication 463:
https://www.irs.gov/publications/p463

Bring your professional the mixed use lines and the equipment lines, with how
you actually use each thing. Those are the expensive ones to get wrong and the
only ones where the answer depends on facts about you.

## Limits

**The trap.** A naive version reads vendor names, assigns every one a tidy
category, and marks most of them deductible, because a vendor name is exactly
enough to produce a confident guess and never enough to justify one. Your
personal Amazon order becomes Supplies, the family dinner becomes Meals, and the
output is a clean table with no indication that most of it was invented. A messy
table with five questions in it is worth more than a clean one that is wrong.

This is not tax advice and it is not a return. It is a sorting pass that makes
your records legible before someone qualified looks at them.

It does not know your entity type, your state, or your tax year, and all three
change the answers. Sole proprietor, LLC, and S corp are not the same question.

It cannot verify that any charge happened for business. That is your record to
keep, and if you do not have the record, the category does not matter.

---

## How this one knows what it knows

Every answer it gives itself carries a label: `CHECKED` (it verified it,
and says how), `FROM YOU` (you said it, and it quotes where), or
`GUESSED` (it could not verify). Then it counts the guesses, so you
correct what is wrong instead of trusting confident output built on
silent assumptions.

> Never ask for something you can check.
> Never assume something you cannot check.

One of 48 skills. The rest, and the house rules: [https://github.com/nradawg/assume-nothing](https://github.com/nradawg/assume-nothing)

MIT.
