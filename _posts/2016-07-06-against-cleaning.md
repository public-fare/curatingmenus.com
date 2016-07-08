---
layout: article
title: Against Cleaning
authors:
  - KR
  - TM
lede: 'Practitioners, critics, and popularizers of new methods of data-driven research treat the concept of “data cleaning” as integral to such work without remarking on the oddly domestic image it makes—as though a corn straw broom were to be incorporated, Rube-Goldberg-like, into the design of the Large Hadron Collider. In reality, “data cleaning” is often the most opaque part of data-intensive research.'
thumbnail: ''
key_image: ''
pubdate: 2016-07-06
featured: true
---
Practitioners, critics, and popularizers of new methods of data-driven
research treat the concept of “data cleaning” as integral to such work
without remarking on the oddly domestic image the term makes—as though a
corn straw broom were to be incorporated, Rube-Goldberg-like, into the
design of the Large Hadron Collider. In reality, “data cleaning” is a
consequential step in the research process that we often make opaque by
the way we talk about it. The phrase “data cleaning” is a stand in for
longer and more precise descriptions of what people are doing in the
initial phases of data-intensive research. If you work with data or pay
attention to discussions among practitioners who do, you’ve probably
heard or read somewhere that 80 percent of that work is “cleaning”.<sup id="fnref:1"><a href="#fn:1" rel="footnote">1</a></sup> Subsequently you likely realize that, there is not one single
understanding of what “data cleaning” means. Many times the specifics of
“data cleaning” are not described anywhere but reside in the general
professional practices, materials, personal histories, and tools of the
researchers. That we employ obscuring language like “data cleaning”
should be a strong invitation to scrutinize, perhaps reimagine, and
almost certainly rename this part of our practice.

The persistence of an element that is “out of focus” in discussions of
data-intensive research does not invalidate the findings of such
research, nor is it meant to cast researchers using these methods under
suspicion. Rather, the collective acceptance of a connotative term,
“cleaning,” suggests two assumptions: first, that researchers in many
domains consider the consequences of whatever is done during this
little-discussed 80 percent of the process devoted to “cleaning” as
sufficiently limited or bounded so as not to threaten the ultimate value
of any findings; and second, relatedly, that there is little to be
gained from more precise description of those elements of the research
process that currently fall under the rubric of “cleaning.”

As researchers working in the relatively new domain of data-intensive
research in the humanities, we have found that these assumptions do not
serve us well. In fields where data intensive work has a longer history,
researchers have developed paradigms and practices that *de facto* define
“data cleaning.” However, in the humanities, these bounds are still
unformed. Yet the humanities cannot import paradigms and practices whole
from other fields, whether from “technoscience” or the nearer “social”
sciences, without risking the foreclosure of specific and valuable
humanistic modes of producing knowledge. If we are interested in working
with data and we accept that there is something in our work with data
that is like what other fields might call “data cleaning,” we have no
choice but to try to articulate both what it is and what it means in
terms of how humanists make knowledge.

This may be a only a current issue, a tax on those humanities
researchers who wish to adopt new methods, asking them to over-explain
their work processes in order to hash out new regimes for research in
this domain. Once new methods are more widely practiced, the
data-intensive humanities researcher may also be able to toss off the
shorthand of “data cleaning.” For now, there is value in being arrested
by the obfuscation of this phrase. Trying to more precisely say what we
mean by “data cleaning” can be fruitful because this effort directs our
attention to an unresolved conversation about data and reductiveness. In
turn, this might help us to develop new work that blends the tradition
of cultural criticism from the humanities with research that is also
digital and data-intensive.

#### Humanities Data and Suspicions of Reduction
{: #humanities-data}
When humanities scholars recoil at data-driven research, they are often
responding to the reductiveness inherent in this form of scholarship.
This reductiveness can feel intellectually impoverishing to scholars who
have spent their careers working through particular kinds of historical
and cultural complexity. The modern humanities have invested mental and
moral energy into, and reaped insights from, studying difference.
Bethany Nowviskie summarizes this tradition in her contribution to the
(forthcoming) 2017 edition of *Debates in the Digital Humanities*,
[“Capacity Through
Care.”](http://nowviskie.org/2016/capacity-through-care/) Nowviskie
writes:
<blockquote>
The finest contribution of the past several decades of humanities research has been to broaden, contextualize, and challenge canonical collections and privileged views. Scholars do this by elevating instances of neglected or alternate lived experience—singular human conditions, often revealed to reflect the mainstream.
</blockquote>
From within this worldview, data cleaning is then maligned because it is understood
as a step that inscribes a normative order by wiping away what is
different. The term “cleaning” implies that a data set is “messy.”
“Messy” suggests an underlying order. It supposes things already have a
rightful place, but they’re not in it—like socks on the bedroom floor
rather than in the wardrobe or the laundry hamper.

Understood this way, suspicions about “cleaning” are suspicions that
researchers are not recognizing or reckoning with the framing orders to
which they are subscribing as they make and manipulate their data. In
fields where researchers have long been explicit about their framing
orders, the limits of results are often understood and articulated using
specialized discourses. For example, in climate science, researchers
confine their claims to the data they can work with and report results
with margins of error.<sup id="fnref:2"><a href="#fn:2" rel="footnote">2</a></sup> While humanities researchers do have
discourses for limiting claims (acknowledging to the choice of an
archive or a particular intellectual tradition), the move into data
intensive research asks humanists to modify such discourses or develop
new ones suitable for these projects. The ways in which humanities
engage these challenges may both open up new practices for other fields
and allow humanities researchers who have made powerful critiques of the
existing systems of data analysis to undertake data-intensive forms of
research in ways that don’t require them to abandon their commitments to
such critiques.

To contribute to the development of new discourses and the practice of
critically-attuned data work, we scrutinize “cleaning” through a
reflection on our own work with *Curating Menus*. *Curating Menus* is a
research project that aims to curate and analyze the open data from New
York Public Library’s [*What’s on the Menu?*](http://menus.nypl.org/).

#### The Value of a Naive Tool
{: #naive-tools}
We set off to answer questions like: can we see the effect of wartime
food rationing in what appeared on menus during World War I? or, can we
track the changing boundaries of what constituted a “dish” over time? To
do this, we thought we needed to “clean” the “messy” data. What became
evident was that “cleaning up” or “correcting” values was a
misleading—and even unproductive—way to think about how to make the data
more useful for our own questions and for other scholars studying food.

Under the rubric of “cleaning,” we began with a technical solution to
what we’d imagined was a technical problem. Variation in the strings of
text transcribed from menus was obscuring our ability to do things as
simple as count how many dishes were in the data set. Trevor, along with
Lydia Zvygintseva, began trying to reduce the number of variations using
[Open Refine](http://openrefine.org/). When the scale of the problem
overwhelmed the capabilities of that tool, Trevor discovered that it was
possible to run the clustering algorithms popularized by Open Refine
using [custom Python
scripts](http://nbviewer.jupyter.org/gist/trevormunoz/8358810). The
output of one of these scripts were lists of variant values such as:

<pre>
id
2759        Potatoes, au gratin
7176         Potatoes au Gratin
8373        Potatoes--Au gratin
35728       Potatoes: au gratin
44271        Au Gratin Potatoes
84510      Au Gratin (Potatoes)
94968     Potatoes, au Gratin,
97166      POTATOES:- Au gratin
185040     Au Gratin [potatoes]
313168      Au Gratin  Potatoes
315697     (Potatoes) Au Gratin
325940       Au Gratin Potatoes
330420       au-Gratin Potatoes
353435     Potatoes:  Au gratin
373639       Potatoes Au Gratin
</pre>

We were very excited to get lists that looked this way because we could
easily imagine looping over such lists and establishing one normalized
value for each set of variants. We hadn’t yet recognized that the data
model around which the data set was organized was not the data model we
needed to answer our research questions. The main challenge seemed to be
processing enough values quickly enough to “get on with it.”

At this point, the Python scripts we were using were small,
purpose-built command line programs. After some deliberation, we decided
to build a simple web application to provide the task-specific user
interfaces we needed to tackle the challenge of NYPL’s menu data.<sup id="fnref:3"><a href="#fn:3" rel="footnote">3</a></sup>

<figure class="figure-center">
<img data-gifffer="{{ site.s3 }}against-cleaning/ssmmfm-v2.gif" data-gifffer-alt="A naive data cleaning tool">
<!-- <figcaption>Scalability in the original physical menus.</figcaption> -->
</figure>

The piece of software we built does, in some ways, the opposite of what
one might expect. A cluster of values like the one for “Potatoes Au
Gratin” above is presented to the user, and he or she (Trevor or Katie)
have to make a decision about how to turn that cluster of variants into
a single value. Our tool sorts the variants by the number of times they
appear across the data set. So the decision may be to simply save the
most commonly occurring value as the normalized form: “potatoes au
gratin”. Or it might be to modify that value based on a set of rules we
have created (more on that later). Or it might be to supply a new value.
The process can end up looking like this:

<em>… What would be the authoritative spelling of Buzzards Bay oysters? Let me Google that.</em>

<em>… Oh, it collapsed an orange juice and an orange sherbet under “orange”; let me flag that.</em>

<em>… A jelly omelet!?</em>

The tool surfaces near-matches, but it does not automate the work of
collapsing them into normalized values. Instead, it focuses one’s
attention and labor on exactly that activity. In our initial version of
computer-assisted data curation, you still have to touch each data
point.

In the process of normalizing values, we found ourselves faced with
questions about the foods themselves. Choosing the “correct” string was
not a self-contained problem, but an issue that required returning to
our research questions and investigating the foods themselves. Since the
research questions we were asking required us to maintain information
about brands and places, we often had to look up items to see which was
the correct spelling of the brand or place name.<sup id="fnref:4"><a href="#fn:4" rel="footnote">4</a></sup> Shellfish and
liquor were two particularly interesting and plagued areas for these
questions. The process revealed kinds of “messiness” that we had not yet
even considered. We realized the data points we were making were not
“corrections” “cleaning up” the original data set, but their rather
formed an additional contribution of information with its own data
model. What we were developing was not an updated version of the NYPL’s
data set. What we thought were data points were, in fact, a synthesis or
mash-up of different kinds of information within a half-finished or
half-articulated data model. We needed to create our own data set, which
would work in context with the NYPL data set.

This approach is made possible by and explicitly rests on a structure of
linked data. The NYPL data was created to be linkable—it uses unique
URLs for dishes and menus. Our data can include links referencing these
URLs. The linked data paradigm thus encourages us to build our own data
and to (inter-)link it with the original.

#### Diversity in Data
{: #diversity-in-data}
The Curating Menus data set is an organized hierarchy of concepts from
the domain of food. To make it, we attach labels that we believe will
best facilitate researchers’ understanding of the scope, diversity, and
value of the NYPL’s data set for research. Our interaction with the NYPL
data set became a process of evaluating variants. Which variants in the
names of dishes revealed new information we should account for in our
own data, and which variants were simply accidents of transcription or
typesetting? The process freed us to attend to difference and detail
rather than only attempting to hide it or clean it away. We can be
sensitive to questions about time, place, and subject. This kind of
attention is imperative if humanities researchers are to find the menus
data legible.

As we considered methods for preserving diversity within our large data
set, the work of anthropologist Anna Tsing offered a valuable
theoretical framework to approach these issues. In “On Nonscalability:
The Living World is Not Amenable to Precision-Nested Scales,” Tsing
critiques scalability as an overarching paradigm for organizing systems
(whether world trade, scientific research, or colonial economies).<sup id="fnref:5"><a href="#fn:5" rel="footnote">5</a></sup> By
scalability, Tsing means the quality that allows things to be traded out
for each other in a totalizing system without regard to the unique or
individual qualities of those things—like many stalks of sugarcane
(which are biological clones of one another), or, subsequently, workers
in a factory. From this definition of scalability, she goes on to argue
for a theory of nonscalability. Tsing writes, “The definition of
nonscalability is in the negative: scalability is a distinctive design
feature; nonscalability refers to everything that is without that
feature … Nonscalability theory is an analytic apparatus that helps us
notice nonscalable phenomena.” While scalable design creates only one
relationship between elements of a system (what Tsing calls “precision
nesting”), nonscalable phenomena are enmeshed in multiple relationships,
outside or in tension with the nesting frame. “Scales jostle and contest
each other. Because relationships are encounters across difference, they
have a quality of indeterminacy. Relationships are transformative, and
one is not sure of the outcome. Thus diversity-in-the-making is always
part of the mix.”

Currently, the imagination of the cultural heritage world has been
captured by crowdsourced information production on the one hand and
large-scale institutional aggregation on the other—the *What’s On the
Menu?* project exemplifies both of these trends. Our difficulties
working with the open data from this project suggest that it is a vital
moment to consider the virtues of non-scalability theory in relation to
digital scholarship. Engineering crowdsourced cultural heritage projects
usually involves making object transcription, identification, and the
development of metadata scalable. For example, the makers of the *What’s
On the Menu?* project designed their system to divide the work into
parcels that could be done quickly by users while reducing friction that
arise from differences in the menus (the organization of the information
on the page, other evidence of physical manifestations like handwriting
and typeface variations).<sup id="fnref:6"><a href="#fn:6" rel="footnote">6</a></sup> The images of menus and the metadata about
them are also being republished through projects like the [Digital
Public Library of America](https://dp.la/) (DPLA), another example of
how things get shaped and parsed for purposes of scaling up to ever
wider distribution. Tsing reminds us, “At best, scalable projects are
articulations between scalable and nonscalable elements, in which
nonscalable effects can be hidden.” She argues that the question is not
whether we do or do not engage in scalable or non-scalable processes. To
explore the articulations between scalable and nonscalable, Tsing tells
the story of the contemporary matsutake industry, which encompasses both
foraging (by immigrant harvesters in the ruins of large-scale industrial
forestry in the U.S. Pacific Northwest) and global supply chains serving
Japanese markets. Tsing’s account focuses our attention on how “scales…
arise from the relationships that inform particular projects, scenes, or
events” (509). The elements of nonscalable systems enter into
“transformative relationships” and these “contact\[s\] across difference
can produce new agendas” (510). Following Tsing, we came to see points
of articulation which had previously been invisible to us as would-be
consumers of scaled data. Beginning from the creation of the original,
physical menus and tracing the development of the crowd-created data, we
identify and account for “nonscalable elements”—and consequently, edge
further and further from the terminology of “cleaning.”

#### Seeing Nonscalability in NYPL’s Crowdsourced Menus Project
{: #nonscalability-nypl}
Making menus is a scalable process. Although menus are sometimes
handwritten or elaborately printed on ribbon-sewn silk, the format of a
menu is designed to be scalable. Menus are an efficient typographical
vehicle for communicating a set of offerings for often low-margin dining
enterprises. Part of the way that we know that menus are scaleable is
how alike they appear. “Eggs Benedict” or “caviar”, with their
accompanying prices may fit interchangeably into the “slots” of the
menu’s layout. Within the menus themselves, we also see evidence of the
nexus of printing scalability, dish scalability, and cost in, for
example, the use of ellipses to express different options: eggs with …
cheese, … ham, … tomatoes, etc. The visual evidence of *What’s on the
Menu?* shows us how headings, cover images, epigraphs—for all their
surface variations—follow recognizable patterns. These strong genre
conventions and the mass production of the menus as physical objects
allow us to see and treat them as scaled and scalable.<sup id="fnref:7"><a href="#fn:7" rel="footnote">7</a></sup>

<figure class="figure-center">
<img src="{{ site.s3 }}against-cleaning/menus-ellipses.png" alt="Use of ellipses on a menu">
<figcaption>Scalability in the original physical menus.</figcaption>
</figure>

However, the menus also express nonscalable elements—historical
contingencies and encounters across difference. Some of these
nonscalable elements are revealed by the kind of questions we find
ourselves asking about the experience of ordering from these menus. How
were they understood as part of interactions between purveyors,
customers, and diners? How did diners navigate elements like the
pervasive use of French in the late nineteenth and early twentieth
centuries? How did they interpret the particular style and content of
cover images or quotations? Evidence for these questions manifests in
the menus as objects but does not fit within the scalable frames of menu
production nor the menu data we have at hand. The nonscalable elements
cannot be disregarded and have the potential to impact how we interpret
and handle the scalable data. Nonscalability theory encourages us to
grapple with this dynamic at each point of articulation in the process
of making scalable objects.

The collection of these menus was also scalable. The system set up for
their accession and processing not only treated the menus as
interchangeable objects; it also treated them like the many other paper
materials that entered the collections of the New York Public Library in
the twentieth century. Perhaps the clearest evidence of this is in the
cataloging. The catalog cards fit each menu into the same frame—with
fields for the dining establishment, the date of creation and date of
accession, and the sponsor of the meal if available. Cataloging is a way
of suppressing or ignoring the great differences in the menus, choosing
one type of data to attend to. The cards index the collection so that
the institution has a record of its holdings and so that a user can find
a particular object. The menus, with their scalable and nonscalable
features, become scalable library inventory through this process.<sup id="fnref:8"><a href="#fn:8" rel="footnote">8</a></sup>

Cataloging’s aim is to find a way to make items at least interchangeable
enough not to break the system. The practice is rife with examples of
catalogers navigating encounters with difference. Catalogers practice
nonscalability theory constantly. Sometimes the answer is
institutionally-specific fields in [MARC
records](https://en.wikipedia.org/wiki/MARC_standards); sometimes the
solution is overhauling subject headings or creating a new way of making
records (like the [BIBFRAME
initiative](https://www.loc.gov/bibframe/)). However, the answer is
almost never to treat each object as a unique form; instead the object
is to find a way to keep the important and usable information while
continuing to use socially and technologically embedded forms of
classifying and finding materials.

Digitization is also a process designed for scalability. As long as an
object can fit into the focal area of an imaging device, its size,
texture, and other material features are reduced to a digital image
file. The zooming enabled by high-resolution digital images is one of
Tsing’s prime examples of design and engineering for scalability. In the
distribution of digitized images, the properties of the digital
surrogate which are suited to scalability are perpetuated, while the
properties of the original which are nonscalable (the feel of the paper,
its heft or daintiness) are lost.<sup id="fnref:9"><a href="#fn:9" rel="footnote">9</a></sup>

The point at which certain objects are selected for digitization is one
of the moments of articulation Tsing describes between the scalable and
nonscalable. Digitization transforms of diverse physical
materials—brittle, acidic paper or animal parchment, large wooden covers
or handstitched bindings, leaves or inserts—into standardized grids of
pixels. From the point of digitization forward, the logic of scalability
permeates projects like *What’s On the Menu?*. The transcription
platform is constructed to nest precisely within the framework of how
cultural heritage organizations like NYPL create digital objects from
their original materials.

Paul Beaudoin from the NYPL Labs team discusses some of the logic behind
their approach to these kind of projects in a [blog
post](http://www.nypl.org/blog/2015/11/23/scribe-framework-community-transcription)
announcing Scribe, an open-source software platform released in 2015 but
derived from the library’s experience with crowdsourced transcription
projects. Beaudoin describes how the [Scribe
platform](http://scribeproject.github.io/) is based on “simplification
\[that\] allows us to reduce complex document transcription to a series
of smaller decisions that can be tackled individually. ... the atomicity
of tasks makes projects less daunting for volunteers to begin and easier
to continue.” *What’s on the Menu?*, for example, presents visitors with
a segment of a digitized image of a menu and a single text input box to
record what they see.<sup id="fnref:10"><a href="#fn:10" rel="footnote">10</a></sup> The NYPL Labs team is explicit about its
commitments to designing for scalability. We know from work in the
domain of scholarly editing that what comprises “transcription” is not
self-evident.<sup id="fnref:11"><a href="#fn:11" rel="footnote">11</a></sup> It could be modeled and implemented in software in a
number of ways. The menus project uses Optical Character Recognition
(OCR) software to generate bounding boxes that determine what human
volunteers will transcribe. In this, we can see the “precision nesting”
of scales at work. OCR software is designed to scalably produce
machine-readable, machine-processable digital text from images of
printed material. In the case of the menus, the software can detect
regions of text within the digital images; however, due to the variation
in typefaces, the ageing of inks and paper, and other nonscalable
elements, the output of the OCR algorithm is not a legible set of words.
Using the bounding boxes but discarding the OCR text in favor of text
supplied by human volunteers is a clever and elegant design. It
constructs the act of transcription in such a way that it matches the
scalable process of digitization and ways of understanding the content
of a menu that privilege scalable data.

Yet, even here, now that we know to look for them, the nonscalable
effects cannot be completely hidden. The controls allow users to zoom
through three levels of an image, a feature that evidences slippage in
the segmentation algorithm. This element of the tool acknowledges that
someone might need to zoom out to complete a transcription—often because
the name of a dish has to be understood through the relation between the
line of text in the bounding box and other nearby text, like a heading.
Further, the text box on the transcription screen is unadorned, implying
that what to do is self-evident, but the help page is full of lengthy
instructions for how to “navigate some of the more commonly encountered
issues,” revealing the ways that transcription is not a self-evident,
scalable process.

<figure class="figure-center">
<img src="{{ site.s3 }}against-cleaning/menu-editor-zoom.png" alt="The zoom tool at menus.nypl.org">
<figcaption>The physical layout of text often requires zooming out the image presented for transcription to decipher a dish.</figcaption>
</figure>

In addition, the project was designed so that people did not have to
create accounts or sign in to submit transcriptions. This reflects a
view of volunteers as interchangeable, and embedded in this assumption
is the hope that it allows more work to get done more quickly. However,
what is is construed as a scalable workforce is, in fact, made up of
people who have different levels of understanding or adherence to the
guidelines and different perceptions or interpretations of the
materials. When we understand this workforce as a collection of
individuals, we can see how any crowd as large as the one that has
worked on the menus project will contain such diversity. The analytic
apparatus of Tsing’s nonscalability theory makes all these design
choices visible and allows us to see the transcription task, as framed
within *What’s on the Menu?*, as another moment of articulation between
scalable and nonscalable elements.

When we download the open data from the *What’s on the Menu?* site and
open up the files, we are presented with the results of all this
activity—menu collection and digitization and transcription. Instead of
seeing mess, we see the ways in which diversity has seeped or broken
into what were designed to be smoothly scaling systems. Now we are
better prepared to envision how our work—creating new data organized
around concepts of historical food practices—begins from what the NYPL
has released, which is transcription data (words volunteers typed into
the boxes at *What’s on the Menu?* linked to metadata from their digital
library systems). In both of these data sets there is something called
“dish.” In NYPL’s data, “dish” is the name of the field in which a
transcribed string from a menu is stored in the project’s database. In
Curating Menus’s data, “dish” is a representation created to reflect and
name an arrangement of foods and culinary practices in a particular
historical moment. This is an example of, as Tsing puts it, the ways
that “scales jostle and contest.” We know that the response to this
friction is not to retreat from working at scale. Instead we have to
find ways of working while aware that *precision* nesting hides
diversity and that there are stakes to things being hidden.

#### Indexes: Making Scalability Explicit and Preserving Diversity
{: #indexes}
Our answer this challenge is an index. We’re suggesting that indexing is
a more precise replacement for some of the work that travels under the
name of "cleaning." An index is an information structure designed to
serve as a system of pointers between two bodies of information, one of
which is organized to provide access to concepts in the other. The lists
of terms and associated page numbers from the back of a book is one
familiar example. An array of other terms that people use alongside
“cleaning” (wrangling, munging, normalizing, casting) name other
important parts of working with data, but indexing best captures the
crucial interplay of scalability and diversity that we are trying to
trace in this piece.

<figure class="figure-center">
<img src="{{ site.s3 }}against-cleaning/cookbook-index.JPG" alt="A cookbook index">
<figcaption>A cookbook index</figcaption>
</figure>

We began to think of the work we were doing as building something like a
back-of-the-book index for the *What’s On the Menu?* data. We would
create additional data structures around and atop the existing data,
generating links between a set of names or categories we created and the
larger and more heterogeneous set of data from NYPL. We are interested
in ultimately building two interconnected indexes, one focused on
historical food concepts and one on the organizations connected to the
menus (businesses, community organizations, fraternal societies, etc.).
We have begun with the food index, and we are developing a framework
that echoes cookbook indexes in order to structure our data:
ingredients, cooking methods, courses, cuisines.

If we felt no unease continuing the lineage of precision nesting that
link the scales of digitization and crowd-sourced transcription, we
could proceed with a completely algorithmic approach—“cleaning” our data
using scripts, linguistic rules, and even machine learning. These
methods yield results by providing an approximation—which we suspected
might hide diversity. We could imagine trusting that an approximation
could be good enough or using algorithmic approaches. However, to
understand what was being approximated—and what was being smoothed
together—we needed to create a grounded approach to making a data model
for our index.

Now when we look at those lists of variations on “Potatoes au Gratin” or
some other group of transcriptions, we are focused on the task of
choosing a label that will be a node in our data set and will serve as a
pointer to all of the varying transcribed values in the NYPL data set.
We are building the set of labels from the set of data rather than
beginning by writing some large, hierarchical domain model. We want to
represent the concept of two eggs and bacon not caring if it was written
“bacon and two eggs” or “2 Eggs and Bacon.”

To get from transcription to concept, we began with a set of simple
rules: spell out numbers, use lower case letters. Actually engaging with
the menu transcriptions quickly raised other questions. For example, on
the question of place names, we decided to apply capitalization rules
(in accord with style guides like the [*Chicago Manual of
Style*](http://www.chicagomanualofstyle.org/16/ch08/ch08_sec060.html))
that say that you capitalize when the reference to place is literal, but
not when the reference makes a generic association: yes to Virginia ham
or Blue Point oysters but no to swiss cheese or scotch. We also found
many single transcriptions containing multiple concepts, like “steak,
sauce béarnaise.” Since we want a way to be able to systematically find
multiple components of a dish, we’re opting to standardize how we
labeled the addition of sauces, garnishes, and other added ingredients.
Here is one instance where we plan to use algorithmic tools to help us
analyze some of this big data after we have grounded it in a specific
data model.

In building an index, we are engaged in creating scalability. We know
that scalability is a process of articulations between different scales;
however, Tsing suggests—and we believe—that those articulations are
often hidden. Conversely, indexes are tools of scalability that make
these articulations explicit.

Our index is about ingredients, meal structures, and cooking techniques.
Someone else could re-index the menus material in a different way.
Variations might involve attending to the species of the plants and
animals that are in foods or taking a nutritional approach that
classifies food based on calories, vitamins, carbohydrates. We can also
imagine projects that attend to language use in ways that our index
suppresses. As libraries and researchers move forward in making and
curating data, instead of the constant refrain of “cleaning,” we want to
encourage indexing, which allows us to build up explicit and flexible
bases of knowledge that people can continue to access and understand.

#### Sharing Control of Authority
{: #sharing-authority}
One of the mechanisms that librarians and archivists have used to build
and maintain large, distributed information systems is a set of
practices referred to as authority control. In brief, these practices
involve creating defined and agreed upon taxonomies as well as
guidelines for the application of such arrangements of terms. The
[Library of Congress Subject
Headings](http://id.loc.gov/authorities/subjects.html) represent one
instance of authority control. Maintaining such a system is labor
intensive and has been used only for supporting core library activities
like managing collections and supporting patrons in finding materials.
Libraries and archives are trying to take advantage of technological
developments in linked data—merging their centuries-old authority
control practices with the affordances of the World Wide Web. However,
what relatively few have seized on are new opportunities to apply the
practices of authority control outside the original core needs of
collection organization and wayfinding.

These new opportunities fall somewhere between digital library practices
and digital humanities research, but the gap is one that more projects
should embrace the opportunity to fill. There is a need for projects
that take “authority work” as an invitation to new creativity; an
invitation for making and building. In such a model, multiple regimes of
authorities might be built up from critically-aware and engaged
intellectual communities to meet their own specific needs while also
participating in larger technological and information systems.

We imagine those communities will contain librarians and scholars.
Though librarians and humanities scholars have frequently intersected,
they have rarely interacted in the ways we are calling for. Simplifying
to the point of caricature, these existing interactions go something
like this: humanities scholars point out that the structure and content
of a specific archive or collection represents even recreates certain
cultural logics. For example, the systems of describing collections—such
as the widely-used Library of Congress Subject Headings—reify concepts
about persons or cultures that really ought to be interrogated more
closely or perhaps discredited and dismantled all together. For the most
part, librarians, archivists, and information scientists acknowledge
these flaws and perhaps even work to remedy them in the course of
maintaining systems that preserve whatever partial archives do exist or
helping patrons to find information they need.

We are looking for new forms of collective action that can be expressed
through the professional work of humanities scholars and librarians.
This is not simply a call for the production of more and more
data—attempting to subvert the work of categorization and classification
through the production of ever more local, finely-wrought distinctions,
details, qualifications. Our aim is to develop ways of working that
validate local experiences of data without removing them from a more
global network of information exchange. These practices, as we imagine
them, resonate with [Bethany Nowviskie’s
interpretation](http://nowviskie.org/2016/everywhere-every-when/) of
the Afrofuturist philosophy of Sun Ra (as expressed by Shabaka
Hutchings), which claims: “Communities that have agency are able to form
their own philosophical structures.” The transition to working in a
linked data paradigm should be valued not principally for the ways in
which it might make large-scale information systems operate more
smoothly, but rather for the ways in which it can create localized
communities of authority, within which people can take control of the
construction of data and the contexts in which it lives. In a [keynote
presentation](http://matienzo.org/2016/to-hell-with-good-intentions/)
at the 2015 LITA Forum Mx (Mark) A. Matienzo articulated a parallel
version of this view, saying:

> We need to begin having some serious conversations about how we can
> best serve our communities not only as repositories of authoritative
> knowledge or mere individuals who work within them. We should be
> examining the way in which we can best serve our communities to
> support their need to tell stories, to heal, and to work in the
> process of naming.

Discussions of “cleaning” data fails to capture this need. The cleaning
paradigm assumes an underlying, “correct” order. However tidy values may
look grouped into rows or columns or neatly-delimited records, this
tidiness privileges the structure of a container rather than the data
inside it. This is the same diversity-hiding trick that nonscalability
theory encourages us to recognize.

It is not enough to recognize; we also wish to offer a way of working.
In arguing against cleaning, we propose index-making. In this approach,
the first things we would do with our data sets, rather than normalize
them, is find the communities within which our data matters. With those
communities in mind and even in dialogue, we would ask, what are the
concepts that structure this data? And how can this data, structured in
this way, point to other people’s data? This way of thinking allows us
to see the messiness of data not as a block to scalability but as a
vital feature of the world which our data represents and from which it
emerges.

#### Please cite as
{: .article-section-head}

Katie Rawson and Trevor Muñoz, “Against Cleaning,” Curating Menus, <span class="date-span">July 7, 2016</span>, http://www.curatingmenus.org/articles/against-cleaning/.

#### Notes
{: .article-section-head}

<div class="footnotes" id="notes-against-cleaning">
    <ol>
        <li class="footnote" id="fn:1">
            <p>Cf. Hadley, Wickham, "Tidy Data." <em>Journal of Statistical Software</em>, 59.10 (2014): 1 - 23. doi: <a href="http://dx.doi.org/10.18637/jss.v059.i10">	10.18637/jss.v059.i10</a>. <a href="#fnref:1" title="return to article">&#8617;</a></p>
        </li>

        <li class="footnote" id="fn:2">
            <p>The fact that these communities have developed discourses for describing the boundaries of the claims they make does not inoculate them from critique about the costs and shortcomings of their methods. Cf. Bruno, Latour, "Why has critique run out of steam? From matters of fact to matters of concern." <em>Critical Inquiry</em> 30.2 (2004): 225-248.<a href="#fnref:2" title="return to article">&#8617;</a></p>
        </li>

        <li class="footnote" id="fn:3">
            <p>For a variety of reasons, we would not recommend this course of action to others without serious deliberation.There is a reason why applications like Open Refine are so popular and useful. If you would like to know more, contact us.<a href="#fnref:3" title="return to article">&#8617;</a></p>
        </li>
         <li class="footnote" id="fn:4">
            <p>If we had a dictionary to compare these materials too, the process may had been more automatable; however, from what we have found thus far, that particular language resource&mdash;Wordnet for Oysters!&mdash;doesn’t exist.<a href="#fnref:4" title="return to article">&#8617;</a></p>
        </li>
        <li class="footnote" id="fn:5">
           <p>Anna Lowenhaupt Tsing. "On Nonscalability: the Living World Is Not Amenable to Precision-Nested Scales." <em>Common Knowledge</em>. 18.3 (2012): 505-524.<a href="#fnref:5" title="return to article">&#8617;</a></p>
       </li>
        <li class="footnote" id="fn:6">
            <p>Michael Lascarides and Ben Vershbow, “What’s On the Menu?: Crowdsourcing at the New York Public Library,” Crowdsourcing our Cultural Heritage, ed. Mia Ridge (Surrey, UK: Ashgate, 2014).<a href="#fnref:6" title="return to article">&#8617;</a></p>
        </li>

        <li class="footnote" id="fn:7">
            <p>The NYPL menu collector Frank E. Buttolph’s acquisition practices reinforce the role and scale of printers in menu production in the twentieth century. In addition to restaurants and customers, she went straight to the menu source&mdash;printers&mdash;to fill out her collection.<a href="#fnref:7" title="return to article">&#8617;</a></p>
        </li>
        <li class="footnote" id="fn:8">
            <p>Cf. Tsing 519<a href="#fnref:8" title="return to article">&#8617;</a></p>
        </li>
        <li class="footnote" id="fn:9">
            <p>Andrew Stauffer. "The Nineteenth-Century Archive in the Digital Age,"
            <em>European Romantic Review</em>. 23:3 (2012): 335-341. doi: <a href="http://dx.doi.org/10.1080/10509585.2012.674264">10.1080/10509585.2012.674264</a>.<a href="#fnref:9" title="return to article">&#8617;</a></p>
        </li>
        <li class="footnote" id="fn:10">
            <p>Early versions of the project interface featured a social-media-style call-to-action below the image snippet (“What does this say?”), as well as brief instructions below the text input box: “Please type the text of the indicated dish EXACTLY as it appears. Don't worry about accents” (see an example at the <a href="https://web.archive.org/web/20120102212103/http://menus.nypl.org/menu_items/664698/edit">Internet Archive</a>). This accompanying text was quickly dropped—presumably because the task seemed self-evident enough from the layout of the transcription screen.<a href="#fnref:10" title="return to article">&#8617;</a></p>
        </li><li class="footnote" id="fn:11">
            <p>See <a href="https://datasymposium.wordpress.com/sahle/">https://datasymposium.wordpress.com/sahle/</a>.<a href="#fnref:11" title="return to article">&#8617;</a></p>
        </li>
    </ol>
</div>
