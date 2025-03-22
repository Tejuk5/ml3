from nltk.tokenize import word_tokenize ,sent_tokenize
from nltk.corpus import stopwords
import nltk

s=''' Good muffins cost $10000.\nin New York. Please buy me... two of them.\n\nThanks.'''


print(word_tokenize(s))
print(sent_tokenize(s))

nltk.download('stopwords')
print(stopwords.words('english'))
stop_words = set(stopwords.words('english'))

word_tokens = word_tokenize(s)
filtered_sentence = []
 
for w in word_tokens:
    if w not in stop_words:
        filtered_sentence.append(w)

print(word_tokens)
print(filtered_sentence)
