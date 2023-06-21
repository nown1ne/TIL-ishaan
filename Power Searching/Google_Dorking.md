# Google Advanced Search Operators


| Operator    | Description                                                                                                                                                                                   | Category   |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| `""`        | Allows searching for a specific phrase - exact match search. Individual word prevents synonyms                                                                                                | Basic,Mail |
| `OR`/`AND`  | Boolean search function for OR searches as Google defaults to AND between words - must be all caps                                                                                            | Basic,Mail |
| `\`         | Implements OR                                                                                                                                                                                 | Basic      |
| `()`        | Allows grouping of operators and helps dictate order                                                                                                                                          | Basic,Mail |
| `-`         | Excludes a word from results                                                                                                                                                                  | Basic,Mail |
| `*`         | Acts as a wildcard and will match any word or phrase                                                                                                                                          | Basic      |
| `#..#`      | # represents a number in this instance. Use to find numbers in a series.                                                                                                                      | Basic      |
| `$`         | Allows for search of USD                                                                                                                                                                      | Basic      |
| `€`         | Allows for search of Euro                                                                                                                                                                     | Basic      |
| `in`        | Allows searches for unit conversion (currency, unit or measure)                                                                                                                               | Basic      |
| `~`         | Prefix - Include synonyms (potentially defunct)                                                                                                                                               | Basic      |
| `+`         | Prefix - Force exact match on single phrase                                                                                                                                                   | Basic,Mail |
| `AROUND(X)` | This is sandwiched between two words and the X declares how many words they must be mentioned between. I.e. if it’s (4) then the two keywords must be mentioned within 4 words of each other. | Advanced   |
| `_`         | Acts as wildcard for autocomplete                                                                                                                                                             | Advanced   |


### Search with url
| Operator    | Description                                                                                                                                | Category |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|----------|
| `inurl:`    | Only returns results where the queried keyword(s) is present in the URL                                                                    | Advanced |
| `allinurl:` | As above but only containing all of the specified words in the URL                                                                         | Advanced |
| `blogurl:`  | Find blog URLs under a specific domain. This was used in Google blog search, but I’ve found it does return some results in regular search. | Advanced |
| `site:`     | Limit results to those from one site                                                                                                       | Advanced |
| `related:`  | Find similar domains to the queried domain                                                                                                 | Advanced |


### Search with dates
| Operator     | Description                                                                                          | Category   |
|--------------|------------------------------------------------------------------------------------------------------|------------|
| `daterange:` | Return results in a specified range (requires julian dates)                                          | Advanced   |
| `after:`     | Allows you to search drive or mail for files modified or mail sent/received anytime after a set date | Drive,Mail |
| `before:`    | Allows you to search drive or mail for files modified or mail sent/received before a certain date    | Drive,Mail |
| `older:`     | Search for messages older than a certain date                                                        | Mail       |
| `newer:`     | Search for messages newer than a certain date                                                        | Mail       |


### Search files
| Operator        | Description                                                                                          | Category   |
|-----------------|------------------------------------------------------------------------------------------------------|------------|
| `filename:`     | Search for messages with a particular type of file attached, or the exact name of a file             | Mail       |
| `type:`         | Allows you to search drive by file type                                                              | Drive      |
| `owner:`        | Allows you to search drive by owner of file or folder                                                | Drive      |
| `to:`           | Allows you to search drive for files shared with a specific person                                   | Drive      |
| `title:`        | Searches drive for files with the keyword in their title alone                                       | Drive      |
| `source:domain` | Allows you to search for files or folders shared with everyone in your business                      | Drive      |
| `filetype:`     | Returns only files of a particular type associated with the keyword searched                         | Advanced   |
| `ext:`          | As above, based on extension                                                                         | Advanced   |
| `after:`        | Allows you to search drive or mail for files modified or mail sent/received anytime after a set date | Drive,Mail |
| `before:`       | Allows you to search drive or mail for files modified or mail sent/received before a certain date    | Drive,Mail |
| `is:trashed`    | Searches for the item in the Drive bin                                                               | Drive      |


### Search with page content
| Operator       | Description                                                                                                         | Category |
|----------------|---------------------------------------------------------------------------------------------------------------------|----------|
| `link:`        | Find pages that link to the target domain                                                                           | Advanced |
| `inanchor:`    | Find pages linked to with the specified anchor text/ phrase. Data is heavily sampled.                               | Advanced |
| `allinanchor:` | Find pages with all individual terms after "inanchor:" in the inbound anchor text.                                  | Advanced |
| `intitle:`     | Returns pages based on the searched query appearing in their title                                                  | Advanced |
| `allintitle:`  | Similar to intitle: but only returns titles where all the words in the title match                                  | Advanced |
| `inposttile:`  | Finds pages with keywords in their post titles (i.e. for researching blogs)                                         | &nbsp;   |
| `intext:`      | Finds pages where the keyword(s) are mentioned within the page content.                                             | Advanced |
| `allintext:`   | Similar to “intext,” but only results containing all of the specified words somewhere on the page will be returned. | Advanced |


### Keywords
| Operator          | Description                                                                                      | Category |
|-------------------|--------------------------------------------------------------------------------------------------|----------|
| `Business`        | type E.g. cafe, restaurant, bar etc will return a selection of appropriate businesses in the are | Maps     |
| `Petrol/Charging` | Station EV near me or perol station near me returns                                              | Maps     |
| `Search`          | for a message with a google sheet attached                                                       | Mail     |
| `Search`          | for a message with a google presentation attached                                                | Mail     |


### Search on emails
| Operator          | Description                                                                                           | Category   |
|-------------------|-------------------------------------------------------------------------------------------------------|------------|
| `+`               | Prefix - Force exact match on single phrase                                                           | Basic,Mail |
| `()`              | Allows grouping of operators and helps dictate order                                                  | Basic,Mail |
| `-`               | Excludes a word from results                                                                          | Basic,Mail |
| `""`              | Allows searching for a specific phrase - exact match search. Individual word prevents synonyms        | Basic,Mail |
| `OR`/`AND`        | Boolean search function for OR searches as Google defaults to AND between words - must be all caps    | Basic,Mail |
| `after:`          | Allows you to search drive or mail for files modified or mail sent/received anytime after a set date  | Drive,Mail |
| `before:`         | Allows you to search drive or mail for files modified or mail sent/received before a certain date     | Drive,Mail |
| `is:starred`      | Searches only items that have been starred in drive                                                   | Drive,Mail |
| `from:`           | Specify the sender in google mail                                                                     | Mail       |
| `to:`             | Specify the recipient in google mail                                                                  | Mail       |
| `cc:`             | Search by a recipient that was copied into an email                                                   | Mail       |
| `bcc:`            | Search by a recipient that was blind copied into an email                                             | Mail       |
| `older:`          | Search for messages older than a certain date                                                         | Mail       |
| `newer:`          | Search for messages newer than a certain date                                                         | Mail       |
| `Search`          | for a message with a google sheet attached                                                            | Mail       |
| `Search`          | for a message with a google presentation attached                                                     | Mail       |
| `AROUND`          | Similar to the normal google search function, allows you to search for keywords near each other.      | Mail       |
| `subject:`        | Search by keywords featured in the subject line                                                       | Mail       |
| `{}`              | Use for OR in mail instead of the OR function                                                         | Mail       |
| `label:`          | Search for messages that have a certain label                                                         | Mail       |
| `has:attachment`  | Search for messages that have an item attached                                                        | Mail       |
| `has:drive`       | Search for messages with a google drive attached                                                      | Mail       |
| `has:document`    | Search for messages with a google doc attached                                                        | Mail       |
| `has:youtube`     | Search for a message containing a youtube video                                                       | Mail       |
| `list:`           | Search for all messages from a particular mailing list                                                | Mail       |
| `in:anywhere`     | Includes all folders in your search, including spam and bin                                           | Mail       |
| `is:important`    | Search for messages that have been marked as important                                                | Mail       |
| `label:important` | Same as is:important                                                                                  | Mail       |
| `is:snoozed`      | Searches for messages that have been snoozed                                                          | Mail       |
| `is:unread`       | Searches for unread messages                                                                          | Mail       |
| `is:read`         | searches for read messages only                                                                       | Mail       |
| `has:yellow-star` | Searches for messages with coloured star icon                                                         | Mail       |
| `has:blue-info`   | Searches for messages with colourd icon                                                               | Mail       |
| `is:chat`         | Searches for messagse from chat                                                                       | Mail       |
| `deliveredto:`    | Search by email address for delivered messages                                                        | Mail       |
| `category:`       | Searches by messages based on category. Follow the colon with the categoy name, i.e. category:primary | Mail       |
| `size:`           | Messages larger than a certain size in bytes                                                          | Mail       |
| `larger:`         | Messages larger than a certain size in bytes                                                          | Mail       |
| `smaller:`        | Messages smaller than a certain size in bytes                                                         | Mail       |
| `has:userlabels`  | Search for messages that have custom user labels                                                      | Mail       |
| ` `               | Search for messages that have no custom user labels                                                   | Mail       |


### Some other useful search operators
| Operator          | Description                                                                                                                                                            | Category   |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| `define:`         | Pulls a card response from Google displaying the dictionary definition of the word or phrase                                                                           | Advanced   |
| `cache:`          | Returns the most up to date cache of an indexed web page                                                                                                               | Advanced   |
| `weather:`        | Brings up the featured snipped for weather for that location                                                                                                           | Advanced   |
| `stocks:`         | Returns stock information for the specified ticker                                                                                                                     | Advanced   |
| `map:`            | Force google map results for a particular query                                                                                                                        | Advanced   |
| `movie:`          | Find information for the specified movie (particularly useful when that movie has an ambiguous name). If the movie is still in theatres it’ll also return screen times | Advanced   |
| `source:`         | Use in google news, returns results from the specified source                                                                                                          | Advanced   |
| `loc:`            | Returns results for a specific location                                                                                                                                | Advanced   |
| `location:`       | As above but with Google news                                                                                                                                          | Advanced   |
| `info:`           | Returns information related to a domain (pages with domain text, similar on-site pages, cache etc)                                                                     | Advanced   |
| `near`            | Part of the google maps lazy searches e.g. book shops near work                                                                                                        | Maps       |



Also see
--------

- [Google Search Operators Cheat Sheet](https://static.semrush.com/blog/uploads/files/39/12/39121580a18160d3587274faed6323e2.pdf) _(static.semrush.com)_


# Google Dorking

## Table Of Contents

- [Advanced Searching](#advanced-searching)

- [Search Operators](#search-operators)

- [Simple Examples](#simple-examples)

- [Finding Valuable Information](#finding-valuable-information)

- [Further](#further)

- [Meta](#meta)

---

## Advanced Searching

Google Dorking describes the process of using advanced search filters that allow to retrieve more efficient results. It is a technique often used by cybersecurity professionals in order to find valuable information about a target. While Google Dorking itself is legal (in most countries), it might quickly lead to actions that aren't, such as visiting a site with illegal content in it. Hence using [TOR](https://www.torproject.org/) or a [VPN](https://privacyguides.org/vpn/) is recommended. It is also beneficial to use a search aggregator like [SearX](https://searx.github.io/searx/).

---

## Search Operators

| Operator         | Description                                                                                                              | Syntax                               | Example                           |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------ | ------------------------------------ | --------------------------------- |
| ()               | Group multiple terms or operators. Allows advanced expressions                                                           | (&lt;term> or &lt;operator>)         | inurl:(html \| php)               |
| *                | Wildcard. Matches any word                                                                                               | &lt;text> * &lt;text>                | How to * a computer               |
| ""               | The given keyword has to match exactly. *case-insensitive*                                                               | "&lt;keywords>"                      | "google"                          |
| m..n / m...n     | Search for a range of numbers. *n* should be greater than *m*                                                            | &lt;number>..&lt;number>             | 1..100                            |
| -                | Documents that match the operator are excluded. *NOT*-Operator                                                           | -&lt;operator>                       | -site:youtube.com                 |
| +                | Include documents that match the operator                                                                                | +&lt;operator>                       | +site:youtube.com                 |
| \|               | Logical *OR-Operator*. Only one operator needs to match in order for the overall expression to match                     | &lt;operator> \| &lt;operator>       | "google" \| "yahoo"               |
| ~                | Search for synonyms of the given word. Not supported by Google                                                           | ~&lt;word>                           | ~book                             |
| @                | Perform a search only on the given social media platform. Rather use **site**                                            | @&lt;socialmedia>                    | @instagram                        |
| after            | Search for documents published / indexed after the given date                                                            | after:&lt;yy(-mm-dd)>                | after:2020-06-03                  |
| allintitle       | Same as **intitle** but allows multiple keywords seperated by a space                                                    | allintitle:&lt;keywords>             | allintitle:dog cat                |
| allinurl         | Same as **inurl** but allows multiple keywords seperated by a space                                                      | allinurl:&lt;keywords>               | allinurl:search com               |
| allintext        | Same as **intext** but allows multiple keywords seperated by a space                                                     | allintext:&lt;keywords>              | allintext:math science university |
| AROUND           | Search for documents in which the first word is up to *n* words away from the second word and vice versa                 | &lt;word1> AROUND(&lt;n>) &lt;word2> | google AROUND(10) good            |
| author           | Search for articles written by the given author if applicable                                                            | author:&lt;name>                     | author:Max                        |
| before           | Search for documents published / indexed before the given date                                                           | before:&lt;yy(-mm-dd)>               | before:2020-06-03                 |
| cache            | Search on the cached version of the given website. Uses Google's cache to do so                                          | cache:&lt;domain>                    | cache:google.com                  |
| contains         | Search for documents that link to the given fileype. Not supported by Google                                             | contains:&lt;filetype>               | contains:pdf                      |
| date             | Search for documents published within the past *n* months. Not supported by Google                                       | date:&lt;number>                     | date:3                            |
| define           | Search for the definition of the given word                                                                              | define:&lt;word>                     | define:funny                      |
| ext              | Search for a specific filetype                                                                                           | ext:&lt;documenttype>                | ext:pdf                           |
| filetype         | Refer to **ext**                                                                                                         | filetype:&lt;documenttype>           | filetype:pdf                      |
| inanchor         | Search for the given keyword in a website's anchors                                                                      | inanchor:&lt;keyword>                | inanchor:security                 |
| index of         | Search for documents containing direct downloads                                                                         | index of:&lt;term>                   | index of:mp4 videos               |
| info             | Search for information about a website                                                                                   | info:&lt;domain>                     | info:google.com                   |
| intext           | Keyword needs to be in the text of the document                                                                          | intext:&lt;keyword>                  | intext:news                       |
| intitle          | Keyword needs to be in the title of the document                                                                         | intitle:&lt;keyword>                 | intitle:money                     |
| inurl            | Keyword needs to be in the URL of the document                                                                           | inurl:&lt;keyword>                   | inurl:sheet                       |
| link / links     | Search for documents whose links contain the given keyword. Useful for finding documents that link to a specific website | link:&lt;keyword>                    | link:google                       |
| location         | Show documents based on the given location                                                                               | location:&lt;location>               | location:USA                      |
| numrange         | Refer to **m..n**                                                                                                        | numrange:&lt;number>-&lt;number>     | numrange:1-100                    |
| OR               | Refer to **\|**                                                                                                          | &lt;operator> OR &lt;operator>       | "google" OR "yahoo"               |
| phonebook        | Search for related phone numbers associated with the given name                                                          | phonebook:&lt;name>                  | phonebook:"william smith"         |
| relate / related | Search for documents that are related to the given website                                                               | relate:&lt;domain>                   | relate:google.com                 |
| safesearch       | Exclude adult content such as pornographic videos                                                                        | safesearch:&lt;keyword>              | safesearch:sex                    |
| source           | Search on a specific news site. Rather use **site**                                                                      | source:&lt;news>                     | source:theguardian                |
| site             | Search on the given site. Given argument might also be just a TLD such as **com, net**, etc                              | site:&lt;domain>                     | site:google.com                   |
| stock            | Search for information about a market stock                                                                              | stock:&lt;stock>                     | stock:dax                         |
| weather          | Search for information about the weather of the given location                                                           | weather:&lt;location>                | weather:Miami                     |

[[Back to top]](#table-of-contents)

---

## Simple Examples

```dork
"google" 1..100
```

> Search for websites that contain the word "google" and a number between 1 and 100

```dork
Videos -site:youtube.*
```

> Search for the term "Videos" but exclude results from YouTube

```dork
How to * a computer after:2022-01-01
```

> Search for websites published after the 1st January 2022 dealing about how to `use/repair/shutdown/...` a computer

```dork
allintext:homework teacher school site:gov before:2020 ext:(html | php)
```

> Search for websites published before 2020 which have the TLD `.gov`, are either html or php documents and contain the words "homework", "teacher" and "school"

```dork
@instagram chr3st5an
```

> Search for the term "chr3st5an" on instagram

[[Back to top]](#table-of-contents)

---

## Finding Valuable Information

```dork
intitle:"webcamXP 5" | inurl:"lvappl.htm"
```

> Find open/public webcams

```dork
intext:password ext:log
```

> Find log documents wich have the string "password" in it

```dork
inurl:/proc/self/cwd
```

> Find vulnerable webservers

```dork
inurl:email.xls ext:xls
```

> Find excel documents that contain email addresses

```dork
index of:mp3 intext:.mp3
```

> Find mp3 (music) documents

[[Back to top]](#table-of-contents)

---

## Further

You can find more Google Dorks at the [exploit-db](https://www.exploit-db.com/google-hacking-database)

[[Back to top]](#table-of-contents)

---

## Meta

##### License

The information provided here are dedicated to the public domain. Use them as you wish.

[[Back to top]](#table-of-contents)

