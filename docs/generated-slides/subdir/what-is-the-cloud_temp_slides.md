= What is "the cloud"?
Clément Levallois <levallois@em-lyon.com>
2017-31-07

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

[.stretch]
image::EMLyon_logo_corp.png[width="242" align="center"]


==  'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

==  !

Find the reading list for this session on Pinterest:
https://fr.pinterest.com/seinecle/what-is-the-cloud/

==  1. Note on the terminology: what is a server?

For this topic, you need to know what a "server" is. A server is simply a computer stripped of everything unessential (screen, mouse, graphic card, sound card, keyboard)...

To illustrate: when Google is calculating what the best results are for your search "what are cheap and delicious restaurants in Lyon", this calculation must be done on a computer, right?

The kind of computer used to do this calculation is *not* this one:

==  !

[.stretch]
image::desktop.jpg[align="center",title="A desktop computer"]


==  !
The reason is, we don't need a screen, mouse, desktop, and not even the big box containing the computer itself. They take too much space, consume energy, and there is no need for them.

So when all the unecessary parts are removed, the computer looks like this, and is called a "server":

==  !

[.stretch]
image::server.jpg[align="center",title="A server"]


source: https://www.oracle.com/servers/sparc/s7-2/index.html

==  !
Take a look at the shape: rectangular and very slim. This makes it easy to stack up servers one on the other. Because for Google and other companies crunching data for their business, a lot of servers are needed, so gaining on space is a real issue.

When many servers are piled up together and put in a big tall box, this is called a *rack* of servers, and look like this:

==  !

[.stretch]
image::rack.jpg[align="center",title="A rack of servers"]


==  !

When all the racks of servers are put in the same room, this is called a "data center" and looks like this:

[.stretch]
image::datacenter.jpg[align="center",title="A data center"]


==  !

Look at this video showing a tour of a data center at Google:

video::https://www.youtube.com/watch?v=XZmGGAbHqa0[align="center"]

==  !
Usually, until 2005 roughly, companies had two options:

- buying their own servers and using them on their premises (at their location).
- paying the services of companies specializing in managing data centers.

Then the "cloud" changed this.

==  2. The cloud

The term "cloud" was made popular by Amazon with their service “Amazon Elastic Compute Cloud” (Amazon EC2) launched in 2006.

This service was new in many ways:

==  !

- you can rent servers owned by Amazon, at a distance, when you need them, for a duration that you choose.

- there is an emphasis on ease of use: no need to know the technical details of these servers (how they are plugged, how they are configured…)

==  !

- you are just given a login + password and you can start using these servers for your needs.

- it's "elastic": if you need more servers, or more powerful servers, it's just possible. No need for signing a new contract or to evaluate whether Amazon has the capacity... it's dimensioned to be possible.

==  !

Let's compare a situation with or without the cloud:

[width="100%"]
|=======
|*Without the cloud* |*With the cloud*
|You make a market study for which server to buy

Get the approval by your finance department to buy it (that’s a fixed asset!)

Wait for the server to ship

Install it and configure it

Maintain it (security, etc.)

When the job is over: what do you do with your server? That’s a sunk cost.

If the job happens to need more computing capacity than your server offers: you are stuck with your too-small-server!
|On https://aws.amazon.com/ec2/?nc1=h_ls[Amazon’ EC2 website], you click to choose a server among those on offer: it is *on demand*

You run your job on it. Costs are metered precisely.

When your job is over, you stop the server with a click and pay the bill.

If the job happens to need more computing capacity, you switch to a bigger server with a single click, or it can be done for you automatically: it is *elastic*.
|It is a capex|It is an opex
|=======

The cloud can fit in the budget as an operational expense instead of a capital expenditure.
Opex are not inherently a better or cheaper option than a capex, but they are easier for a project team or business unit to fit in their budget.
See http://gevaperry.typepad.com/main/2009/01/accounting-for-clouds-stop-saying-capex-vs-opex.html[this blog post], especially the critical comments below the post, to continue this discussion.

==  2. IaaS, PaaS, Saas ... ??

What a company can do with the cloud?

They can use it to run elementary operations, up to more complex ones:

==  !

*Infrastructure as a service* (IaaS)

You use servers in the cloud for basic capabilities like storing data, or computing operations.

==  !

*Platform as a Service* (Paas)

The cloud is used to provide building blocks of a service: to manage a messenging system, to host apps, ...

==  !

*Software as a Service* (Saas)

The cloud is used to host a full software accessible "on demand" through the browser: like Google Drive, https://www.d2l.com/products/learning-environment/[Brightspace] or https://www.salesforce.com/fr/?ir=1[SalesForce].

==  2. Private or public cloud? Hybrid cloud?

- Amazon EC2 is an example of a *public cloud*: it is publicly accessible to any customer. Of course, this does not mean that every customer can see what the others are doing on the cloud! Each customer have their private spaces on the cloud.

==  !

- Many companies have security requirements which prevent them from accessing public clouds.
They need to have their servers on premises.
In this case, they can build their own *private cloud*: it is a cloud just like Amazon EC2, except that it is owned, managed and used by the company exclusively - it is not accessible to third parties.
But even private, it keeps the basic characteristics of a cloud: on-demand and elastic in particular.

==  !
- *Hybrid clouds* are a variety of private clouds: it is a private cloud where some forms of operations can be delegated to a public cloud.
For example, operations which are not security sensitive and which need a capacity of computing in excess of what the private cloud of the company can provide.

==  !

==  The end
==  !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: http://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
pass:[    <!-- Start of StatCounter Code for Default Guide -->
    <script type="text/javascript">
        var sc_project = 11411204;
        var sc_invisible = 1;
        var sc_security = "11411204";
        var scJsHost = (("https:" == document.location.protocol) ?
            "https://secure." : "http://www.");
        document.write("<sc" + "ript type='text/javascript' src='" +
            scJsHost +
            "statcounter.com/counter/counter.js'></" + "script>");
    </script>
    <noscript><div class="statcounter"><a title="site stats"
    href="http://statcounter.com/" target="_blank"><img
    class="statcounter"
    src="//c.statcounter.com/11411204/0/11411204/1/" alt="site
    stats"></a></div></noscript>
    <!-- End of StatCounter Code for Default Guide -->]