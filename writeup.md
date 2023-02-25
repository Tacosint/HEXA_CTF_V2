# Write-up HEXA OSINT CTF V2 - OSINT CTF

### By Eldwiin & R0ck3t & Tab & Zmondy - Team Tacosint

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image65.png" width="650" alt="Logo HEXA CTF V2"/>

# Contents

- [Write-up OSINT](#Write-up-OSINT)
    - [Challenges dependency map](#Challenges-dependency-map)
    - [Intro](#Intro)
        - [Welcome Back](#Welcome-Back)
    - [Action Man](#Action-Man)
        - [Hijacking](#Hijacking)
        - [Fast and Furious](#Fast-and-Furious)
        - [Fly me to the moon](#Fly-me-to-the-moon)
        - [Chocolate](#Chocolate)
        - [Tank Engine](#Tank-Engine)
        - [Bonbon](#Bonbon)
        - [Sovereign City](#Sovereign-City)
        - [Original](#Original)
        - [Final countdown](#Final-countdown)
    - [The Lawyer](#The-Lawyer)
        - [The law firm](#The-law-firm)
        - [The lawyer](#The-lawyer)
        - [Alias](#Alias)
        - [Trustworthy](#Trustworthy)
        - [Herbaceous](#Herbaceous)
        - [Good time](#Good-time)
        - [Decentralized](#Decentralized)
        - [Kanagawa](#Kanagawa)
        - [Experts](#Experts)
    - [The Developer](#The-Developer)
        - [Programming](#Programming)
        - [Listen to your heart](#Listen-to-your-heart)
        - [The Associate](#The-Associate)
        - [Contract](#Contract)
        - [Impersonator](#Impersonator)
        - [Setup](#Setup)
    - [The Intruder](#The-Intruder-Challenge)
        - [The Intruder](#The-Intruder)
        - [Infiltration](#Infiltration)
        - [Sneak beak](#Sneak-beak)
            - [Challenge 1](#Challenge-1)
            - [Challenge 2](#Challenge-2)
        - [Grow owlder](#Grow-owlder)
            - [Challenge 3](#Challenge-3)
            - [Challenge 4](#Challenge-4)
            - [Challenge 5](#Challenge-5)
        - [Tell me owl your secrets](#Tell-me-owl-your-secrets)
            - [Challenge 6](#Challenge-6)
            - [Challenge 7](#Challenge-7)
            - [Challenge 8](#Challenge-8)
        - [Owlmost there](#Owlmost-there)
            - [Challenge 9](#Challenge-9)
            - [Challenge 10](#Challenge-10)
            - [Challenge 11](#Challenge-11)
        - [Cowl me maybe](#Cowl-me-maybe)
    - [Sidequest](#Sidequest)
        - [He is back](#He-is-back)
        - [He is back 2](#He-is-back-2)
- [Rapport](#Rapport)
    - [Mission Analysis](#Mission-Analysis)
    - [Mastermind Analysis](#Mastermind-Analysis)
    - [Associate analysis](#Associate-analysis)
    - [Action Man Analysis](#Action-Man-Analysis)
- [Maltego](#Maltego)


# Write-up OSINT

## Challenges dependency map

The unlocking order of the challenges provided by the organizer is the following:

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image23.png" alt="" />
<br/>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image76.png" width="650" alt=""/>
<br/>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image61.png" width="650" alt=""/>

## Intro

### Welcome Back

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image80.png" alt=""/>

The first challenge is to set the context. Nothing complicated here, just copy the flag: **HEXA{Briefing_OK}**

## Action Man

### Hijacking

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image16.png" alt=""/>
<br/>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image17.jpg" width="700" alt=""/>

With the statement, we had a photo. All we had to do was to perform a reverse image search with Google Lens.  
This one tells us that it is the “Tribunal Judiciaire de Versailles”. The flag is **
HEXA{Tribunal_Judiciaire_de_Versailles}**.

### Fast and Furious

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image31.png" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image111.jpg" width="650" alt=""/>

For this challenge, we also had a photo. However, with Google Lens, it doesn't give us much. On the right side of the
picture,
there are signs for the place written in French. We can then search the place with Google Maps thanks to this.
We arrive easily in the surroundings by searching "Meudon D57" on Maps. We look for an intersection near a tramway stop.
We look at some intersections with the Street View mode and find this one corresponding to the picture we are looking
for.
https://www.google.fr/maps/@48.7802802,2.1907343,3a,75y,63.83h,85.23t/data=!3m6!1e1!3m4!1sSW--njUUkGWoZhYIAkL7Jg!2e0!7i16384!8i8192

Flag: **HEXA{Avenue_du_capitaine_tarron}**.

### Fly me to the moon

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image43.png" alt=""/>

A picture of the evidence found at the safehouse was provided with this challenge:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image57.png" width="650" alt=""/>  
We can read on the paper on the left:

```
pictures + flight
14/12/2022

Oleg,
I attached the pictures → Print them for your passport.
You know where to reach me.
I attached your flight for tomorrow.
See ya.
```

With the picture, we can read a code: FSF145P. By making the link between those two, we searched for flight n°FSF145P:

- https://www.radarbox.com/data/flights/FSF145P
- https://flightaware.com/live/flight/FSF145P

It looks like they were heading from Paris to Payerne and the plane went back to Clermont-Ferrand after it.  
Flag: **HEXA{Payerne}**

### Chocolate

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image19.png" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image77.png" width="650" alt=""/>

We can see on the picture that there are tramway tracks in the picture and some shops called `[...]ETSCH`
and `[...]alle Wo[...]`.

There are 4 cities with tramways in Switzerland: Basel, Bern, Geneva and Zürich.
When searching names ending with `ETSCH` using a tool like https://www.dcode.fr/words-ending-with, we find a list of 14
words in German:
KETSCH, FLETSCH, KNETSCH, PIETSCH, QUETSCH, SKETSCH, KNIETSCH, PLIETSCH, QUIETSCH, ABQUETSCH, BORRETSCH, DOLMETSCH,
ZERQUETSCH and PLAUTDIETSCH.

When searching shops in Switzerland containing these words, we can find one called `Dolmetsch AG` in Zürich, on
Limmatquai Street.
https://www.google.fr/maps/place/Dolmetsch+AG/@47.3757964,8.5433349,20.5z/data=!4m6!3m5!1s0x479aa0a81b33fcb9:0x3c1f431f2ee5f917!8m2!3d47.3756737!4d8.5438018!16s%2Fg%2F1tf7r2td?hl=fr

Flag: **HEXA{limmatquai}**

### Tank Engine

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image72.png" alt=""/>

After searching multiple ways to get this information, we typed “direct train connections” in Google or DuckDuckGo. The
first link points to https://direkt.bahn.guru/.
When you search direct connections from Zurich, we can find one yellow dot indicating 3h07 in the south of Switzerland:
Cadenazzo.

Flag: **HEXA{Cadenazzo}**

### Bonbon

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image88.png" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image98.jpg" width="650" alt=""/>

By analyzing the EXIF metadata of the picture provided with the challenge, we find GPS coordinates in Chania, Greece:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image115.png" />

There are not many airports nearby but we can find an international one in Heraklion called “Níkos-Kazantzákis”, 142 km
east by road.

Flag: **HEXA{nikos_kazantzakis}**

### Sovereign City

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image97.png" alt=""/>

In this challenge, the first question we asked ourselves is “What is a way, a node and a relation ?”. A quick search on
Google with “way node relation number” let us know that OpenStreetMap elements use this kind of nomenclature. The help
forum lets us know how to request for ways, nodes and relations. From this, the following links help us determine where
they were:

[They arrived here: ](https://www.openstreetmap.org/way/646940106#map=14/1.3254/104.0077) 
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image3.png" width="350" alt=""/>

[They hide here:](https://www.openstreetmap.org/node/1803847939)  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image55.png" width="350" alt=""/>

[They changed car here: ](https://www.openstreetmap.org/way/22762642#map=14/1.4332/103.7970) 
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image44.png" width="350" alt=""/>

[And they turned here: ](https://www.openstreetmap.org/relation/8810294#map=14/1.4161/103.7838) 
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image85.png" width="350" alt=""/>

The neighborhood where they hide is Hougang (it is a little small on the screen, but it is more visible via the link).
From the last turn they took and assuming that they stayed left after that one, we can see where they were going. They
were going north of Singapore, to Johor Bahru.

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image67.png" width="650" alt=""/>  

So the flag is **HEXA{hougang_JohorBahru}**.

### Original

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image36.png" alt=""/>

For this challenge, we began by thinking “what could be the main difference between a machine and a human?” The first
one that came to our mind was that a machine does what it is supposed to do, without making mistakes, or if it made one
mistake, it should be present in all the reports written by the machine. So in this case, a machine shouldn’t make any
error writing the report (or always the same error) whereas a human could do one. Following this lead, we used the
tool https://www.onlinecorrection.com/ to check each report to see if there was a mistake.
One report had a slight error (the placement of a coma) and another one had a real error: `For this crimes` instead
of `For these crimes` (even my text editor is asking me if I am sure about the first sentence). This is typically the
kind of little mistake a human would make. The concerned report was number 8.
So the flag is:  **HEXA{8}**

### Final countdown

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image102.png" alt=""/>

This challenge was the one that had the most revamp during the CTF. Indeed, at first it had 5 tries allowed, and the
text was a bit less explicit. We first thought we needed to find an OSM building but it turned out we were looking for a
node with a building attribute. The perfect way to do this kind of search was to use overpass turbo which relies on the
OpenStreetMap API.
Before going on overpass turbo and kicking some queries in, we first need to figure out what this “zone 4” is. Luckily
for us, we already did the Herbaceous challenge before. On the website, there was a kmz file which contained only a kml
file with several zones. Zone 4 was in Malaysia, south of Kuala Terengganu.
To open the KML file, either you can use the base app from your system (if it has any), or create a my map Google like
this one:
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image92.png" alt=""/>

Going on overpass turbo, we start by drawing the zone we want to search in (using
the <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image49.png" alt=""/> button on the
left of
the map).
Now, it is time for us to create the query. First, we only searched for places of worship, and football fields, but it
turned out not to be very effective. So using some tutorials on how to use this tool, we manage to create our own
request:

````
[out:json][timeout:800];
// query part that looks for building which is related to religion and names it “religious”
(
      way["religion"]["building"]({{bbox}});
    relation["religion"]["building"]({{bbox}});
    node["religion"]["building"]({{bbox}});
)->.religious;
  
// query part that looks for pitches and names it “soccer”
(
    way["leisure"="pitch"]({{bbox}});
    relation["leisure"="pitch"]({{bbox}});
    node["leisure"="pitch"]({{bbox}});
)->.soccer;
// Now, let’s only select religious buildings that are within 500m of a pitch
nwr.religious(around.soccer:500);

// and print it all out !
out body;
>;
out skel qt;

````

The result gives us three points. However, the challenge specifies that the building is far from the sea (at least 3 km
by feet). A little google map search let us see that only one building fits this description.
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image8.png" width="1500" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image71.png" alt=""/>

The flag is **HEXA{3975813161}**

## The Lawyer

### The law firm

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image100.png" alt=""/>  

In this challenge, the aim was to find the domain name of the company. The main hint was the name of the company.
Given that, we went on who.is to check which “nelexat” domain was taken. It taught us that nelexat.io was the only
common one taken. However, accessing this website didn’t work, so the domain we are looking for is not this one.
Reading the challenge again, another piece of intel that was given to us was the country of the company: Switzerland.
The TLD (top level domain) of switzerland is “ch”. A visit on nelexat.ch let us know that we found the right website.
Scrolling to the bottom of the first page, we can find the flag we were looking for: **
HEXA{N3l3x4t_w1ll_M4ke_You_R1ch}**

### The lawyer

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image28.png" alt=""/>  

The most famous social network where one writes where he went to school is LinkedIn. That’s where we started our
research on this challenge. The only piece of information we had was the company our lawyer was from. Searching for
“nelexat” show us 2 people. Initially, the first time we arrived here, there was only one, the one working in Zurich.
The localization of the company would also help us identify which one was the one we were looking for.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image47.png" width="650" alt=""/>

This doesn’t help us a lot... However, by looking at the filters available, we can discover some interesting
information.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image96.png" alt=""/>

To determine which school our target went to, we need to filter them one by one. Doing so, we can see that he went to
King’s College London and to “Faculté de droit de l’université de Neuchâtel”. However, at this moment of the
investigation, we can’t be sure which one of the 2 remaining schools he went to first. By trying them, the flag reveals
himself: **HEXA{london}**

### Alias

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image59.png" alt=""/>

This challenge was the last one we managed to resolve. For the record, we flagged it 22 seconds before the end of the
CTF. From the previous challenge, we had the LinkedIn of the lawyer. However, we couldn’t access his profile. To be able
to access his profile, we used intel we gathered from other challenges. From the herbaceous challenge, we know the
lawyer’s initials (L. N.), and from the impersonator, we know that someone in the team is named Lian. It looks like our
lawyer’s name might be Lian. By adding the filter “Lian” as a name in the LinkedIn search, it allows us to see the
profile link and click on it.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image66.png" alt=""/>  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image103.png" width="650" alt=""/>

On his profile, we can see a bunch of posts, however, one is more interesting for us than the others, because it
contains a useful piece of information, his pseudonym: Nelexlian.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image81.jpg" width="650" alt=""/>  
With his pseudonym, we can now search for a trading platform where this lawyer is giving his advice.
We had already searched on google "trading platform social media" to get names of the main trading platforms with a
social media aspect, where Lian can possibly share advice with other users.
The one that stands out in many rankings was Etoro.
We created a fake account on it and kept the website aside, until we found Lian's pseudonym and tried to search for "
Nelexlian" in the eToro search bar. We found this account https://www.etoro.com/people/nelexlian. In the "About
Nelexlian" part, we can find the flag **HEXA{nelexlian_is_rich}**.

### Trustworthy

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image51.png" alt=""/>

This challenge was about a hidden email on the website. The statement here says that the email address is hidden. It
could mean two things. Either the email address is hidden by the target for it not to be found, or the email is in a
place the target wouldn’t think of. First, we tried to find some “hidden places” on the website. By going on any other
pages than the home, we can see the website going to https and we can see that the certificate is from an unknown
issuer. What could go wrong? We tried to go to page 404 of the website, which let us know the website is using Wordpress
as a CMS, and that an article “Bonjour tout le monde !” was written by ``admin4847``. At this moment I thought again
about
the HTTPS and the certificate thing. By clicking on the lock on the address bar, I looked at the certificate. As I
started to suspect, the field email address of the certificate’s subject was filled.  
The flag was: **HEXA{mastermind_mastermind@proton.me}**

### Herbaceous

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image75.png" alt=""/>

The last challenge gave us an email address. To find out for which services an email address is used, we decided to use
the (famous) tool epieos. We also could have used holehe to do so. This tool lets us know that the email address
mastermind_mastermind@proton.me has a google account. In addition to that, it also gives us the maps contribution link
and the calendar link. The maps link shows that mastermind has left no reviews on google maps. However, the calendar
link is much more interesting. Indeed, on the 16/12/2022, there is a meeting planned at 12pm.

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image15.png" alt=""/>

By clicking on more details, we can see the whole text which gives us an onion
link: http://nvnomrsfvy3dcq25c5y2stgbptt4dcuiaidugy63zca2vc5vnhetaoad.onion/
This kind of link can be opened with the TOR browser.
If you click on more details while being connected, it opens the details of the meeting as if it was an invitation,
allowing us to see who else was invited. 2 other people were invited: mincah_mm@proton.me and vok_0lski@proton.me.
For the end of the challenge, let’s go to the onion website. The first page is only a text containing a crypto address (
useful for the next challenges) and an image with a link to another page “zones”. The zones page only contains a link to
download a kmz file (zip file containing geo data). To be sure that nothing was hidden, a look at the source code with
the developer console let us see the flag as a comment on the home page: **HEXA{N3l3x4t_is_L1nk3d_to_M4stermind}**.

### Good time

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image34.png" alt=""/>

Searching the different nicknames of the people invited in the calendar event (“mincah_mm” and “vok_0lski”), we found a
Tripadvisor account of Minca H https://www.tripadvisor.com/Profile/mincah_mm. The account made a review in a restaurant
in Zurich, the “Kaufleuten”.  
So the flag is **HEXA{Kaufleuten}**.

### Decentralized

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image93.png" alt=""/>  

The crypto address we found in the challenge Herbaceous is going to be useful here. The crypto address
is: ``0x64D0D945AE5a384c18A3876064816b7E141980E7``.  
A search on blockchain.com let us know that the address is an ethereum one. For ethereum addresses, etherscan is better
than blockchain.com, so here we go. We can see that several transactions have been made to this address (initially there
was only the older one.).  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image48.png" alt=""/>

By looking closer, we can see a star near the method used on this specific transaction (we only found it out later, it
means that the transaction includes data that may be an utf-8 message).
Going on the transaction details, we can see the input data. The drop down allows us to see this data as utf-8.
It reveals us a message from the initiator of the transaction:
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image64.png" alt=""/>

The flag is: **HEXA{bruised_rogue}**.

### Kanagawa

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image45.png" alt=""/>  

In the challenge statement it’s written that the cryptocurrency address found is used for something else.
One of the first things that come to mind is the NFT world. With a simple search on DuckDuckGo “famous cryptocurrency
platform nft”, this link appears:
https://www.fool.com/the-ascent/cryptocurrency/nft-marketplaces/.  
And on this webpage that lists the Best NFT Marketplaces, https://opensea.io/ is the first shown. Then in opensea, there
is a search bar where it’s possible
to paste the cryptocurrency address:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image114.png" alt=""/>

Thanks to that, a “Mind_master” profile appears which contains only one NFT. On this one, there is a description that
contains the flag **HEXA{n1ce_L0g0_br0}**.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image84.png" width="" alt=""/>

### Experts

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image90.png" alt=""/>

When looking at every page of Nexelat’s website, we found an API on https://www.nelexat.ch/index.php/our-advices/. Dark
Reader’s dark theme was very useful as text remained white but the background was changed so we saw it directly.

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image52.png" alt=""/>

As it is a FastApi, we are searching for a Swagger file referencing all the endpoints. Thanks to the
doc (https://fastapi.tiangolo.com/tutorial/first-steps/) we know it is available under the ``/docs`` endpoint.

On http://217.182.69.14:8000/docs, we can search for cases using clients names, or missions using mission names. As we
know one of the clients, Lucilhe Dumarquais, we can try to execute a request on:
http://217.182.69.14:8000/cases/{client_last_name_lowercase}?name=dumarquais

It returns:
> {
> "name": "dumarquais",
> "description": "This case is related to Lucilhe Dumarquais, head of Manipar organization, which was organizing a data
> traffic. After a bitter battle with the opposing lawyers, I managed to get a lighter sentence in a prison in France,
> without my client having to give any information about the people she was working with. HEXA{s3cure_y0ur_d4mn_4p1}"
> }

Flag: **HEXA{s3cure_y0ur_d4mn_4p1}**

## The Developer

### Programming

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image42.png" alt=""/>

We are looking for an account for an IT project. The first idea we had was to go on GitHub and search if we couldn't
find a project named "Nelexat". However, no relevant result.  
If the developer used Git to do his versioning, we may be able to find traces on the site. Our second idea was to check
if the site was published with the development information. These are contained in a “.git” folder in the project
directory. So we searched for the URL https://www.nelexat.ch/.git and it exists! We will be able to find the elements we
are looking for.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image35.png" alt=""/>  
We had a config folder, https://www.nelexat.ch/.git/config, and it contains developer information.

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image12.png" alt=""/>

We can now search for the developer's name on Github and find his profile page: https://github.com/OVokolska.   
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image110.png" />  
Flag: **HEXA{https://github.com/OVokolska}**.

During our research, we were able to investigate the .git on the site. To do this, we retrieved the .git folder with the
wget command:
> wget --mirror --no-check-certificate https://www.nelexat.ch/.git

Now that we have retrieved the elements, we can dig into the site. With the "branch" command, we see the different
branches available in the directory. We see the “master” branch, which is the main branch, and another branch called "
feature-live-chat". This one catches our eye.

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image106.png" alt=""/>

So we’re going on it.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image91.png" alt=""/>  
We look at the latest changes made to the branch.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image11.png" alt=""/>  
We are interested in the last commit made. We can see the changes that have been made. Two lines have been removed and 3
lines have been added. The deleted lines are about a woman with hazel eyes. This information helped us in the analysis
requested at the end of the CTF.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image83.png" alt=""/>

### Listen to your heart

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image79.png" alt=""/>  

The developer's github page is not very active. However, we found two things: in his bio it says "littleSparr0w" and he
liked a Mastodon web client project. We first tried to search accounts with the username “OVokolska” but no conclusive
results. Then, we searched for the nickname “littleSparr0w” and an account caught our attention, a Mastodon account:
https://cyberplace.social/@littlesparr0w.  
By going to the URL, we find the flag: **HEXA{mY_H34R7_i5_pURp13}**.

We also noticed that the message had been modified and before containing the flag, it was referring to a link.
However, we did not have time to investigate this link further.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image70.png" alt=""/>

## The Associate

### Contract

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image20.png" alt=""/>  
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image29.png" width="650" alt=""/>  

By looking at the EXIF of the image, we recover a date (24/11/2022 13:17) and also the time zone of the country in which
it was taken (UTC+4). On the image, we can see numbers "14 32" written on the floor, indicating the orientation of the
runway.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image94.png" />  
Then, we searched for countries in the UTC+4 timezone with an airport with “14/32”. The search "aéroport 14/32 Maurice"
brings us to an airport corresponding to the photo taken: **HEXA{Maurice}**.

### Impersonator

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image89.png" alt=""/>  

As the challenge says, we need to use the “world's largest Open Database of Cell Towers”. Then, we search for it and
find https://opencellid.org.

To find a phone on it, we need 4 items: MCC, MNC, LAC and Cell ID. As we already have the last two, we have to find the
MCC and MNC knowing the antenna operator: EE (previously Orange S.A.) and the prefix number: +44 (corresponding to UK)
.  
To find correspondences, we opened https://mcc-mnc.net/. There is only a two in UK, owned by EE:

- MCC = 234 / MNC = 33
- MCC = 234 / MNC = 34

When entering the following parameters in OpenCellID: MCC = 234 / MNC = 33 / LAC = 11 / Cell ID = 27855, we find a
location in Chelsea.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image10.png" alt=""/>

Flag: **HEXA{Chelsea}**

### Setup

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image58.png" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image82.jpg" width="650" alt=""/>  

This challenge is pretty simple, we just had to turn the image and do a search via Google Lens on the watch. We got
“Montre Festina Homme Chrono Acier Cuir Bleu F20286/3”.  
https://fr.shopping.rakuten.com/offer/buy/2425062830/montre-festina-homme-chrono-acier-cuir-bleu-f20286-3.html  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image101.png" width="650" alt=""/>  
The flag is **HEXA{F20286/3}**.

## The Intruder

### The Intruder Challenge

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image39.png" alt=""/>

First, we searched for a famous detective born in 1819. Without searching very far, we found Allan **Pinkerton**, who
made one of the most famous detective agencies.  
After searching for hours for Pinkerton on Youtube, we decided to read the challenge statement once more. But this time,
instead of giggling at “He could be among us”, it made sense: What if it broke the 4th wall and Pinkerton was really
among us for the CTF?

We searched for Pinkerton among the users of the CTFd.   
Eureka! There he was, with a link pointing to his Youtube
channel: https://hexactf.ctfd.io/users/109  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image9.png" alt=""/>  
https://www.youtube.com/channel/UCjyLqrOsjkpsMhczlbHJoFA

Flag: **HEXA{UCjyLqrOsjkpsMhczlbHJoFA}**

### Infiltration

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image25.png" alt=""/>

On Pinkerton’s Youtube channel, we can find a short video (https://www.youtube.com/shorts/nhh7Z8gnDmA) with the alias of
what looks like a TikTok account (``@user545947198194``).  
In the description of this account, we find a link to a discord server: https://discord.gg/unsb62pMc7.  
When joining the discord server, we find the flag in the welcome message.

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image21.png" alt=""/>

Flag: **HEXA{P1nk3Rt0n_solV1n9_C4s3}**

### Sneak beak

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image63.png" alt=""/>

On the Discord server it was needed to resolve small challenges to access a more privileged role in the goal to meet
Pinkerton. To obtain the first role, it was needed to solve two challenges:

#### Challenge 1

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image5.png" alt=""/>

The first challenge included a .mp4 video with a fixed black picture. Nevertheless, it was the audio which was
interesting.
Indeed, a person was singing something. At the second 14 we can hear the only lyrics “Catolina”. This lyric is
absolutely
not useful because it’s the only one and OSINT searches gave nothing interesting. The smart part was to use a music
recognizer like the Google assistant. Thanks to the context of the music variation around the lyric, Google retrieved a
list that potentially corresponded to this music. The first was Lemonade from the bonobos group which corresponded at
8% of the music. Before entering the flag, it was important to listen to this music to confirm the recognition.
And indeed it was this one.  
The flag was then **!c1-lemonade-bonobos**.

#### Challenge 2

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image74.png" alt=""/>

For this challenge, it was necessary to do a search with DuckDuckGo or Google with the key word in French of the
statement
“usurpation d'identité france code penal”. This one gave a link
to https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000042193593/ which included the article number.  
The flag was **!c2-226-4-1**

Finally, after giving those two flags, the bot gave the command **!yxmdvbn5jvwnnjy3htfe** to have the next Discord
role.  
The flag was then **HEXA{!yxmdvbn5jvwnnjy3htfe}**.

### Grow owlder

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image107.png" alt=""/>  
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image6.png" alt=""/>  

Ok, let’s go for 3 more challenges.

#### Challenge 3

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image86.png" alt=""/>

For this challenge, we had to find an article of a European law about data collection. It looks like we are searching
an article of the GDPR about data deletion.
When searching “GDPR deletion”, we find: https://gdpr-info.eu/art-17-gdpr/ about the right to erasure.  
Answer: **!c3-GDPR-17**

#### Challenge 4

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image105.png" alt=""/>

For this challenge, a research on google with the keywords “egg change October 2022 November USA month by month” led us
to find this website. Here, we can have the price of eggs per month. In October 2022 it was 3.419 and in November, it
was 3.589. From those information we can infer that the price of the eggs changed by (3.589 - 3.419) / 3.419 * 100 =
4.97…%  
However, this answer doesn’t work, there must be another way to find what Pinkerton is looking for.
To do so, a quick search using another search engine (bing) and the search “egg price US november up” let us find this
article that let us know that “Egg prices jumped 2.3% just in the month of November, and by 10.1% in October, according
to the CPI”.  
Answer: **!c4-23**

#### Challenge 5

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image54.png" alt=""/>

We are searching for a webcam in Veneto. Most of our research is pointing to https://www.skylinewebcams.com. After a few
minutes on this site, we find a webcam which looks like the one we are searching:
https://www.skylinewebcams.com/fr/webcam/italia/veneto/venezia/chioggia-sottomarina.html
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image26.png" width="650" alt=""/>

We can clearly see a panel where “Fantasy” is written.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image46.png" alt=""/>

We find the name of the hotel at the top of the video: Hotel Ambasciatori.
When we search Hotel Ambasciatori, Veneto, Chioggia on Google maps, we find it, near Pizza Fantasy! Their phone number
is +390415540660.  
Answer: **!c5-390415540660**

### Tell me owl your secrets

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image69.png" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image13.png" alt=""/>

#### Challenge 6

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image4.png" alt=""/>

For this challenge, we went through a hard time. We only had a surname and a name, and that the guy is japanese.  
First, we tried some combination of the name and the surname to create an alias he could have used to search it
via whatsmyname.app. However, nothing came up. We thought that the name sounded strangely familiar, and so we used
the email address tsuyo63@proton.me we found during the challenge Decentralized. Nothing came up neither via holehe
nor via epieos. At this moment, we thought that maybe the fact that the guy was Japanese should be a better help than
just trying to translate his name and googling it. So we searched what is the most famous social network used in Japan,
and apparently Line was one of the most used. So we tried to install Line, but to do so, we needed to use a phone number
to receive the confirmation code and to do the inscription. It was a little problematic because we had no phone coverage
where we were located so we had to run outside (it was kinda cold) to receive the sms.  
Once the registration was complete, we searched for TsuzuneYokoyama and found the graal we were looking for:   
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image41.png" height="650" alt=""/>

Google Lens translates this to: “Life is good at 59, 21 March”.
So Tsuzune Yokoyama was born on 21/03/1963 which sounds kinda like tsuyo63, confirming our hypothesis.  
The flag is: **!c6-21031963**

#### Challenge 7

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image24.png" alt=""/>

Challenge pretty easy here, you must first activate the Developer Mode in the Discord settings.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image87.png" alt=""/>

After that, right-click on the profile image, and “Copy ID”.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image95.png" alt=""/>  
Command: **!c7-1055577878022070302**.

#### Challenge 8

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image60.png" alt=""/>

We can see on the video the end of a MAC address: “9E:A9:75” and a website where we can read “Draytek”.
So we started by searching the MAC address of a Draytek router.  
On https://maclookup.app/vendors/draytek-corp, we found 3 OUI corresponding to DrayTek:

- 14:49:BC
- 00:50:7F
- 00:1D:AA

We then searched a network corresponding to this MAC address on https://www.wigle.net/.  
We found an ssid with MAC address 00:1D:AA:9E:A9:75 which is called “LGNF Health Inovative Ltd - Guest”  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image32.png" alt=""/>

Answer: **!c8-LGNFhealthinovativeltd-Guest**

Command to get the Tengmalm role: **!dzuf1i2ufe63wv5fscmt2x8pyyilrm**  
Flag: **HEXA{!dzuf1i2ufe63wv5fscmt2x8pyyilrm}**

### Owlmost there

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image2.png" alt=""/>

#### Challenge 9

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image18.png" alt=""/>
<br>
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image62.png" alt=""/>

In the first place, we tried to find the bullet using Google Lens or search by image but we couldn’t find a match with
the same dimensions.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image104.png" />

We are searching for a bullet with a probable cartridge diameter of 7.62mm as it is a very common diameter with a length
of 24 or 25mm.
With those dimensions, we find the 7.62x25mm Tokarev caliber which looks like the one we are searching for.

Answer: **!c9-762-tokarev**

#### Challenge 10

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image112.png" alt=""/>

For this challenge, we need to find what this A-Team is. But the first thing that struck us was the use of the term
“winding up”.
This term is used for companies, so this A-team should be a Mauritian company. We used the website opencorporates to
search for A-team that exist in Mauritius. There were 3 companies, however one is still active, so it shouldn’t be the
one we are looking for. However, OpenCorporates doesn’t give us the winding up date for these companies. To do so, we
had to go on the website from which the data came. Opencorporates gives us a link to the original data.
It was a bit broken so we had to delete the path to go directly to the home page. From there, we searched
for A-team and looked one by one at the 3 companies that were returned. For the A-Team Security Ltd, there
was a winding up date that occurred in 2014, just like our mauritian friend told us.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image27.png" alt=""/>

So the flag is **!c10-18-06-2014**

#### Challenge 11

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image50.png" alt=""/>

The first reflex was to search "させつ。はばとび。はなよめ" on google.  
The first result link was https://mapfan.com/spots/SC353,J,87. On this webpage, the coordinates of the location were
written: 35.295554 139.5804492. By putting them in Google Maps, we go to the location in this application. Then,
the first reflex was to search FM radios around this area. The nearest result was ShonanBeach FM 78.9:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image37.png" width="650" alt=""/>

By adding 78.9 MHz and 500KHz, the result was 79400 KHz (and not 079400 like the format example mentioned with the 6
digits).  
The result was then **!c11-79400**

### Cowl me maybe

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image99.png" alt=""/>

The last challenge is available on the discord with the last role that we unlocked via the previous three challenges:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image22.png" alt=""/>

Which e-mail address was used by the client who ordered MM mission ? First, who is MM ? MasterMind. How was the mission
ordered ? We learned it through the challenge Herbaceous taught us that the client should use the crypto address to
contact MM. Furthermore, during the challenge Decentralized we saw an email address being transmitted with a mission
name. The mission name was linked to the main operation we were working on via the API we found for the challenge
Experts. So the email address we are looking for is ``tsuyo63@gmail.com``. We also found a link between this email
address
and the japanese guy Pinkerton was looking for, Tsuzune Yokoyama born in 1963. In addition, on the paper of the
challenge Setup we can see the operation bruised rogue being asked by Tsuzune Y.
So we called Pinkerton and said the email address out loud, and a recorded voice answered us with some information about
the case. Following are the notes we took during the talk:
The case is a crazy one where Lucilhe, arrested in 2021 escaped. The operation was planned by MasterMind, which is a
company that provides criminals services in exchange for services later. The chief of MasterMind is Minca H, a business
woman with long wavy red hair with venetian highlights.

## Sidequest

### He is back

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image73.png" alt=""/>

Please not him. Back to 2022, the Kermit challenge gave some PTSD to the team, and apparently, he is back. The most
complicated thing here was to understand the challenge statement.  
It was important to divide the sentences to translate them into simpler words:

* The third of his name refers to the grandfather’s person
* There are lots of events called “The great war”, even in Game of Thrones, but when we did some research about this,
  the first related event was the First World War.
* Seeing the organization of the sentence, the second novel could refer to either his grandparent or him.
* His second novel would be adapted into a movie and there is a small interesting fact about the adaptation of the main
  character

Those fourth points bring lots of, too much information to do the searches. There were lots of great wars, lots of
different Kermit, lots of people that made novels… So we decided to keep it simple and took the first person that came
regularly to the results of our searches: Kermit Roosevelt. The key word for this search was “kermit first world war”.  
After analyzing his Wikipedia page, we read that he has a child, Kermit Roosevelt Jr who also has a child, Kermit
Roosevelt III. To sum-up their direct link, we created a short family tree:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image108.png" height="450" alt=""/>

By taking back the information of the challenge statement, Kermit Roosevelet wrote some books after WW1 and has a
grandson called Kermit Roosevelt III.  
The next step was to find the second novel. In the wikipedia page of Kermit Roosevelt III, we learnt in the “Reception
of novels” and “Fiction” sections that he wrote 2 novels. The second one “Allegiance” was the one searched.  
At this step the idea was to find an article which described the personal opinion of Kermit Roosevelt III to match the
challenge statement part ”about the actor he will see to take the role of the main character in a movie theater". For
that, a simple Google search was used “Kermit Roosevelt III "Allegiance" interview”. This one gave a bunch of websites,
and thepenngazette.com was interesting. This article talked about the work of Kermit Roosevelt III. By searching some
information by the keyword “character”, we found, like in the Wikipedia page, a section describing some actors. In the
7th occurrence of this keyword, a certain “Franck Langella” appeared:  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image68.png" alt=""/>

Franck Langella was an interesting finding because we already saw him in the Wikipedia article. The reflex was then to
do another Google search with this actor, because he perhaps also appeared in the second novel adaptation but was not
mentioned in the Wikipedia page for some reason.  
So “Kermit Roosevelt III "Frank Langella" "allegiance"” was used for another Google search and one of the first links
after Wikipedia's one was harvardwood.org. In this article, searching by the keyword “Franck Langella” was not so
interesting because he only appeared in the introduction part. The second search was with the “Allegiance” keyword that
was much more logic in this context. By reading the text located after this keyword, we read that Kermit Roosevelt III
wanted to see the caracter Cash Harrison played by a Joseph Gordon-Levitt.  
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image40.png" width="650" alt=""/>  
This statement was exactly what the challenge explained.  
The flag was then: **HEXA{Joseph Gordon-Levitt}**

### He is back 2

<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image116.png" alt=""/>

For this challenge, we know that we are looking for a chemical that has three cyclohexane and one cyclopentane as
compounds.  
A google search with the request `”three cyclohexane” “one cyclopentane”`let us know that “The steroid nucleus, sterane,
is composed of three cyclohexane rings and one cyclopentane ring.”
Wikipedia helps us understand what steroids are, and also that its nomenclature is “Gonane, also known as steran or
cyclopentanoperhydrophenanthrene”.   
The challenge asks us the scientific name of the recipe, and as we all know, scientific names are always the ones you
can’t say out loud without your furniture starting to levitate (or the more specific, depending on the point of view)
.   
The flag is **HEXA{cyclopentanoperhydrophenanthrene}**.

# Rapport

## Mission Analysis

Mastermind's mission to exfiltrate Lucilhe is called "Bruised Rogue".
The mission was commissioned by a Japanese man named Tsuzune Yokoyama. He contacted Mastermind through the ethereum
address available on Mastermind's onion site.  
The objective of the mission is clear, to make Lucilhe Dumarquais escape during her transfer to court. He wants to
recruit her because of the skills she has shown in Manipar. However, if anything goes wrong with the mission, the order
is clear, Tsuzune Yokoyama's identity comes first and Lucilhe Dumarquais must be eliminated.  
This mission began in 2022 when the law firm Nelexat took over Lucilhe's case. This case is not usually one they work
on (they are tax lawyers). This allowed Mastermind to recover information about the transfer during which the escape
took place.  
The man who helped Lucilhe escape from the Versailles court is a certain "O. Vokolski", answering to the pseudonym "
action-man".  
They then took a plane from Clermont-Ferrand to Zürich, on Limmatquai Street. There they met Lian Nussbaumer, Lucilhe's
lawyer.  
From Zürich they took a train to Cadenazzo from where they took a boat to the safehouse in the town of Chania in Greece.
Once on the island, they flew to Heraklion Níkos-Kazantzákis International Airport to catch a flight to Singapore Changi
Airport.  
Once in Singapore, they hid in the Hougang area before driving to a safe house in Kuala Terengganu, Malaysia, where they
were apprehended before they could set sail to their final destination, probably in Japan.

## Mastermind Analysis

The Mastermind organization is managed by Minca H and is a secret organization operating under the cover of the company
Nelexat. Nelexat provides tax lawyers in Zurich. This organization carries out various missions, such as the "Bruised
Rogue'' operation which consists of exfiltrating Lucilhe DUMARQUAIS. Mastermind is a complete organization with various
members under Minca's command. First of all, Lian Nussbaumer working for Nelexat is the group's tax lawyer who protects
the group. The Nelexat website at Nelexat.ch is administered by O. Vokolska. Secondly, the person who operates in the
field is Oleg Vokolski, who kidnapped Lucilhe. Finally, Mastermind's operations are investigated by the investigator
Julian Pinkerton.

----
**MASTERMIND :**

* Name : Minca H.
* Pseudo : MastermindAlly3743 / mincah_mm
* Email : mincah_mm@proton.me
* How involved : Head, The associate  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image30.png" width="50" alt=""/>

———

* Name : Lian Nussbaumer
* Pseudo : Nelexlian
* Email : mastermind_mastermind@proton.me
* How involved : Senior tax lawyer and partner at Nelexat. Organised the meeting in Switzerland (google meet link)  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image113.png" width="50" alt=""/>

———

* Name : Oleg Vokolski
* Pseudo : vok_0lski
* Email : vok_0lski@proton.me
* How involved :
* Role : The action man, the person on the ground who recovered Lucilhe.  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image38.png" width="50" alt=""/>

———

* Name : O. Vokolska
* Pseudo : littlesparr0w / OVokolska
* Email : ovokolska@protonmail.com
* How involved : Development of nelexat.ch
* Note : Looking for love, has a profile on which she is waiting to be contacted (
  profile/0zAhMACjE4NzI4NjIzMDkAII1ix1PX0QWiZqTHLnMHsD7jvBDObPuG-Vm_WZaWh-qd). She is 19 years old and has just finished
  her studies. Daughter of Oleg Vokolski.  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image56.png" width="50" alt=""/>

-----

**EXTERNES :**

* Name : Julian Pinkerton
* Pseudo : Pinkerton91 / Julian Pinkerton#9348 / user545947198194
* Email : ovokolska@protonmail.com
* How involved : The Intruder, Mastermind survey  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image14.png" width="50" alt=""/>

———

* Name : Lucilhe DUMARQUAIS
* Pseudo :
* Email :
* How involved : Target of the bruised rogue mission  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image7.png" width="50" alt=""/>

———

* Name : Tsuzune Yokoyama
* Pseudo : tsuyo63
* Email : tsuyo63@proton.me
* How involved : Mission sponsor Bruised Rogue, Mastermind client  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image7.png" width="50" alt=""/>

------
**NELEXAT :**

* Name : Fridrich Merker
* Pseudo : BizneuilleTrader
* Email :
* How involved : Only Nelexat, not Mastermind  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image109.png" width="50" alt=""/>

———

* Name : Lucie Dleau-Berger
* Pseudo : GiantIncomesForYou
* Email :
* How involved : Only Nelexat, not Mastermind  
  <img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image53.png" width="50" alt=""/>

## Associate analysis

The lawyer's partner, the head of mastermind, is a businesswoman by the name of Minca H. According to Pinkerton's
information, she is English with a Slavic look. She is said to have long, wavy, red hair with Venetian blonde
highlights. The developer describes her as having hazel eyes. She is also listed on TripAdvisor as being 1.87m tall.
She was the one who gave the watch to the lawyer (Lian) a few years ago.

In brief:

* Height: 1.87m
* Eyes: Hazel
* Hair : Long, wavy, red with Venetian blond highlights
* Face : Slavic origin
* Nationality : English
* Last known location : Chelsea

## Action Man Analysis

The Action man's name is Oleg Vokolski.  
He is known for the following crimes: theft, car theft, escape.  
He was recruited into Mastermind after a mission he requested from them.  
He is the one who retrieved Lucilhe from France and has to bring her to Tsuzune Yokoyama.  
Oleg Vokolski is a man about 6'2" tall with brown and grey hair. He is Polish and speaks fluent Polish and English. He
has a scar on his right arm and a rose tattoo on his right arm.  
He uses the email address vok_0lski@proton.me.  
The man is under a red europol notice which can be used as a pressure point and also his daughter developed the website
of nelexat.

# Maltego

During this CTF, we completed a Malteo with information that we retrieved.
<img src="https://raw.githubusercontent.com/Tacosint/HEXA_CTF_V2/master/images/image33.png" alt=""/>
