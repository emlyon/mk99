= What an API?
Clément Levallois <levallois@em-lyon.com>
2017-31-07

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

image::EMLyon_logo_corp.png[width="242" align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


== 1. Definition of API
//ST: 1. Definition of API
//ST: !

API: acronym for "Application Programming Interface"

An API is the way to make software programs “easy to plug and share” with other programs.

Ok so... APIs are a cable? A computer? A USB connection? No.

//ST: !

An API is simply a group of rules (you can also call it a convention, or an agreement...) which programmers follow when writing the part of their code which is in charge of communicating with other software.

These rules are then published (on a webpage for example), so that anyone who needs to connect to the program can learn what rules to follow.
That's it.

//ST: !
So, an API is simply a way to write code to make it easy to interface with other programs?
Yes.

Why the fuss then?

//ST: !
Having conventions on how to write a software so that somebody can plug it to its own software is one thing.
APIs of this sort are a https://dzone.com/articles/how-design-good-regular-api[classic topic in computer science] but we are not concerned with this here.

//ST: !
APIs we are going to discuss are about communication between distant computers, in a business context.

Let's do a bit of history:

== 2. The origin of APIs
//ST: 2. The origin of APIs
//ST: !



//ST: !
Companies which need to exchange data is nothing new.
Manufacturers, retailers, banks, ... they need to exchange information at regular interval.

Sending invoices, receiving receipts for merchandise, and many other administrative records generated in the course of business.

//ST: !
These receipts, invoices... can be printed and mailed (this solution still exists of course).

With informatics developing in the 1970s and 1980s, a new system emerged: the exchange of information via computers: https://en.wikipedia.org/wiki/Electronic_data_interchange[Electronic Data Interchange] (EDI)

//ST: !
EDI is not an exchange of file attachments in emails or via a file transfer on a website, because emails and websites did not exist yet! (emails and the Web were adopted by firms in the late 1990s).

//ST: !
Instead, exchanging data via EDI consisted in using complex electronic tools (like the fax but even more complicated) because:

//ST: !
- each industry has its own protocol to exchange data (one protocol for logistics, one for payments, one for this or that retailer chain, etc.)
- you need a dedicated device or software for each EDI protocol, and these are not given for free

//ST: !
- EDI protocols can vary from one country to another
- EDI protocols are controlled by industry associations which do not adopt innovation quickly

//ST: !
So EDI is fragmented, complicated to implement, slow to evolve and not cheap.

It still exists, especially in large B2B industries like transportation (http://cerasis.com/2014/12/11/edi-in-transportation/[check here]), but it lost in popularity in the wider economy because...  APIs have arrived.


//ST: !
In the late 1990s and early 2000s, Internet and the World Wide Web expanded a lot.
More and more servers in different parts of the world needed to be interfaced with each other to exchange data.


//ST: !
It became increasingly convenient to define simple and universal conventions that everyone could learn and follow to standardize these exchanges, for free and easily.
That's what web APIs (API for short) do.

//ST: !
Unlike EDI, APIs drop any industry-specific concern. APIs are just a convention to send and receive data, without any saying on the content of the data.
The data sent and received can be invoices, webpages, train schedules...

//ST: !
Another difference between APIs and EDIs is that APIs use the Web to transfer data, using the same route as the webpages you load in your browsers. This is why APIs are called "web services", or "web APIs".

Two popular API conventions emerged and competed for popularity:

//ST: !
- SOAP (https://en.wikipedia.org/wiki/SOAP[Simple Object Access Protocol])
- REST (https://en.wikipedia.org/wiki/Representational_state_transfer[Representational State Transfer])

//ST: !
REST became ultimately the most widely adopted, because it uses the same simple principles that webpages use to be transferred over the Internet (the "http" protocol that you see in web page addresses).
This is why APIs are often called "REST APIs"

//ST: !
In 2000-2010, it became increasingly easy and natural to adopt the REST convention to make one's software and data available to another computer.
This simple evolution to ease interoperability had *immense effects*:

== 3. Business consequences of APIs
//ST: 3. Business consequences of APIs
//ST: !

==== 1. APIs *opened* software to the world.

//ST:!

An API transforms a closed software into something that can be plugged to anything other computer or object, as long as it is connected to the Internet.

//ST:!
Fo instance, APIs were a key factor of success for https://en.wikipedia.org/wiki/Salesforce.com[SalesForce] in the early 2000s. SalesForce, created in 1999, has a revenue of US$8.39 billion in 2017:

//ST:!
a) SalesForce developed a CRM as a SaaS where features of the CRM were *exposed as APIs* (meaning, these features could be plugged to external apps via the REST protocol).

//ST:!
b) SalesForce created a PaaS to host apps that could plug to the SalesForce CRM via the APIs developed by SalesForce.

This platform is called https://www.salesforce.com/products/platform/products/force/[Force.com] and external developers can put their apps there, as long as they are compatible with the SalesForce API.

//ST:!
SalesForce takes a commission on the sales made by these third party apps hosted on Force.com, but more importantly, the platform creates an *ecosystem* of apps and developers around the SalesForce products which makes it hard for a custmer company to switch to a different product.

//ST:!
==== 2. APIs *accelerated* software innovation

//ST:!

Thanks to API it became easy to add software blocks together and create new apps, even if the app developers where from different countries, industries, or big and small. https://medium.freecodecamp.org/how-i-replicated-an-86-million-project-in-57-lines-of-code-277031330ee9[Check this amazing story].

//ST:!
==== 3. APIs *opened* data

//ST:!
Companies and public organization own many datasets of great business interest.
The use of these datasets can be free (for small projects and NGOs) or monetized if the user is an entreprise.

Without APIs, datasets can be made publicly available as docs (eg, Excel spreadsheets) to download but this is not practical (try downloading something like `all_train_schedules_2000_to_2017.xls` ! 😓).

//ST:!
So, imagine a transportation company like French SNCF which finds it interesting to publish station names, train schedules, etc. because it could be used by other companies to build new services : how can it do it?

The data is on a server of SNCF. Then SNCF adds https://data.sncf.com/api/en[an API and its documentation], making the data available to anyone who knows about REST APIs (and https://youtu.be/7YcW25PHnAA[this is trivial]).

//ST:!
Entrepreneurs and programmers in general will be able to access the data via the API and use it, possibly to create new services based on this train information.

//ST:!
==== 1. A wealth of APIs

//ST:!
To discover new APIs, or to make your APIs easier to discover, the most well known place is the website "Programmable Web": https://www.programmableweb.com/

Searching on this website, you will find APIs ranging from the most https://www.programmableweb.com/api/coca-cola-enterprises[business-y] use case, to APIs of a https://www.programmableweb.com/api/itsthisforthat[more fun and odd sort].


//ST:!
Still, many APIs are not listed on this website, and a google search for "info I need + API" is also a good way to find if the API you'd need exists. Interested in whale sightings? http://hotline.whalemuseum.org/api[There is an API for that].


//ST:!
==== 2. APIs: a business world of its own

//ST:!
APIs have become central to the economy. As a result, a large number of services associated to APIs have developed to cater for all the needs of companies that use them.

How to create an API, how to manage the documentation of a large number of APIs, how to connect a wide variety of APIs, how to manage the security of APIs, how to monetize and API...

//ST:!
-> Many large firms and startups now specialize in all these different issues.
Here is the 2017 landscape of the main companies active in the API industry:

//ST:!
image::api-landscape-2017.jpg[align="center", title="The API landscape in 2017"]
{nbsp} +

//ST: !
[FINAL NOTE]
====
As business students, you have roles to play in the API economy. Engineers develop the technical part of the APIs (the code itself), but you have the expertise to develop the business aspects of this kind of product. In your job search, don't hesitate to query job postings with "API" in it, you will probably find positions where you'd apply successfully!
====

== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
pass:[    <!-- Start of StatCounter Code for Default Guide -->
    <script type="text/javascript">
        var sc_project = 11411204;
        var sc_invisible = 1;
        var sc_security = "7b86ca26";
        var scJsHost = (("https:" == document.location.protocol) ?
            "https://secure." : "http://www.");
        document.write("<sc" + "ript type='text/javascript' src='" +
            scJsHost +
            "statcounter.com/counter/counter.js'></" + "script>");
    </script>
    <noscript><div class="statcounter"><a title="site stats"
    href="http://statcounter.com/" target="_blank"><img
    class="statcounter"
    src="//c.statcounter.com/11411204/0/7b86ca26/1/" alt="site
    stats"></a></div></noscript>
    <!-- End of StatCounter Code for Default Guide -->]
