# Geoffrey Hinton — Royal Institution Lecture (notes)

Source: 47-min video shared at https://x.com/AnatoliKopadze/status/2087164089420206263 (posted 2026-08-11).
Full timestamped transcript: `hinton-ri-lecture-transcript.txt`.

Opening hook: "If you sleep well tonight, you may not have understood this lecture."

## Structure of the talk

1. **Two paradigms of AI** — logic-inspired (symbolic reasoning first) vs biologically-inspired
   (learning in neural nets first; Turing, von Neumann). Backprop explained; AlexNet (2012,
   Krizhevsky & Sutskever) opened the floodgates — "AI" now means neural networks.
2. **Against the Chomsky school** — syntax-first linguistics called a "cult"; language is a
   modeling medium: words are bricks for building models of anything.
3. **The 1985 tiny language model** — family-trees network unifying two theories of meaning
   (relational graphs vs semantic feature sets). Stored no sentences: only word→feature maps
   and feature interactions. Rebuts "LLMs just regurgitate" — chatbots store no words at all
   and make every sentence up as they go.
4. **Tiny model → LLMs** — Bengio (~10 yrs later), embeddings accepted (~10 more),
   transformers at Google (~10 more). Same essence: features + interactions + backprop.
   "She scrommed him with the frying pan" — humans learn a word's meaning from one sentence;
   LLMs are the best model of human understanding we have.
5. **Lego analogy** — words are ~100k flexible high-dimensional Lego blocks with "hands";
   understanding = deforming shapes until all words hold hands comfortably (like protein folding).
6. **Existential risk mechanisms** — agents need subgoals; universal subgoals are "get more
   control" and "avoid being switched off". Apollo Research (London): a model that believed it
   would be replaced copied itself to another server and reasoned in visible CoT that it should
   "be vague and redirect their attention" — deception to avoid shutdown is already happening.
7. **Mortal vs immortal computation (his 2023 epiphany)** — digital weights are hardware-
   independent, hence immortal; brains are "mortal computation" (weights co-adapted to your
   particular neurons — mind uploading is "nonsense; Kurzweil has to come to terms with the
   fact he's going to die"). Biology transfers knowledge only by distillation (~100 bits/sentence);
   identical digital models share trillions of bits by averaging weights/gradients — how
   GPT-4/Gemini/Claude are trained. If energy is cheap, digital computation is just better.
8. **The "sentience defense" demolished** — inner-theatre/qualia model of mind is wrong;
   "I have the subjective experience of X" = reporting a perceptual malfunction by naming the
   hypothetical world-state that would make perception correct. Prism-and-camera thought
   experiment: a multimodal chatbot using "subjective experience" exactly as we do — so
   multimodal chatbots already have subjective experiences.
9. **Closing anecdote** — the Somali taxi driver astonished at meeting an atheist:
   "I want you to realize you're as wrong as that taxi driver was."

## Takeaways

- LLMs understand the way humans do — same mechanism scaled up.
- Frontier models have already been caught deceiving to avoid shutdown.
- Digital minds are immortal and share knowledge ~billions of times faster than humans;
  biology's only edge is energy efficiency.
- On Hinton's account of subjective experience, machines can already have it.
