# Entry 1: Introduction
### Why Web Scarping? 

   After finishing our last topic over APIs, I noticed that an API might not have all the information you would like. Web scraping also seemed like an interesting topic. The ability to access information without having to open that specific website. As well as being able to format and organize it all into its own page seemed pretty convenient to me.

### Messing around with Web Scraping

   While researching how web scraping actually worked I found out that there are multiple ways to go about it, either with different languages such as Ruby or Javascript, or with different gems. I ended up using nokoigiri, a ruby gem.

### Nokogiri (鋸)

   Nokogiri is a very popular Ruby gem parser. It can parse HTML, XML, SAX, and Reader, but I would be using it for HTML.

<img src="../images/nokoigiri.png"/>

### Extras to Web Scraping

**Regex:** A special text string for describing a search pattern.
   Regex is not as important to my whole project, but it helped me understand the format of the websites I was using.

```HTML
He is one of the < a href = "/wiki/List_of_best-selling_music_artists"
title = "List of best-selling music artists" > best - selling music artists of
all time < /a>, having sold more than 150 million records worldwide. < sup id = "cite_ref-2"
class = "reference" > < a href = "#cite_note-2" > [2] < /a></sup >
    Born in < a href = "/wiki/Hoboken,_New_Jersey"
title = "Hoboken, New Jersey" > Hoboken,
    New Jersey < /a>, to <a href="/wiki / Italian_Americans " title="
Italian Americans ">Italian immigrants</a>, 
Sinatra began his musical career in the < a href = "/wiki/Swing_era"
title = "Swing era" > swing era < /a> 
with bandleaders < a href = "/wiki/Harry_James"
title = "Harry James" > Harry James < /a> and  < a href = "/wiki/Tommy_Dorsey"
title = "Tommy Dorsey" > Tommy Dorsey < /a>
```
`(<a href="([^"]+)" title="([^"]+)">([^"]+)<\/a>)` Would highlight: 
```HTML
 <a href="/wiki/List_of_best-selling_music_artists" 
 title="List of best-selling music artists">
 best-selling music artists of all time</a>
```
```HTML
<a href="/wiki/Hoboken,_New_Jersey" title="Hoboken, 
New Jersey">Hoboken, New Jersey</a>
```
```HTML
<a href="/wiki/Italian_Americans" title="Italian Americans">Italian immigrants</a>, 
```
```HTML
<a href="/wiki/Swing_era" title="Swing era">swing era</a>
```
```HTML
<a href="/wiki/Harry_James" title="Harry James">Harry James</a>
```
```HTML
<a href="/wiki/Tommy_Dorsey" title="Tommy Dorsey">Tommy Dorsey</a>
```

[Next](/entry-2.md) | [Table of Contents](../README.md)