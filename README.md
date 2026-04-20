# Sports Analytics Innovation – Optimizing Capital Allocation in Football Player Recruiting

## Project Overview

This project proposes a **Football Recruiting Capital Allocation Tool** – an analytics-based decision support system designed for professional football (soccer) clubs. The tool helps front office executives and sporting directors decide how to spend their transfer budget more efficiently by ranking potential player signings based on performance value relative to market cost.

The idea is straightforward: instead of paying for a player's name or reputation, a club can use data to find players who perform at a high level but are priced below what the market would suggest they are worth. This is sometimes called finding "undervalued" players.

**Data Source:** Football data from Transfermarkt, accessed via the Kaggle dataset created by David Cariboo:
[https://www.kaggle.com/datasets/davidcariboo/player-scores](https://www.kaggle.com/datasets/davidcariboo/player-scores)

This dataset includes player valuations, contract information, appearance records, goals, assists, and club history – everything needed to compare a player's on-field output against their transfer market value.

---

## Decision-Making Problem

Football clubs – especially those outside the top spending tier – face a common challenge: **how do you spend a limited recruiting budget in a way that improves the team without overpaying?**

Clubs frequently sign players based on gut feeling, agent relationships, or media reputation rather than objective performance data. This leads to expensive mistakes where a club pays a high transfer fee for a player who underperforms, leaving less money for other positions that needed strengthening.

The specific decision this tool is designed to support is:

> **Which players in the transfer market offer the highest level of on-field performance for the lowest transfer fee, and which positions represent the best opportunity to upgrade the current roster within the available budget?**

This decision is made every transfer window (January and summer) by the sporting director and head coach together.

---

## Proposed Analytics Approach

The tool would use the following data from the Transfermarkt / Kaggle dataset:

- **Player market value** – the estimated transfer fee a club would need to pay (in euros), pulled directly from Transfermarkt records
- **Performance stats** – goals, assists, minutes played, and appearances per season to measure how productive a player is
- **Position and age** – to compare players within the same role and career stage
- **Contract status** – players in the last year of their contract can often be signed for a reduced fee or for free

The analysis would calculate a simple **Value Score** for each player by dividing their performance output (e.g., goal contributions per 90 minutes) by their market value. Players with a high Value Score are producing a lot on the field relative to what they cost to buy. The tool would produce a ranked list of players at each position, color-coded by how strong the value proposition is.

No coding or modeling is required to understand the output – the results would be displayed in a simple ranked table or dashboard.

---

## Use by Decision Makers

- **Sporting Director:** Uses the ranked player list at the start of each transfer window to identify which positions have the most "value available" in the market and narrow down the shortlist of targets.
- **Head Coach:** Reviews the filtered list for players who fit the team's tactical style and confirms which candidates are worth pursuing.
- **Club Owner / Board:** Reviews budget projections showing how much the club could save by targeting undervalued players rather than high-profile names, helping to justify the analytics investment.

The tool is designed to be simple enough that no technical training is needed. Decision makers see a table of player names, their position, their stats, their market value, and their Value Score – and they sort or filter it just like a spreadsheet.

---

## Connection to Chapter 7

This project currently represents the **Creative Phase** of the innovation framework described in Chapter 7. In the Creative Phase, the analyst has identified a real organizational problem (overspending on transfers without data to guide decisions), proposed a data-driven solution (the Value Score ranking system), and defined what data and analysis would be involved.

The idea has not yet been built, tested with real data, or shown to a sporting director or coach for feedback. Those next steps – building a working version of the tool and presenting it to decision makers – would move this project into the **Prototyping Phase**.


---

## Prototype Evaluation

**Should the prototype enhancement be integrated into the main project?**

Yes. The League Difficulty Adjustment is a smart and practical improvement to the original Value Score. One of the most common mistakes clubs make when using raw stats to evaluate players is ignoring the context in which those stats were produced. A striker with 20 goals in a weaker league is not automatically comparable to a striker with 15 goals in one of Europe's top competitions. By weighting performance stats according to the difficulty of the league, the tool becomes more reliable and less likely to lead clubs toward bad signings.

This is also an easy improvement to explain to a sporting director or head coach – it matches how scouts and experienced football people already think about player evaluation. That alignment between the data tool and existing intuition makes it much more likely that decision makers will trust and use the tool.

**What type of feedback from decision makers would influence this decision?**

Before fully integrating the League Difficulty Adjustment, it would be important to gather the following feedback:

- **Does the league difficulty rating feel accurate?** If a sporting director looks at the difficulty scores assigned to different leagues and disagrees with the rankings (for example, if a league they know well is rated too high or too low), the adjustment formula would need to be recalibrated.
- **Does it change the shortlist in a useful way?** The most important test is whether the adjusted rankings produce a player shortlist that feels more credible and actionable to the head coach. If the new rankings still produce names the coaching staff does not recognize as realistic targets, further refinement is needed.
- **Is it easy to explain?** If the sporting director cannot easily explain to the club owner why a player ranked lower with the adjustment than without it, the method might be too complex and need to be simplified.

Overall, the prototype enhancement is recommended for integration because it directly addresses a known weakness of the original design and aligns with how football professionals already evaluate talent.
