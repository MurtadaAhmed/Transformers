# Transformers

attention

1. self-attention: how much attention each word in the sentence pays to the other words including itself. >> assign attention score to each word.
each word is converted into three vectors:
Q >> what am I looking for?
K >>  what do i contain?
V >> what info do i carry?

- Attention score is calculated by comparing the Q and K for each word
- turning the scores in weights (using softmax)
- the word takes weighted average of the values based on those wrights.

this way each word knows a little bit about the whole sentence, not just itself.

2. Transformer architecture:

A. encoder: understands the input
B. decoder: generate output

each part has:
- multi-head self-attention
- feed-forward neural network
- LayerNorm + Residual connections

3. Positional encoding:
adding positional encoding for each words' embedding to indicate it position

4. muti-head attention
instead of one self-attention, it will do multiple in parralel
- one focus on grammar
- another on meaning
- another on nearby words
then combine them.

5. Feedforward Layer
each word's representation goes through small neural network to help learning complex patterns