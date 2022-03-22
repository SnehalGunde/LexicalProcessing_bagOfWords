# LexicalProcessing_bagOfWords

In this approach, we use the tokenized words for each observation and find out the frequency of each token.
Let’s take an example to understand this concept in depth.

“It was the best of times”

“It was the worst of times”

“It was the age of wisdom”

“It was the age of foolishness”

We treat each sentence as a separate document and we make a list of all words from all the four documents excluding the punctuation. We get,

‘It’, ‘was’, ‘the’, ‘best’, ‘of’, ‘times’, ‘worst’, ‘age’, ‘wisdom’, ‘foolishness’

The next step is the create vectors. Vectors convert text that can be used by the machine learning algorithm.

We take the first document — “It was the best of times” and we check the frequency of words from the 10 unique words.
“it” = 1
“was” = 1
“the” = 1
“best” = 1
“of” = 1
“times” = 1
“worst” = 0
“age” = 0
“wisdom” = 0
“foolishness” = 0

Rest of the documents will be:

“It was the best of times” = [1, 1, 1, 1, 1, 1, 0, 0, 0, 0]

“It was the worst of times” = [1, 1, 1, 0, 1, 1, 1, 0, 0, 0]

“It was the age of wisdom” = [1, 1, 1, 0, 1, 0, 0, 1, 1, 0]

“It was the age of foolishness” = [1, 1, 1, 0, 1, 0, 0, 1, 0, 1]

In this approach, each word or token is called a “gram”. Creating a vocabulary of two-word pairs is called a bigram model.
For example, the bigrams in the first document : “It was the best of times” are as follows:

“it was”

“was the”

“the best”

“best of”

“of times”

The process of converting NLP text into numbers is called vectorization in ML. Different ways to convert text into vectors are:
Counting the number of times each word appears in a document.

Calculating the frequency that each word appears in a document out of all the words in the document.

### CountVectorizer
CountVectorizer works on Terms Frequency, i.e. counting the occurrences of tokens and building a sparse matrix of documents x tokens.
