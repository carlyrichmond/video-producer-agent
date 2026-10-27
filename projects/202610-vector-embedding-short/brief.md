---
type: brief
title: "What is an embedding? (and what do dimensions actually mean)"
status: outline-revised
timestamp: 2026-10-27
format: youtube-short
---

# Brief

## Viewer

A developer who has used or seen an embedding model, or is about to, but treats the output as an opaque list of numbers. They may be new to vector search.

## Job of the video

After watching, the viewer can say: **"A dimension is one learned score, and real models use hundreds or thousands of them, so meaning is spread across all of them."**

That is the single concept. The Short does not teach how to store, index, or query vectors.

## Promise

The title and hook ask what each number in a 1024-number embedding is doing. The Short answers that question using a 2D Star Wars chart, then explains why real models differ from the chart.

## Scope boundaries

In scope:

- What an embedding is, in one sentence.
- What a dimension is, using the 2D Star Wars chart.
- Closeness as the idea behind semantic search.
- Why real dimensions aren't individually interpretable, and the cost of more of them.
- One closing takeaway: more dimensions isn't automatically better, so judge a model against your own data.

Out of scope (link forward, don't explain):

- Matryoshka dimensions (Post 1 of the social set).
- BBQ quantization and other ways to shrink vectors (Post 3).
- Storing vectors in Elasticsearch, index types, and similarity metrics.
- A full guide to choosing an embedding model. The takeaway line is a pointer, not a method.

## Format

- Vertical 9:16 YouTube Short, one idea, burned-in captions (most Shorts are watched muted).
- Reuses the "What is a dimension?" Star Wars asset from Post 4 of the W/C 6th July social copy, so the Short and the post reinforce each other.
- Length: roughly 1–2 minutes, about 200–300 spoken words. Past Elastic shorts on vector indexes ran 100–200 words, so treat this as the upper bound.

## Open decisions

- **Axis labels.** Confirm the chart's two axes and each character's placement against the infographic before scripting. The narration must describe the chart as drawn.
- **Hook model.** Decided: the hook names Jina Embeddings v5 (text-small, 1024 dimensions by default). Confirm on the model card before recording, and check whether a newer Jina model has shipped.
- **Follow-up link.** Decide which video the end card points to (the Vector Indexes Explained series, or a Matryoshka/BBQ Short once published).
- **Search example.** Check that "young rebel pilot" is a believable match for Luke's placement and for the description being embedded.

## Risks

- A viewer may take the 2D chart literally. The Real models section carries the correction and must stay in.
- "Hundreds to thousands of dimensions" is unsourced in the wiki. Cite model documentation if you want to be more specific.

## References

- [Outline](outline.md)
- [Developer Video Production Guidelines](../../wiki/developer-video-production-guidelines.md)
- [Script Structure Patterns — Short-Form](../../wiki/script-structure-patterns.md)
- Elastic docs, dense vector field type: https://www.elastic.co/docs/reference/elasticsearch/mapping-reference/dense-vector (max 4096 dims)
- Social copy doc, Post 4 (W/C 6th July 2026): https://docs.google.com/document/d/1fdSdCsnsOMWREEgHHikmSZEC644BTvBjZwtbOcobXXc/edit?tab=t.0
