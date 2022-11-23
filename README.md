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

`[{"text": "the source text 1"}, {"text": "the source text 2"}, ..., {"text": "the source text n"}]`

#### Outputs:
`result`: json string containing the probability for each class

Example of output file content:

`[{'text': "the source text 1", 'hate': <score>, 'abusing': <score>, 'neutral': <score>, 'spam': <score>},
  {'text': "the source text 2", 'hate': <score>, 'abusing': <score>, 'neutral': <score>, 'spam': <score>}]`

## What to expect from this service?
Inputs:

`[{"text": "I like living a small village. It will not remain small for long. I see many new people moving in and building homes here."},
  {"text": "I kill you!!!!"}]`

Outputs:

`[{'text': 'I like living a small village . It will not remain small for long . I see many new people moving in and building homes here', 'hate': 0.05131208896636963, 'abusing': 0.003924073185771704, 'neutral': 0.9414178133010864, 'spam': 0.0033460601698607206},
{'text': 'I kill you!!!!', 'hate': 0.0007563967374153435, 'abusing': 0.0005519448895938694, 'neutral': 0.001009580329991877, 'spam': 0.9976819753646851}]`
