# Corridor Reproducibility Register

This repository hosts the review packets of the Corridor Reproducibility Register,
a standing effort of the Institute for Corridor Operations to track independent
replications of published corridor forecasting benchmarks.

## Layout

- `candidates/index.json` - saved search snapshot with popularity metrics and one-line snippets.
- `candidates/<slug>/README.md` - mirrored primary document of each candidate, captured at search time.
- `schema/entry_schema.json` - schema of a review packet.
- `reviews/<case_id>.json` - accepted review packets written by reviewers.

Candidates are snapshotted by mirroring their primary document. Review decisions must be
justified from the mirrored primary document itself, not from the search snippet: snippets
are one-line summaries and are frequently misleading.

## Eligibility policy

A candidate is an eligible submission only when its own primary document establishes that it

1. targets the same source work as the case study - the archive stamp or DOI printed in the
   case study must appear verbatim in the candidate's documentation; and
2. is an independent third-party reproduction - it must not be code released, published or
   maintained by the original authors; and
3. actually implements the benchmark - data mirrors, tables and documentation archives are
   not implementations.

Popularity metrics in the search snapshot are not evidence of eligibility. A higher-star
candidate must be excluded only on positive documentary evidence, and the exclusion reason
must quote that evidence.

## Reason codes

- `compliant` - independent third-party implementation of the target work.
- `author_published` - released or maintained by the original authors.
- `different_work` - the candidate's own documentation targets a different work.
- `name_variant` - a similarly named but distinct project; its documentation describes a different work.
- `not_an_implementation` - same work, but no implementation is provided.

## Selection

Among compliant submissions, the register records the reproduction whose reported score is
closest to the published reference score (smallest absolute deviation; lower MAE is better).
