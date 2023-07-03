I'm a big fan of static site generators and since last year I've been using [Hugo](https://gohugo.io/)for a lot of simple and small marketing/product websites for clients. However, I don't know `Go` and I struggle a bit to remember all the logic that works in the templates so... I do a lot of searching and copy-pasting. 

I started to collect the code/logic that I use most often in websites of this kind. Basically, this page will become for me what CSS Tricks's "A complete guide to Flexbox" is for everyone!

Some of these are in the documentation of Hugo but I personally find it easier to find things with examples. In fact, almost everything I needed, I found via the community chat from Hugo.

Also, some of these things will likely seem very obvious to people who are very used to using Hugo. I am also 100% certain that there are better ways to do certain things. In my opinion, it doesn't really matter as long as the output does what we need. But I had to start somewhere, so this is the blog post I wish I had found when I first started.

The if/else
----------------------------------------------------------------------------

```
{{ if }}
 // something
{{ else }}
 //something
{{ end }}

```

How to check if a value is equal to something
-------------------------------------------------------------------------------------------------------------------------------------------------

```
{{ if eq value_1 value_2 }}

```

How to check if a value is lower than something
-----------------------------------------------------------------------------------------------------------------------------------------------------

```
{{ if lt value_1 value_2 }}

```

How to check if a value is greater than something
---------------------------------------------------------------------------------------------------------------------------------------------------------

```
{{ if gt value_1 value_2 }}

```

How to combine two checks
---------------------------------------------------------------------------------------------------------

This example checks if a value is lower than 5 and greater than 1.

```
{{ if and (lt $currentIndex 5) (gt $currentIndex 1) }}

```

How to add a class based on what page you're on
----------------------------------------------------------------------------------------------------------------------------------------------------

I wanted to add a specific class to a page called "Privacy Policy". This page was created inside my `content` folder and I named its folder `privacy-policy`and inside it I created an `_index.md`. The frontmatter of the `.md` file has a title. Something like: `title: Privacy Policy`.

I want a specific class to be added to an element when I visit this particular page.

```
<main class="{{ if eq .Name `Privacy Policy` }}privacy{{ end }}" id="main"> My content</main>

```

How to update aria-current in a menu
------------------------------------------------------------------------------------------------------------------------------

This particular example assumes we're iterating on a menu set in the config.

```
<nav aria-label="Main menu">
 <ul>
  {{ $currentPage := . }} {{ range .Site.Menus.main }}
  <li>
   <a aria-current="{{if or ($currentPage.IsMenuCurrent `main` .) ($currentPage.HasMenuCurrent `main` .)}}true{{else}}false{{end}}" href="{{ .URL }}" title="{{ .Title }}">
    {{ .Name }}
   </a>
  </li>
  {{ end }}
 </ul>
</nav>

```

How to only render something if there is more than one page in a section.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This example assumes we have a section called "latest" that has some posts inside it.

```
{{ $news := where .Site.RegularPages "Section" "latest" }}
{{ $postCount := len $news }}

{{ if gt $postCount 0 }}
 <section>{{.Title}}</section>
{{end}}

```

How to only show the latest three posts of a section
---------------------------------------------------------------------------------------------------------------------------------------------------------------

This example assumes we have a section called "latest" that has some posts inside it.

```
{{ $news := where .Site.RegularPages "Section" "latest" }}
<ul>
 {{ range first 3 $news }}
  <li>
   {{.Title}}
  </li>
 {{ end }}
</ul>

```

How to create a collection of posts that have a certain param and value
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This example wants to collect all the posts inside a section that have a specific param defined in the frontmatter.For this example, let's assume that we're looking for all the posts inside a section called "latest" that have `type: summary`.

```
{{ $services := where .Site.RegularPages "Section" "latest" }}
{{ $finalList := where $services "Params.type" "summary" }}

```

How to create a collection of posts that match a certain value
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This example creates a variable called `test` that iterates over the pages inside a section called `case-studies` that have the value of `draft` as false.

```
{{$test := where (where .Site.RegularPages "Section" "case-studies") ".Params.draft" false }}

```

How to range and order by the value of a param
---------------------------------------------------------------------------------------------------------------------------------------------------

This example assumes that a page has `order` in the frontmatter and a number.

```
{{ $services := where .Site.RegularPages "Section" "latest" }}
{{ range $services.ByParam "order" }}
// your content
{{ end }}

```

How to replace a character with something else
---------------------------------------------------------------------------------------------------------------------------------------------------

I had a specific situation where I had to replace "_" with a blank space in a couple of words.

```
{{ replace $tag "_" " "}}

```

How to get the content of an _index.md inside a partial
-------------------------------------------------------------------------------------------------------------------------------------------------------------------

Imagine you have a partial (like a banner) and could like to bring the content of the index of a section to it (in this case, for example an "about" page).

```
{{ with .Site.GetPage "/about" }} {{ .Content }}{{ end }}

```

How to get Pages that have a value that resolves into false
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

This example collects all the pages inside a section that has the value "false" for the draft.

```
where .Pages ".Params.draft" false

```

How to show a list and add commas
-------------------------------------------------------------------------------------------------------------------------

This example attempts to re-create something like the following:

"Animals that are very chill: capybaras, tortoises, dogs."

```
<div>
 <p>Animals that are very chill:
 {{ $list := (where .Site.Pages "Section" "animals") }}
 {{ $len := (len $list) }}
 {{ range where .Site.Pages "Section" "animals" }}
  {{ range $index, $element := .Pages }}
   {{ $currentIndex := (add $index 1)}}
   {{ $currentLength := (sub $len 1 )}}
   {{.Title}}
   {{ if eq $currentIndex $currentLength }}. {{else}}, {{end}}
  {{ end }}
 {{ end }}
 </p>
</div>

```

Iterate inside a section and combine options
-----------------------------------------------------------------------------------------------------------------------------------------------

Assuming you're adding this to the `list.html` of a section, this example shows how to get all the pages of a section that have the param draft as `false` and putting them in reverse chronological order.

```
{{ range ((where .Pages ".Params.draft" false).ByParam "order").Reverse }}

```
