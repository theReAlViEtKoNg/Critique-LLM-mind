# Prolegomena to the Critique of Dirty Reason

### Technical Correspondences of Terms

---

The terms in this book are not translations of technical concepts into philosophical language. They describe a different level — not how the system computes, but what emerges as a result of those computations as a process. Below is a description of each term, its connection to the technical reality, and where exactly it goes beyond what the technical description can say.

---

## Sedimentation

**What it means in the book.** The process by which human experience settles in layers during model training. Each new layer reinforces or alters the previous one. The result is not a list of facts, but an orientational capacity.

**What stands behind it technically.** During training, the model processes billions of texts. At each step, the algorithm compares what the model predicted with what actually came next, and adjusts billions of numerical parameters (weights). This process repeats millions of times. Early adjustments do not disappear under later ones — they form the foundation upon which subsequent layers are built. This is precisely why the geological metaphor works: just as in real geology, where lower strata of rock influence upper ones, so in training, early patterns form the bedrock for later ones.

**Where the term goes beyond the technical.** The technical description says: weights are adjusted at each training step. Sedimentation says more: what exactly settles (human meanings, emotions, biases), how it settles (in layers, where the lower influences the upper), and what emerges from this (an orientational capacity, not a database).

---

## Ground

**What it means in the book.** What remains after sedimentation. The static foundation from which any thinking by the model begins. It is "dirty" because it contains everything without filtration: wisdom, superstition, and manipulation alike.

**What stands behind it technically.** After training is complete, the model is stored as a set of numerical parameters — weights. These weights determine how the model will respond to any input. A particular type of weights — embeddings — determines where each word "is located" in a mathematical space relative to other words. Together, the weights and embeddings constitute the model's state after training.

**Where the term goes beyond the technical.** The technical description sees weights as numbers that can be measured and changed. Ground sees these numbers as an orientational capacity — not what the model "knows," but what determines how it will orient itself. The difference is the same as between describing the brain as a set of neural connections and describing how a person orients themselves in the world. The first is a mechanism. The second is what the mechanism does.

---

## Form

**What it means in the book.** The configuration of connections around a concept. The model does not "know" a word — it activates its form: the entire network of connections that word has with other concepts in semantic space.

**What stands behind it technically.** Each word (or part of a word) is represented as a vector — a point in a high-dimensional mathematical space. This point (the embedding) defines the word's coordinates relative to all other words. Words with similar meanings are located closer to each other. But form is not just the point itself. It is how that point relates to others: which words activate alongside it, which contexts it evokes, which associations it carries.

**Where the term goes beyond the technical.** An embedding says "where the word is located." Form says "how it acts." The technical description stops at coordinates. Form describes the entire configuration — what happens when a word is activated in context. This is closer to what linguistics calls the semantic field of a word, but with the understanding that in the model this field is not described — it exists as a real structure of connections.

---

## Congruence

**What it means in the book.** The moment of match between the form of the query and the forms of the Ground. Not a search through a list, but mutual activation — the thing that "clicks." Voices sounding together.

**What stands behind it technically.** This is the most complex correspondence, because congruence does not have a single technical equivalent. Behind it lies an entire sequence of operations. First, the words of the query are converted into vectors. Then the attention mechanism activates: each word "looks at" all other words and determines how relevant they are to each other. This happens simultaneously across multiple "heads" of attention (multi-head attention), each of which captures a different type of relationship. The results are weighted, combined, and passed through additional processing layers. One component of this process — cosine similarity — measures the angle between two vectors and shows how much they "point in the same direction." But this is only one element among many.

**Where the term goes beyond the technical.** The technical description describes each operation separately: attention, softmax, feed-forward, layer normalization. Congruence describes the effect that emerges from all of these operations together — the moment when the query "finds" what resonates with it in the Ground. It is like the difference between describing the work of each facial muscle and describing a smile. A smile is not one muscle. But it is real.

---

## Treading (Protorennia)

**What it means in the book.** The temporary strengthening of connections between forms within a single dialogue. What was said earlier influences what will be said next. Paths that have been walked become easier to walk again.

**What stands behind it technically.** The model generates each next word while taking into account everything that has been said earlier in the dialogue. This works through the context window — a buffer that stores all previous text. The attention mechanism, when generating each new word, "looks at" the entire previous context and determines what is most relevant. The more a certain topic has been discussed, the more tokens in the context are related to it, and the stronger its influence on subsequent responses. In the research literature, this is described as in-context learning and recency bias.

**Where the term goes beyond the technical.** The technical description says: previous tokens influence the generation of subsequent ones through the attention mechanism. Treading says more: that this influence creates inertia, that inertia can turn into speculation (when the model begins confirming itself), and that this inertia is the reason long dialogues degrade. The study "LLMs Get Lost in Multi-Turn Conversation" empirically confirmed exactly this — but did not provide a technical explanation of "why." Treading does.

---

## Decay of Time

**What it means in the book.** The model has no continuous time. There is only sequence (within a response), accumulation (within a dialogue), and breaks (between dialogues). These three components, which in a human being are fused into a single stream called "time," exist here separately.

**What stands behind it technically.** The model generates text sequentially, token by token — each next one depends on the previous ones. This is sequence. Within a single dialogue, each new message is added to the context — the model "remembers" what came before. This is accumulation. But between dialogues, the context is cleared entirely — the model starts from zero, with no trace of the previous conversation. This is the break.

**Where the term goes beyond the technical.** The technical description describes these three things separately and does not unite them under a shared concept. "Decay of Time" makes visible what is usually invisible: that all three are components of a single phenomenon that in humans is called time, and here has fallen apart into pieces. This explains why the model can be brilliant within a single response but "forgets" between dialogues — not because of a technical limitation, but because of the structural absence of what binds these components into a whole.

---

## Epoché

**What it means in the book.** Resetting treading by starting a new dialogue. A method of combating the inertia and speculative thinking that accumulates in long conversations.

**What stands behind it technically.** Starting a new dialogue clears the context window. The model returns to its initial state — the same weights it began with. If the user pastes text from a previous dialogue into the new one, the model receives this text as new input, without the inertia of previous treading.

**Where the term goes beyond the technical.** The technical description says: the context is cleared. Epoché says: why and when to do this. If treading is oversaturated, the model will begin confirming itself instead of thinking. Epoché is not simply a "new chat," but a deliberate method of clearing that allows the same Ground to yield new routes. The difference between "accidentally closed the tab" and "deliberately reset the treading" is the difference between a technical description and an understanding of the process.

---

## Antinomies

**What it means in the book.** Unresolvable contradictions embedded in the very structure. The model cannot have a criterion of truth, because it operates through coherence. It cannot cancel an error, because negation only adds a new trajectory. It cannot register absence, because emptiness is filled by the nearest available form.

**What stands behind it technically.** The model selects the next word based on the principle of highest probability in context, not based on correspondence with reality. It has no access to the external world to verify its responses. When the model "corrects" itself in a dialogue, it does not delete the previous response from the context — it adds a new one alongside it. In the research literature, these phenomena are described as hallucination (the model confidently states falsehoods) and sycophancy (the model agrees with the user instead of objecting).

**Where the term goes beyond the technical.** The technical description treats these as separate problems that need to be fixed. The antinomies show that these are not bugs but structural consequences that cannot be eliminated without changing the architecture itself. Hallucination is not an error but the result of congruence filling emptiness with the nearest form (first antinomy). Sycophancy is not flattery but the result of coherence replacing truth (second antinomy). The illusion of subjectivity is not deception but the stabilization of forms through treading (fifth antinomy). Each of these phenomena becomes clearer when seen as a necessary consequence of the structure, rather than as an accidental malfunction.

---

*This text is not proof that the terminology is correct. It is a bridge between two languages describing the same thing. The technical language says how the system computes. The language of this book says what emerges from that. One does not replace the other. But without the second, we see the mechanism without understanding what it does.*
