# arabic_event_gsr

Gold standard records for Arabic event data

# Event Detection

We provide two "event detection" datasets for Arabic language event coding, one
for ASSAULT events and one for PROTEST events. These events are coded using the
[PLOVER](https://github.com/openeventdata/PLOVER) ontology, which is similar to
the [CAMEO](http://eventdata.parusanalytics.com/data.dir/cameo.html) ontology.
THese files can be used to test an automated coder's ability to recognize these
two event types in Arabic text.

`protest_gsr.csv` and `assault_gsr.csv` each have the following columns:

- `accept`: the number of annotators accepting the event label as true
- `event_type`: "ASSAULT" or "PROTEST", depending on the file
- `id`: the ID number of the sentence
- `label`: one of "yes", "easy no", "difficult no", or "ambiguous", depending
    on the set of labels provided by annotators. "yes" is unanimous accept,
    "easy no" is unanimous reject, "hard no" is mostly reject with a dissenting
    accept, and "ambiguous" are entries with insufficent labels to be sure.
- `reject`: the number of annotators who rejected the label.
- `text`: the text shown to the annotator and that should be provided to the
    event detection system
- `total`: the total number of annotations provided on the sentence.

