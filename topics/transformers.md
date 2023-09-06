- [Transformers](#transformers)
  - [Encoder](#encoder)
  - [Decoder](#decoder)

# Transformers

A neural network architecture useful for understanding language, which does not have to analyze words one at a time but can look at an entire sentence at once. The Transformer is designed to handle sequences of data, such as a sentence or paragraph, by paying selective attention to parts of the input sequence when producing the output. This leads to faster computations and the ability to capture relationships between words regardless of their distance from each other in a sequence. This is done using self-attention mechanisms.

1. **Self-Attention Mechanism**: Allows the model to weigh the importance of different words in an input sequence relative to a particular word being processed. This means that when the model is "thinking" about a word, it can consider the context provided by all other words in the sentence, not just nearby ones.
2. **Positional Encoding**: A unique feature of the Transformer is its lack of inherent understanding of the order or position of words. To address this, positional encodings are added to word embeddings (numeric representations of words) to provide the model with information about where each word is located in the sequence.
3. **Feed-Forward Neural Networks**: Once attention scores are computed and applied to the word embeddings, each resulting embedding is passed through its own feed-forward neural network. This network is the same across positions, but the inputs and outputs to it can vary based on the attention mechanism's results.
4. **Residual Connection**: A residual connection is a shortcut connection that bypasses one or more layers. In the Transformer, it connects the input of each sub-layer to its output. This helps in preventing the "vanishing gradient" problem and facilitates the training of deep networks.
5. **Layer Normalization**: Layer normalization is a technique used to stabilize the activations (outputs) of neurons in a network. By ensuring the activations have a consistent scale and distribution, training becomes more stable and faster.
6. **Stacked Layers**: The Transformer architecture comprises multiple identical layers stacked on top of one another, both in its encoder (which processes the input data) and decoder (which produces the output data). Each layer captures different types of relationships and features in the input data, allowing the model to understand complex patterns.


## Encoder

The encoder's primary job is to process the input sequence and compress this information into a 'context' or 'memory' for the decoder to use. Here's how it works:

1. Input Embedding: The input sequence is first converted into embeddings, which are dense vector representations of the words in the sequence. Words in a sequence (like a sentence) are typically represented as tokens. Directly processing these tokens is challenging because they are discrete and symbolic. So, we convert them into a format that's more amenable to mathematical operations.
    - **Embeddings**: These are continuous vector representations of words. Instead of representing a word as a single number or one-hot vector, embeddings capture the word's meaning in a dense vector, usually with hundreds of dimensions. This makes it easier for the neural network to understand and process the relationship and semantics of words.
2. Positional Encoding: In typical feed-forward or densely connected neural networks, the order of input data isn't inherently considered. But in sequence-to-sequence tasks, the position or order of words is crucial for understanding the meaning.
    - **Positional Encoding**: This step adds information about the position of a word within the sequence to its embedding. By doing so, the model can consider the order of words, which is especially important in languages and tasks where word order can change meaning.
3. Multiple Encoder Layers: The input sequence, now with embeddings and positional encodings, is passed through several layers of processing. These layers help the model to refine its understanding of the input sequence.
   - **Multi-head self-attention mechanism**: This mechanism allows the model to focus on different parts of the input sequence with varying degrees of attention. In essence, it lets the encoder look at other words in the sequence when processing a particular word, determining which words are most relevant in the given context. The "multi-head" aspect means this attention process happens multiple times in parallel, each time focusing on different parts or aspects of the input.
   - **Feed-forward neural networks**: After the attention mechanism, the data passes through a feed-forward neural network. This network is the same for each position (word) in the sequence and helps in further refining the representations. It’s worth noting that the encoder layers are stacked, meaning the output of one layer becomes the input to the next. Each subsequent layer helps in extracting higher-level features and understanding from the input sequence.

To summarize, the encoder takes an input sequence, converts its words to embeddings, adds positional information, and then processes this data through multiple layers that use attention and feed-forward mechanisms to create a rich, compressed context for the decoder to use.

## Decoder 

In models like the original Transformer used for machine translation, the decoder's role is to generate an output sequence from the context provided by the encoder. Here's how it operates:

1. **Output Embedding**: Similar to the input embedding in the encoder but for the output sequence.
    - **What it is**: Just as the encoder has an input embedding to convert input tokens (words or sub-words) into dense vectors, the decoder has an output embedding for the same purpose but for the output sequence.
    - **Purpose**: Embeddings represent words or tokens in a way that captures their semantic meaning in dense vector space. This enables the model to understand and process them more effectively.
2. **Positional Encoding**: Again, positional information is added to the embeddings.
    - **What it is**: The Transformer doesn't inherently know the order of tokens in a sequence since it processes all tokens in parallel. To give it some notion of order or position, a positional encoding is added.
    - **Purpose**: By adding positional encoding to embeddings, the model can take into account the position of a word in a sequence, which is crucial for understanding the meaning in many languages. For example, word order can change the meaning of a sentence.
3. **Multiple Decoder Layers**: The embeddings then pass through several identical decoder layers, each consisting of:
    - Multi-head self-attention mechanism (focused on the output sequence itself).
        - **What it is**: An attention mechanism allows the model to focus on different parts of the input sequence when generating the output. Multi-head means this attention is split into multiple parts (or "heads"), with each head focusing on different aspects or features of the data.
        - **Purpose**: When generating the output, it's crucial to consider previously generated tokens. Self-attention on the output sequence allows the model to consider the relationship between tokens in the output sequence itself.
    - Multi-head attention mechanism over the encoder's output (this provides the link between the input and output sequences).
        - **What it is**: This is another attention mechanism, but instead of focusing on the output sequence, it focuses on the encoder's output.
        - **Purpose**: This allows the decoder to take into account the entire input sequence when generating each token in the output. It essentially provides a bridge between the input and the output, ensuring the output is contextually relevant to the input.
    - Feed-forward neural networks.
        - **What it is**: After the attention mechanisms, the data passes through a feed-forward neural network within the decoder layer.
        - **Purpose**: This network further transforms the data, allowing the model to learn more intricate patterns and relationships.

The final output from the last decoder layer is the sequence that the Transformer model predicts, such as a translated sentence in the context of machine translation.