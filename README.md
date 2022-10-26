# NRCLex

## About
NRCLex will measure emotional affect from a body of text.  Affect dictionary contains approximately 27,000 words, and is based on the National Research Council Canada (NRC) affect lexicon and the NLTK library's WordNet synonym sets.

## Update
* Finally got around to cleaning this up a bit.  Updated PyPI package with current version.  Thanks to all the contributors for cleaning up my terrible code!
* Expanded NRC lexicon from approximately 10,000 words to 27,000 based on WordNet synonyms.
* Minor bug fixes.
* Contributor updated NTC library.

## Installation
`pip install NRCLex`

## Affects
Emotional affects measured include the following:

* fear
* anger
* anticipation
* trust
* surprise
* positive
* negative
* sadness
* disgust
* joy

## Sample Usage

`from nrclex import NRCLex`<br><br>


*#Instantiate NRCLex object, you can pass your own dictionary filename in json format.*<br>

`text_object = NRCLex(lexicon_file='nrc_en.json')`<br><br>


*#You can pass your raw text to this method(for best results, 'text' should be unicode).*<br>

`text_object.load_raw_text(text: str)`<br><br>


*#You can pass your already tokenized text as a list of tokens, if you want to use an already tokenized input.
This usage assumes that the text is correctly tokenized and does not make use of TextBlob.*<br>

`text_object.load_token_list(list_of_tokens: list)`<br><br>


*#Return words list.*<br>

`text_object.words`<br><br>


*#Return sentences list.*<br>

`text_object.sentences`<br><br>


*#Return affect list.*<br>

`text_object.affect_list`<br><br>


*#Return affect dictionary.*<br>

`text_object.affect_dict`<br><br>


*#Return raw emotional counts.*<br>

`text_object.raw_emotion_scores`<br><br>


*#Return highest emotions.*<br>

`text_object.top_emotions`<br><br>


*#Return affect frequencies.*<br>

`text_object.affect_frequencies`
