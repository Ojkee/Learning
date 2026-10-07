# Concept
New (at the time) deep learning approach for translation tasks. 
Authors suppose that fixed-length vector produced by Encoder in Encoder-Decoder networks is bottleneck in such tasks, where length of input may vary and Encoder needs to compress all the information from input sequence to that vector.
They introduce mechanism that (soft-)searches words that are important to generate next word token. In contrast to encoding sentence into fixed-length vector, model encodes input sequence into a sequence of vectors and chooses a most relevant subset.

# Background
Translation from probabilistic perspective the process of maximizing conditional probability of $\bf{y}$ correct sequence, given input sequence $\bf{x}$.
$$ 
\arg\max_{\textbf{y}} p(\textbf y | x)
$$
Neural networks directly learn this conditional distribution. Typically architectures were built with two components, one encoded input sequence, other decoded that encryption to output sequence.

### RNNs 
RNN architectures reads input sequence as sequence of vectors $\textbf {x} = (x_1, \dots, x_{T_x})$, and encodes it to vector $\bf c$ yielding hidden state $\bf h_t$ at time $t$. 
$$
h_t = f(x_t, h_{t-1})
$$
$$
c = q(\{h_1, \dots, h_{T_x}\})
$$
Decoder then takes that encoded state $c$, all previously generated words $\{y_1, \dots, y_{t`-1}\}$ and produces the next word $y_{t`}$.  In other point of view, decoder defines probability over the translation $\bf y$ by decomposing the joint probability into the ordered conditionals:
$$
p(\textbf {y}) = \prod^T_{t=1} p(y_t|\{y_1,\dots,y_{t-1}\}, c)
$$
where each conditional probability is modeled as
$$
p(y_t|\{y_1, \dots, y_{t-1}, c\}) = g(y_t, s_t, c)
$$
$s_t$ is the hidden state of RNN decoder.

# Learning to Align and Translate
### Encoder 
