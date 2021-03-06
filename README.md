# ig-query

This README documents the usage of the `ig-query.py` script for accessing the iDefense IntelGraph Customer APIs. The script processes the rich JSON data returned by the API and optionally renders it in HTML or human-readable text format.

## Usage

The script requires an API authentication token as documented at the [IntelGraph documentation site](https://intelgraph.idefense.com/#/docs/view#page-section-2-0) (the "API code"). For security reasons, the script looks for your IG API token in the environment variable `IDEF_TOKEN` rather than specifying directly on the command line. 

The syntax is as follows:

```
usage: ig-query.py [-h] [--debug] [--format {html,json,markdown}] key
```

- `-h`: Help message
- `--input`: Specify an input file containing keys for querying
- `--format`: Specify format for output. Choices are `json`, `html`, or `markdown` (a human-readable text format).

Note that this script requires the use of the [requests](http://docs.python-requests.org/en/master/) and [Markdown](https://python-markdown.github.io/) libraries.

## Output Formats

### Markdown

\# \[*fundamental indicator entered*\]

\#\# Properties <br>
\- Created on: \[*date created*\] <br>
\- Modified on: \[*last date modified*\] <br>
\- Severity: \[*severity number*\] (if any) <br>
\- Threat Types: (if any)<br>
    \[*list of types*\] <br>
\- Last seen as: (if any) <br>
    \[*list of last seen*\] <br>
\- Comment: \[*meta data*\] (if any) <br>
\#\# Relationships (if any) <br>
    \[*list of relationships*\]

#### examples

<img width="293" alt="markdown example" src="https://user-images.githubusercontent.com/52054422/109847986-c838e600-7c1d-11eb-95cd-fb02896f6beb.png">

<img width="446" alt="mark 2" src="https://user-images.githubusercontent.com/52054422/109848013-d129b780-7c1d-11eb-8247-c075823346e9.png">



## Known issues

None at this time.

Please report any issues via [our GitHub page](https://github.com/iDefense/ig-query).
