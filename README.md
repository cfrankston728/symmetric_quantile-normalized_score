# symmetric_quantile-normalized_score
``symmetric_quantile-normalized_score`` is an implementation of symmetric quantile-normalized score voting (SQNV).

## Introduction
Invented by Connor Frankston on March 16, 2024, with significant contributions from the community at the [Voting Theory Forum](https://www.votingtheory.org/forum/), SQNV offers a novel approach to score voting by incorporating a symmetric quantile normalization process. This method aims to mitigate the impacts of strategic voting tactics like bullet voting and min-maxing. It's important to note that while SQNV brings several advantages to score voting systems, it is not Condorcet compliant for contests involving more than three candidates.

## About SQNV
Symmetric quantile-normalized score voting (SQNV) is a voting system that modifies traditional score voting to enhance fairness and reduce susceptibility to common voting tactics. At its core, SQNV employs a normalization technique that adjusts voters' scores for candidates, ensuring that each ballot contributes equally to the final outcome, regardless of the scoring range used by each voter.

### Process Overview

1. **Normalization**: Each voter's scores are normalized to a 0-1 scale, maintaining the relative preferences but standardizing the score ranges across all ballots.
2. **Quantile Ranking**: Scores on each ballot are ranked, and a quantile calculation is performed to determine the mean score for each rank across all voters.
3. **Symmetric Adjustment**: The quantile scores are then adjusted symmetrically, ensuring that the influence of high and low scores is balanced across the voting population.
4. **Tallying**: The adjusted scores are tallied for each candidate, determining the winner in a way that respects the nuanced preferences of the entire electorate.

This approach not only counters strategic voting behaviors like bullet voting and min-maxing but also respects the subtleties of voter preferences by preserving the integrity of weakly-ranked candidates' scores.

## Features

- Mitigates effects of strategic voting.
- Balances score and rank-based voting methods' advantages.
- Enhances fairness in score distribution among candidates.

## Acknowledgments

A special thanks is extended to Jack Waugh and Toby Periera for their insightful intellectual engagement and concerns pertaining to the development of this system.