# hate-speech-detection
Hate Speech Detection service for SingularityNET
## Welcome
## What’s the point?
The service outputs a label that match to the specified text
## Model details:
Base model is BERTweet.
The service receives the text in English and then classifies it.

available labels:
- hate
- abusing
- neutral
- spam

### The user must provide the following inputs in order to start the service and get a response:
#### Inputs:
`text`: json string

Example of input file content:

`[{"text": "the source text1"}, {"text": "the source text2"}]`

#### Outputs:
`result`: json string containing the probability for each class

Example of output file content:

`[{'text': "the source text1", 'hate': <score>, 'abusing': <score>, 'neutral': <score>, 'spam': <score>},
  {'text': "the source text2", 'hate': <score>, 'abusing': <score>, 'neutral': <score>, 'spam': <score>}]`

## What to expect from this service?
Inputs:

`[{"text": "I hate you!"}, {"text": "I kill you!!!!"}]`

Outputs:

`[{'text': 'I hate you!', 'hate': 0.8309574723243713, 'abusing': 0.1641356498003006, 'neutral': 0.004906846210360527},
  {'text': 'I kill you!!!!', 'hate': 0.8971918225288391, 'abusing': 0.09692168235778809, 'neutral': 0.005886508617550135}]`
