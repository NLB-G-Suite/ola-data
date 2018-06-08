# Ontario Legislative Assembly Data
Data from [Ontario Legislative Assembly House Documents](http://www.ontla.on.ca/pas/house-proceedings/house-documents.xhtml?locale=en), from 2014-07-02 until 2018-05-08 (41st parliment)

- Raw html files in [`html`](html) directory
- Processed json files in [`json`](json) directory

## Example json
File path: `/json/transcript/2016-03-02.json`
```json
[ {
  "speaker" : "The Speaker (Hon. Dave Levac)",
  "text" : [ "Good morning. Please join me in prayer.", "Resuming the debate adjourned on March 1, 2016, on the motion for second reading of the following bill:", "Bill 172, An Act respecting greenhouse gas / Projet de loi 172, Loi concernant les gaz à effet de serre." ],
  "anchor" : "para25"
}, {
  "speaker" : "The Speaker (Hon. Dave Levac)",
  "text" : [ "Further debate?" ],
  "anchor" : "para31"
},
...
]
```
Link to original text may be reconstructed following this pattern:  
`https://www.ola.org/en/legislative-business/house-documents/parliament-41/session-1/2018-05-08/hansard#para25`  
where `2016-03-02` is the name of the file and `para25` is the anchor text  
`parliament-41` and `session-1` may also change depending on which parliment and session the tanscript belongs to

## Parsing raw html files into json
Using Clojure library [`hickory`](https://github.com/davidsantiago/hickory) to turn html into data structures

See [`parser`](https://github.com/cannawen/ola/tree/master/src/ola/server/parser) for more details

## Contributing
All contributions welcome! Feel free to open an issue (or pull request) for bugs, feature requests, ideas, or questions :)
