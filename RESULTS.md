Dataset: https://github.com/UniversalDependencies/UD_Norwegian-Bokmaal

| Before      | After  |
|-------------|--------|
| 96.10       | 96.29  |

Features that increased quality: two and three symbols long prefixes, DET and PRON as previous tags.

Features that did not increased quality: two symbols long suffixes, AUX, PART and ADP as previous tags, prefixes 'her' and 'der', 'å' as previous word.

Mistakes examples: 

sent_id =  015698, 4	tale : NOUN instead of VERB

'Tale' can be both noun and verb in Norwegian. 

sent_id =  015699 14	nøkterne : NOUN instead of ADJ

Both nouns and adjectives can end with 'ne' in Norwegian.

We would need to know semantics of the left and right context to disambiguate these cases.

sent_id =  015701 24	fotografert : VERB instead of ADJ

'fotografert' is a participle, so it is not a mistake

sent_id =  015708 3	heretter : VERB instead of ADV

Words that end with 'er' are usually verbs in Norwegian. I tried to add a feature for 'her' and 'der', since there is a number of adverbs that are derived from 'her' and 'der' ('here' and 'there'), but it helped not.

sent_id =  015708 33	få : VERB instead of AUX

'Få' ('get') can be both auxiliary and main verb. This case is an annotator`s mistake.

It can be seen that a perceptron shows rather good result for Norwegian POS-tagging. Semantical information about given word and its context would be useful to achieve 100% quality.