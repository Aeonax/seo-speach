## Seo... Magic
Search engine optimization is the process of growing the quality and quantity of website traffic by increasing the visibility of a website or a web page to users of a web search engine. _wiki_  
It is huge... It is magic... It is really huge espeсially if include "tricks" of Seo speciallists...

*crying and screaming cat required!*

What our main goal - improve our place in google results page. Currently for `San Francisco pickup waste` we are on second page... How offten do you visit second page?=D And in aggregator like yelp... there is no yellowsack O-o Because it located inside dumpster rent...  
`San Francisco dumpster removal`... IT WAS ON 5-th PAGE!!!!!! just how....

## What influencing on SEO?
- user behavior:
  - how long they inspected page/moved to another pages
  - do they visited another google results after us
- correct content
  - unique
  - descriptive - google hates
    - thin content pages
    - doorway pages - Substantially similar pages that are closer to search results than a clearly defined, browseable hierarchy
    - doesn't stuffed with everything you can...
  - google can reach that content=))) google sending crawlers which loading page with css and js. As some investigations shows it allows page to "load" for 20 seconds, from testing tools for 10 seconds
    - sitemap
    - robots.txt
    - nofollow for links
    - noindex as meta or header
  - we made short description of what located on page - structured data
    - schema.org ... which supported by google too.
    - rich results - google results will have special format

## Ranking
### Main principles
- title:                _Create short, meaningful page titles._
- Hx:                   _Use page headings that convey the subject of the page._
- more text, more alts: _Use text rather than images to convey content. (Google can understand some image and video, but not as well as it can understand text. At minimum, annotate your video and images with alt text and other attributes as appropriate.)_
- Faster!:             _Make your page fast to load, and mobile-friendly._
- Put useful content on your page and keep it up to date.

### How to help understand page
- good text: Create a useful, information-rich site, and write pages that clearly and accurately describe your content.
- keyphrases: Think about the words users would type to find your pages, and make sure that your site actually includes those words within it.
- title + alts: Ensure that your <title> elements and alt attributes are descriptive, specific, and accurate.
- page hierarchy: Design your site to have a clear conceptual page hierarchy.
- don't hide js/css: To help Google fully understand your site's contents, allow all site assets that would significantly affect page rendering to be crawled: for example, CSS and JavaScript files that affect the understanding of the pages. The Google indexing system renders a web page as the user would see it, including images, CSS, and JavaScript files. To see which page assets that Googlebot cannot crawl use the URL Inspection tool; to debug directives in your robots.txt file, use the robots.txt Tester tool.
- don't track robots=)))): Allow search bots to crawl your site without session IDs or URL parameters that track their path through the site. These techniques are useful for tracking individual user behavior, but the access pattern of bots is entirely different. Using these techniques may result in incomplete indexing of your site, as bots may not be able to eliminate URLs that look different but actually point to the same page.
- hide content from robots that shouldn't be seen - Make a reasonable effort to ensure that advertisement links on your pages do not affect search engine rankings. For example, use robots.txt, rel="nofollow", or rel="sponsored" to prevent advertisement links from being followed by a crawler.

### What google expecting from page
[source](https://webmasters.googleblog.com/2011/05/more-guidance-on-building-high-quality.html)
```
- Is this article written by an expert or enthusiast who knows the topic well, or is it more shallow in nature?
- Does the site have duplicate, overlapping, or redundant articles on the same or similar topics with slightly different keyword variations?
- Does this article have spelling, stylistic, or factual errors?
- Are the topics driven by genuine interests of readers of the site, or does the site generate content by attempting to guess what might rank well in search engines?
- Does the article provide original content or information, original reporting, original research, or original analysis?
Does the page provide substantial value when compared to other pages in search results?
```



## What can we do?
### Content
#### We should understand what google benefits should we use - what our company structure or how do we wan't to show it.
We can use rich results feature to be brighter on results page.
We should decide we are LocalCompany OR Product.  
    - LocalCompany with service sounds correct but it will not highlight prices in google results... We can show prices as "$"
    - Product will highlight prices but will not highlight feedbacks...

#### We should invent our "story" around choosen Seo strategic
- We are company that have departments in several regions and we are propposing dumpster bags and their pickups.
- We should describe that service - we should create entry points for our services like "dirt removal". It should be represented with page on which located some text with DIRT REMOVAL unique description/image.
- All pages should be smart linked, all our advantages should have their place in it.

### TECH - fill pages when content is ready
#### User friendly
yellowsack.com shouldn't be redundant entrance for app.yellowsack.com - it is our face and app.yellowsack is just checkout/profile. Newcomers should understand where are they and what should they do. Button order pickup should be understandable only for customers who know what is going on there. But each page should be understandable and lead to order - like "You can order `dumpster bag` or `pickup it`" but better and visible in or after text...
#### Improve google vision
We can add sitemap to show all active pages which we want to show google.
Mark text - google pay more attention to `Hx` and images `alt`, we shouldn't use them as just text formatting - we should make separate classes for divs for such cases...
More structured data with clever story and reverencing between pages.
Page description
#### Optimizations
Lighthouse


### Most apropriate type...
[source](https://www.youtube.com/watch?v=kG8L_-fhkNw)
```
If we want rich search results for pickups we need Product, but Service is good to - it will help google to understand page content and build apropriate search results including our specifics.
```




## Proplems
### Why organization on each page is bad:
[source](https://developers.google.com/search/docs/guides/sd-policies)
```
The structured data is not representative of the main content of the page, or is potentially misleading.
The content referred to by the structured data is hidden from the user.
Don't mark up content that is not visible to readers of the page. For example, if the JSON-LD markup describes a performer, the HTML body should describe that same performer.
```

### Why irrelevant keywords are bad:
[source](https://support.google.com/webmasters/answer/66358)
```
"Keyword stuffing" refers to the practice of loading a webpage with keywords or numbers in an attempt to manipulate a site's ranking in Google search results. Often these keywords appear in a list or group, or out of context (not as natural prose). Filling pages with keywords or numbers results in a negative user experience, and can harm your site's ranking. Focus on creating useful, information-rich content that uses keywords appropriately and in context.
```

## Possible data  
We should stop thinking of page that hauls everything what it can - we can [refer](https://www.w3.org/TR/json-ld/#advanced-concepts) nodes from another pages.
### pickups
Service - Yellowsack pickup - checkout page not suitable for main declaration - there is no description or apropriate image, we can add refering to product on cms.
:offers with binding to Products on cms
    - Pickup dirt with picture and description both in schema and page
    - Pickup wood ...
    - Pickup concrete ...
    - ....
    - Offers will be linked to prices page with a lot of offers with ids. Offer will be region based + offered by LocalBusiness - Yellowsack Brunch in...

Main problem - feedbacks it may be dangerouse to use feedbacks of yellowsack for all that products too...


Cons 
- splitted between pages, but google loves wise pages hierarchy - one page shouldn't respond for all demands and to let another pages be redundant it all should be linked to each other
- static - it may be difficult to support linking between pages=(
Pros
- product content present on page
- we will have pickup with rating and prices
- maybe cms feedbacks can ship to schema rating...
- faster then checkout page

### Yellowsack
We can be "local business" for each region? But it will split feedbacks between regions... It is logical, but still will require some efforts...
Hmmmmm... it supports departments as local business=) So we can have organization Yellowsack and departments Yellowsack in San Francisco and Yellowsack Los Angelles branch

Pros:
- we will be handeled by google separately - we will be on map of local services above search result, but bellow ads
    - holly cow... some scratch like http://junkremovalsamedayservice.com/ with localcompany name Default are above us...
- explicit regions separation
Cons:
- more efforts for supporting it...

### Shop page
I would like to try `CheckoutPage` if we would like to keep it opened for bots... It is custed away from our main content, content free, without apropriate navigation/linking. But after some investigations I changed my mind again - it would be suspicious to follow a lot of links from `app.yellowsack` to our checkout without showing google what is going on there.

### Breadcrumbs
It will show google/users our pages hierarchy, as for me must have...

## Links
[core - quality guidemap](https://support.google.com/webmasters/answer/35769#quality_guidelines)
[structured data guideline](https://developers.google.com/search/docs/guides/get-started)
