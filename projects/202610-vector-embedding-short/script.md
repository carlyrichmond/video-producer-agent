---
type: script
title: "What is an embedding? (and what do dimensions actually mean)"
status: draft-v1
timestamp: 2026-10-27
format: youtube-short
source: outline.md
---

Your embedding model turns text into a list of numbers. Jina Embeddings v5 Text, for example, gives you one thousand and twenty four (1024) of them.
[on-screen: a long scrolling vector `[0.021, -0.443, 0.187, ...]` with "1024 dimensions" stamped over it]

So what do each of those numbers actually mean? Let's find out!

An embedding is a list of numbers that represents the meaning of something. For example, a chunk of text, an image, or a video.

You provide an embedding model your data as the input, and it outputs a vector.

Things with similar meaning get similar vectors, so they appear close together.
[simple animation: text snippets go into a model box and come out as vectors that land near each other]

That's what makes semantic search work. Search for "young rebel pilot", and the closest match is Luke Skywalker's description, even if our query doesn't use those exact words.
[highlight Luke]

So what's a dimension? It's a single number in that list.

Let's check out a simple 2 dimensional example: humanity and realism.
[show the 2D chart]

Every character gets a score for each one.
[animate Luke on a chart with his vector values appearing beside him, before the numbers disappear]

Luke lands high and left. Human, realistic.
[highlight Luke]

Darth Vader is in the opposite corner. More machine than man.
[highlight Vader; draw a line between Luke and Vader]

And Leia? Right next to Luke.
[highlight Leia next to Luke]

Characters that are similar sit close together. Characters that are not similar sit far apart.
[highlight Luke and Vader together]

How close together they are is what vector search looks at, using similarity measures such as cosine similarity or dot product.

Real models don't stop at two dimensions. They use hundreds, even thousands, of dimensions.
[zoom out from the 2D chart; more axes fan out until it becomes an abstract cloud of points]

People don't pick what those dimensions represent. The model learns them during training.

So unlike our chart, one real dimension rarely means one clean idea like "human versus machine". Meaning is spread across many dimensions at once.

More dimensions capture subtler differences. But they also cost more storage, and more compute for each comparison.
[on-screen: "more dims → more nuance, more storage"]

We can plot two dimensions on a chart. The model works across a thousand.
[return to the 2D chart, then cut to the 1024-number vector from the hook]

More dimensions isn't automatically better. Make sure you test a model out on your own data.

"That's what's inside an embedding. Follow the Elastic YouTube channel to see more about vector embeddings. Until next time!
[end on the Elastic logo; end card links to the next vector search video]