---
type: outline
title: "What is an embedding? (and what do dimensions actually mean)"
status: outline-revised
timestamp: 2026-10-27
format: youtube-short
---

# Video outline

Scope, viewer, and open decisions live in [brief.md](brief.md).

**Working title:** What is an embedding, really?

**Alternative titles:**

- Your embedding has 1024 dimensions. What's in each one?
- Embeddings explained with Star Wars
- Luke, Vader, and the vector space
- What does "1024 dimensions" actually mean?

## Hook: the number nobody explains

Your embedding model turns every piece of text into a list of numbers. For example, jina-embeddings-v5-text gives you 1024 of them.

What is each one of those numbers actually doing?

[on-screen: a long scrolling vector `[0.021, -0.443, 0.187, ...]` with "1024 dimensions" stamped over it]

---

## What an embedding is

- An embedding is a list of numbers that represents the meaning of something, such as a chunk of text, an image, or a video.
- An embedding model produces it. Your data goes in, and a vector comes out.
- Things with similar meaning get similar vectors, so they end up close together.
- That's what makes semantic search work. Search for "young rebel pilot" and the closest match is the description of Luke Skywalker, even if it never uses those exact words.
  [simple animation: text snippets go into a model box and come out as vectors that land near each other; Luke highlighted]

---

## What a dimension is: the Star Wars space

- A dimension is a single number in that list. In our chart, each dimension scores one characteristic.
- Here we have a 2-dimensional space with two characteristics: humanity and realism.
- Every character gets a score for each one.
  [animate characters dropping onto the chart one at a time]
- Luke lands high and left: human, realistic.
  [highlight Luke]
- Darth Vader lands in the opposite corner: more machine than man.
  [highlight Vader; draw a line between Luke and Vader to show how far apart they are]
- Characters that are alike sit close together.
  [highlight Leia next to Luke]
- Characters that aren't sit far apart.
  [highlight Luke and Vader together]
- How close they are is what vector search looks at.

---

## Real models: from 2 to 1024

- Real embedding models don't stop at 2. Most use hundreds to thousands of dimensions.
  [zoom out from the 2D chart; more axes fan out until it becomes an abstract cloud of points]
- The model learns these features itself during training. Humans don't define them.
- Unlike the Star Wars chart, a single real dimension rarely maps to one clean concept like "human vs machine". Meaning is spread across many dimensions at once.
- More dimensions can capture more subtle differences. They also cost more storage and more compute per comparison.
  [on-screen: "more dims → more nuance, more storage"]

---

## Payoff and CTA

- You can plot 2 dimensions on a chart. The model works across a thousand.
  [return to the 2D chart, then cut to the 1024-number vector from the hook to close the loop]
- But more dimensions isn't automatically better. Test the model on your own data.
- If you want to know how that gets searched at scale, follow the Elastic YouTube channel. Bye for now!
  [end on the Elastic logo; end card links to the next vector search video]

---

# Visual assets needed

Designer deliverable:

- **What is a dimension? infographic, vertical 9:16:** reframe the existing asset with layered exports (axes, labels, each character separately) so characters can animate in.
  - Design source: https://claude.ai/design/p/6949ef24-c4bd-435d-9ccb-76b9dec49195?file=What+is+a+dimension+infographic.html&via=share
  - PNG: https://drive.google.com/file/d/1aJEkAzdGj0Cd5D4KyLUdUzAcUHhY-fo-/view?usp=drive_link

Editor-time (noted inline above, not designer tasks):

- Text → model → vector animation
- 2D → many-dimensions zoom-out
- Scrolling vector for the hook and closing callback
- Burned-in captions

# Review notes

- The social copy says Vader sits "orthogonally" to Luke. In the chart he's in the opposite quadrant, which is closer to *opposite* than orthogonal (orthogonal would be a 90° angle). The narration says "opposite corner" and "how close they are" to avoid both the orthogonal claim and a distance-only claim. Cosine similarity compares angle, not distance.
- "Each dimension scores a single learned feature" is a useful simplification for the 2D example. The Real models section adds the caveat that real dimensions aren't individually interpretable, so the Short doesn't teach a misconception.
- Luke is on the chart, so the search example uses him instead of Solo.
- Pre-recording checks (axis labels, character placements, the "young rebel pilot" example, dimension-range wording) are tracked under Open decisions in [brief.md](brief.md).

# Source references

Full list in [brief.md](brief.md). The two most useful for the editor:

- Social copy doc, Post 4 (W/C 6th July 2026): https://docs.google.com/document/d/1fdSdCsnsOMWREEgHHikmSZEC644BTvBjZwtbOcobXXc/edit?tab=t.0
- Elastic: What is a vector embedding?: https://www.elastic.co/what-is/vector-embedding
