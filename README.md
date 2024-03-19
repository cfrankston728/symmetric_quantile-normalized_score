# symmetric_quantile-normalized_score
``symmetric_quantile-normalized_score`` is an implementation of symmetric quantile-normalized score voting (SQNV).

<figure>
    <img src="symmetric_quantile_normalization.png" alt="" title="Visual_Plot" width="450"/>
</figure>

## Introduction
Invented by Connor Frankston on March 16, 2024, with significant contributions from the community at the [Voting Theory Forum](https://www.votingtheory.org/forum/), SQNV offers a novel approach to score voting by incorporating a symmetric quantile normalization process. This method aims to mitigate the impacts of strategic voting tactics like bullet voting and min-maxing. It's important to note that while SQNV brings several advantages to score voting systems, it is not Condorcet compliant for contests involving more than three candidates.

## About SQNV
Symmetric quantile-normalized score voting (SQNV) is a voting system that modifies traditional score voting to enhance fairness and reduce susceptibility to common voting tactics. At its core, SQNV employs a normalization technique that adjusts voters' scores for candidates, ensuring that each ballot contributes equally to the final outcome.

### Process Overview

1. **Normalization**: Each voter's scores are normalized to a 0-1 scale, maintaining the relative preferences but standardizing the score ranges across all ballots.
2. **Quantile Ranking**: Scores on each ballot are ranked, and a quantile calculation is performed to determine the central score (ex: mean or median) for each rank across all voters.
3. **Symmetric Adjustment**: The quantile scores are then adjusted symmetrically, ensuring that the influence of high and low scores is balanced across the voting population.
4. **Tallying**: The adjusted scores are tallied for each candidate, determining the winner in a way that respects the nuanced preferences of the entire electorate.

This approach counters strategic voting behaviors like bullet voting and min-maxing while respecting the subtleties of normative voter preferences.

## Motivation
SQNV is motivated by the goal to enable reasonable normalization of score ballots to enhance comparability across voters without (1) resorting to strict rankings or (2) sacrificing the desirable properties of score systems, such as participation and consistency. SQNV accomplishes this by a adjusting quantile normalized score values into a forced symmetry that preserves the following "cancellation" property:

* **Cancellation**: If an election would arrive to a definite resolution in the absence of ballots from voters A and B, then for any ballot voter A casts that alters that resolution, there must be some ballot that voter B can cast to recover the original resolution.

There are methods to trivially satisfy this property, such as [password attacking](https://www.votingtheory.org/forum/post/3256), but not without infringements on a reasonable balance between privacy and transparency. In the case of SQNV, the cancellation property is maintained by preserving the richer Abelian group, "point-summing" structure of traditional score ballots, which offers the advantage of the reinforcement criterion and therefore also the participation criterion. This places SQNV among score and approval voting in the "map" of voting systems.

<figure>
    <img src="map_of_voting_systems.png" alt="" title="Map_of_Voting_Systems" width="450"/>
</figure>

## Features

- Mitigates effects of strategic voting.
- Balances score and rank-based voting methods' advantages.
- Enhances fairness in score distribution among candidates.

## License

This project, "Symmetric Quantile Normalized Score," is licensed under the Creative Commons Attribution 4.0 International License - CC BY 4.0. This license allows others to share, copy, distribute, transmit, and adapt the work, even commercially, as long as proper attribution is given to the original author, Connor Frankston.

For the full license text, please see the [LICENSE.md](LICENSE.md) file in this repository or visit the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/legalcode) page.

![Creative Commons License](https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1) ![Attribution License](https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1)


## Acknowledgments

A special thanks is extended to Jack Waugh and Toby Periera for their insightful intellectual engagement and concerns pertaining to the development of this system.