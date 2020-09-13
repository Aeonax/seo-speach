# SEO
## lil introduction
Search engine oprimization - from wikipedia it is process of improving site positions in search engines results, but it used to name this optimizations too.  

It is huge, it is old, it is magic... There is a lot of myths like we should use divs with actions for links to pages where we don't want to let google go. And there is really a lot of such theories - seo speciallists should do something during the work=D
<div style="display: flex; justify-content: space-between; align-items: center">
<img src="/images/screaming-cat.jpg" alt="Screaming cat">
<img alt="Head explosion" src="/images/explosion.png">
<img alt="Magic" src="/images/magic.jpg">
</div>

But it is 2020 and age of uncontrolled internet is passing away, hopefully SEO articles chaos will fade too...


## Why is it important?
After spending some efforts on optimizations we will get free relative new customers. They will come to us by themselves=) They will be relative - not region based/expensive as from marketing.  
#### What do we have now?  
- [San Francisco dumpster rental](https://www.google.com/search?q=san+francisco+dumpster+rental) - second page, would be cool to wisit yelp top 10... we are not in it=(
- [San Francisco junk removal](https://www.google.com/search?q=san+francisco+junk+removal) - ads, without ads on the end of second page. Yelp - we even not in this category=(
- [compare this queries in trending](https://trends.google.ru/trends/explore?date=2020-03-01%202020-09-03&geo=US-CA-807&q=dumpster%20rental,junk%20removal)
- [awfull query example](https://www.google.com/search?q=san+francisco+remove+my+junk) - from third to fifth page  

![Crying cat](images/crying-cat.jpg)


## What influencing on seo?
I couldn't know order of it and priorities/weight of each important part of search enging ranking. I'll try to represent it in my "logical" flow - from simplest parts to our engeneering area.  
All below info taken from google official documentation. I don't belive SEO specialists because had bad experience with them and their playing around trying to fool search engines.

### User behaviour
- behavior on the page. How tracked? google analytics
  - to mention awfull solution from russion SEO=((
- moving to another search results after visiting

### Content
- unique
- well organized
  - no thin or FAT pages and content spreaded all over the site
  - no doorways
  - smart links - it is easy to navigate got customer=)
- descriptive, but doesn't stuffed with everything possible
- it mirrowing customers desire/need and our benefits compared to competitors.

### Reachable and understandable by search engines
Google crawling our pages by google bots to get content from it. We can help them=)
#### Reach all required pages
- sitemap
  - [our](https://yellowsack.com/sitemap.xml), but without `app.yellowsack.com`
- "smart" links on pages - bots wil follow them and linking between pages improve page ranking, but we shouldn't think just about bots - it should be convinient for customers and google trying to count that too.
#### Block pages which we don't want to show google like user profile
- by noindex `<meta>` or Header
- rel on links which can tell what lays beneath that link - customer created/sponsored/?? content or bot just shouldn't go there
- robots.txt
  - [example](https://app.yellowsack.com/robots.txt)
  - [deprecated testing tool](https://www.google.com/webmasters/tools/robots-testing-tool)
- we shouldn't block js/css google using it too to define what is hidden from customers + acessibility rank + ???
#### Show what is going on on the page
- title/description
- headers
- alts
- structured data
  - schema.org
    - [testing tool](https://search.google.com/structured-data/testing-tool) but doesn't support spa
    - it doesn't like when schema describe content that is not on the page - we can reference it easily
  - rich results on google results page
    - [all supported types](https://developers.google.com/search/docs/guides/search-gallery)
    - [testing tool](https://search.google.com/test/rich-results)
      - it would be cool to compare several competitors from initial quering
    - it is not necessary to break our schema structure to be like google supported rich results

### Performace and another technical stuff
Google made browser extension - lighthouse which shows rating in several categories for page, all of them are influencing on page weight too.
And there is one close example with ukrainian marketplace(kasta.ua) - when they reworked pages from react to server side rendering(with keeping it dynamic - rendering parts of html on backend and placing them in to html when needed) they rised a lot in google.


## Now when we know what influencing on seo, what can we do with it?
### Content
#### We should understand what google benefits should we use - what our company structure or how do we wan't to present it.
We can use rich results feature to be brighter on results page.
We should decide we are LocalCompany OR Product OR ???.  
- LocalCompany with service sounds correct but it will not highlight prices in google results... We can show prices as "$" or "9-150$".
- Product will highlight prices dynamically but will not highlight feedbacks... We shouldn't use company feedbacks for it...

#### We should invent our "story" around choosen Seo strategic
- We are company that have departments in several regions and we are propposing dumpster bags and their pickups.
- We should describe that service - we should create entry points for our services like "dirt removal". It should be represented with page on which located some text with DIRT REMOVAL unique description/image.
- All pages should be smart linked, all our advantages should have their place in it.

### TECH - fill pages when content is ready
#### User friendly
yellowsack.com shouldn't be redundant entrance for app.yellowsack.com - it is our face and app.yellowsack is just checkout/profile. Newcomers should understand where are they and what should they do. Button order pickup should be understandable only for customers who know what is going on there. But each product related page should be understandable and lead to order - like "You can order `dumpster bag` or `pickup it`" but better and visible in or after text...
#### Improve google vision
- Include app.yellowsack to sitemap if we decide to keep it opened.
- Mark text - google pay more attention to `Hx` and images `alt`, we shouldn't use them as just text formatting - we should make separate classes for divs for such cases...
- More structured data with clever story and reverencing between pages.
- Page description
#### Optimizations
Lighthouse will guide us=)




## Possible data  
We should stop thinking of page that hauls everything what it can - we can [refer](https://www.w3.org/TR/json-ld/#advanced-concepts) nodes from another pages.
### pickups
Yellowsack pickup `Servie` - checkout page not suitable for main declaration - there is no description or apropriate image, we can add refering to product on cms.  
- :offers with binding to Services on cms
  - Pickup dirt with picture and description both in schema and page
    - Offers will be linked to prices page with a lot of offers with ids. Offer will be region based + offered by LocalBusiness - Yellowsack Brunch in...
  - ....

Cons  
- splitted between pages, but google loves wise pages hierarchy - one page shouldn't respond for all demands and to let another pages be redundant it all should be linked to each other
- static - it may be difficult to support linking between pages=(  

Pros
- customer friendly entrance - new customer shouldn't land on ordering page
- product content present on page
- faster then checkout page=)))

### Yellowsack
We can be "local business" for each region? But it will split feedbacks between regions... It is logical, but still will require some efforts...  
It supports departments as local business. So we can have organization Yellowsack and departments Yellowsack in San Francisco or Yellowsack Los Angelles branch.

Pros:
- we will be handeled by google separately - we will be on map of local services above search result, but bellow ads
  - holly cow... something like http://junkremovalsamedayservice.com/ with `LocalCompany` name "Default" are above us...
- explicit regions separation

Cons:
- more efforts for supporting it...

### Shop page
I would like to try `CheckoutPage` if we would like to keep it opened for bots... It is custed away from our main content, content free, without apropriate navigation/linking.  
After some investigations I changed my mind again - it would be suspicious to follow a lot of links from `app.yellowsack` to our checkout without showing google what is going on there.

### Breadcrumbs
It will show google/users our pages hierarchy, as for me must have... After we will reinvent our hierarchy.

## Pages hierarchy
- Yellowsack main - Yellowsack organization
  - Yellowsack in XX(SF...) - Yellowsack LocalBusiness + offers with prices related to region + refered to service
- Yellowsack bag :see_no_evil: Product with description and images
- Yellowsack pickup
  - Pickup XXXXX(dirt....), offers refered to LocalBusiness offers
- FAQ. google supports structured data and uses it in reach results. They should contain all response and be ready to fit google snippet and be used by customer to navigate in necessary place.
  - without errors!!!! Make Troy check it out or order someone to create/validate content=)))
  - without repeats!!!-_-
  - How to use(short(1,2,3) with link to how-to-use page)?
  - Contractors. What benefits will i get as contactor(with link to sign as contractor)
  - Can I buy bag without ordering pickup?=)))))
  

  - When will I recieve my Yellowsack? "We are doing our best to ship it within 24 hours, if we ship it by UPS and not our deiver it'll depend on ups, but usually to 3 days." - 2-3 days sux especially if we deliver it in one day.
  - Can i order pickup of non Yellowsack bag?
  - How can i get yellowsack? "In partners stores(link) or order it online(link to Product)."
  - What is the size of the Yellowsack? (more human text?)
  - delivery address question - we even haven't delivery address input :see_no_evil:
  - What benefits compared to dumpster rental - short with link to Service or more big description(would be better?=))
  
  <!-- - What benefits compared to waste removal -->
  <!-- - ... -->
- Stores... we should add some content to it-_- or prohibit from indexing... but as for me there is some place for content like... "We provide fast and free deliveries, but if you would like to take a look on it in live you can check out our partners shops: ..... If you would like to partner with us feel free to leave support request *here*"
- Check out our workday kinda lie - it is just instagram feed=( If i would like to check out our instagram i would follow the bottom link. But it may be cool to create story of drivers/trucks working day.

- add email to the bottom
- Maybe Troy should post fotos to yellowsack instagram too? instagram looks kinda dropped=( we need to do something with it?
