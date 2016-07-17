---
layout: post
title:  "Adding mappable data to non-map records (for libraries and archives)"
date:   2014-10-16
categories: talks
---


The question:

> I’m curious to find people who are encoding coordinates (or
> standardized addresses) in library records for non-map materials.
>
> I know that there are spaces within Dublin Core
> (<http://dublincore.org/documents/dcmi-point/>), MARC (255 or 034) and
> VRA Core for including coordinates, but I haven’t found examples of
> catalogers who are routinely specifying either geographic coordinates
> or standardized addresses for non-map materials.
>
> A few examples:\
> 1) A book describing the history of a particular building or
> intersection\
> 2) A lithograph of a 19th century street scene\
> 3) A photograph of a person in front of a recognizable building\
> 3) A manuscript collection related to the history of a particular
> place.
>
> Some context: I’ve recently worked with students ~~and “hacktivists”~~
> on pulling data out of library systems and exploring those data
> through various data visualization tools. We’ve found that the
> geographic data in many of the records is often either not included or
> not standardized, so that a lot of data cleaning needs to be done in
> order to map the contents. However, in many cases, an addresses or
> other standard geographic information is included in plain text notes
> field.
>
> A collection of Philadelphia librarians and archives would like to
> learn from someone who has already established best practices for
> coordinate-level or address level encoding of places.

The answers fell into a few categories

1) Encouragement
----------------

Quite a few people wrote saying that they had struggled with this
question or variations of it, or that they had collections that would
really benefit from a good answer to these questions. That was great to
hear, and I appreciated those responses quite a lot.

2) Approaches based on taking advantage of the coordinates that are included in Geographic **Authority files.**
---------------------------------------------------------------------------------------------------------------

Some background on this approach if you’re not a librarian is at the
very bottom of this post.

The two geographic authority files that I know of that are most widely
used in libraries, archives, and museums are the Getty Thesaurus of
Geographic Names
([TGN](https://www.getty.edu/research/tools/vocabularies/tgn/)),  used
very widely in visual resource description and lots of other contexts,
and the Library of Congress [Name Authority
Files](http://www.loc.gov/aba/pcc/naco/geogfaq.html) (which include
Geographic names as ‘corporate names’) which is used most widely in MARC
records for library catalogs.

The responses in this category tended to point out that geographic name
authority records often include coordinates. This is awesome and
important. However, it’s worth pointing that the TGN explicitly states
that their coordinates aren’t really for mapping, and the LC Name
Authority files for geographic names are not complete as far as I can
tell. I really love this idea, but I don’t think I got any examples back
from my query where people were using these authority records to do
mapping directly. Instead, they mostly re-processed the geographic info
after cataloging, as in 3 below.

3) Approaches to encoding the geographic information after the item is cataloged.
---------------------------------------------------------------------------------

There were a few cases where I was pointed to a map of some collection,
but generally when I followed up with the makers of the site, they had
actually pulled the records out of the system and then geocoded them
separately, through an API with lots of data cleanup, or some by hand.
There’s lots of interesting work being done there, and still to be done,
but it doesn’t address my particular question, which is how metadata
records could be created that wouldn’t require that.

### 4) Using the Address or Coordinates Fields in Dublin Core or MODS

Both MODS and Dublin Core allow space for geographic coordinates
directly in the records (it’s in DC-extended).  I think that is awesome.
It still doesn’t solve the problem of knowing what level of geographic
specificity is being used so you would need a lot of rules about what
coordintaes one would use. After all, real places aren’t actually points
— they take up space and frequently have fuzzy boundaries. But it was
gratifying to hear of a few places that were using this approach (see
below for the two examples).

Overall Struggles with Geographic coordinates in records
--------------------------------------------------------

1\) Geojson would be awesome. How would a cataloger do that technically?

2\) Who makes the decision about what constitutes “Delaware Valley” or a
neighborhood called “East Passyunk neighborhood”

3\) For images, geographic coordinates are the simplest, and even better
the coordinates of the viewer if you’re cataloging a photograph or
painting.

4\) Addresses change over time, so you’d need current address and
historic address, which I haven’t seen anyone doing. (especially for old
places like Philadelphia, where the same physical building might have
had a dozen addresses over its life)

 

Relevant Links and Resources:

-   Hardy, D., & Durante, K. (2014). [A Metadata Schema for Geospatial
    Resource Discovery Use
    Cases](http://journal.code4lib.org/articles/9710). Code4Lib
    Journal, (25).
-   a [discussion recently on how to deal with bounding
    coordinates](http://listserv.loc.gov/cgi-bin/wa?A1=ind1410&L=mods)
-   Harvard seems to working on adding coordinates to non-cartographic
    materials: <http://sanger.hul.harvard.edu:8080/geohollis>
-   <div>

    Ohio History Connection (formerly Ohio Historical Society) is doing
    with such collections as these:  
    <http://www.ohiohistoryhost.org/ohiomemory/learning-resources/then-and-now-maps>
    and 
    [http://www.remarkableohio.org/Index.aspx ](http://www.remarkableohio.org/Index.aspx)

    </div>

<!-- -->

-   <http://connect.ala.org/files/Cartographic_Resources_CIG_Midwinter_2014_detailed.pdf>
    — great place to look for discussions of how MARC data has been used
    to make maps, and some of the trouble with encoding points data
    in maps. Also a good description of why and how bounding boxes and
    points are not the best sources for this.
-   <http://www.stonybrook.edu/libmap/coordinates/seriesb/no8/b8.htm> –
    mostly about cataloging maps, but addresses some specific issues
    with coordinates-based approach.

 

———————————————————————————

Descriptions of Current Practices at two places:

**UCONN**

> Our digital repository uses MODS 3.5 which doesn’t have an element for
> historic or current address. There’s the cartographics subelements but
> this is only scale, projection, and coordinates. A lot of our digital
> content about Connecticut has metadata that lists the historic or
> current address of where the image was taken. It was necessary to keep
> this information. Lacking an appropriate slot, we decided on the MODS
> element with a type value of historic/current address. This looks like
> . We’ve used these for our non map materials that have any information
> about addresses. For our maps, the information can also have this
> information or is more specific to FGDC with bounding coordinates and
> not a physical address.
>
> If you are using MODS, you can always use the MODS and put in any
> schema and information you want whether it is VRA, FGDC, DC, etc. For
> coordinates, I would look at the MODS list. I started a discussion
> recently on how to deal with bounding coordinates
> (http://listserv.loc.gov/cgi-bin/wa?A1=ind1410&L=mods).\
> For the bounding box coordinates, we map these to and use FGDC and not
> geoRSS and we also map to one MODS field. That way we have information
> in both places just in case. We selected FGDC because it is better for
> bounding box information and we will be migrating information from
> ArcGIS to our digital repository which can be exported as FGDC; this
> means we can store the entire FGDC record in the mods.
>
>  
>
>  

**UCLA**

> We have been routinely supplying coordinates for digitized visual
> resources (mostly photographs) for a few years now, and are in the
> midst of designing a public digital library portal that will allow
> users to browse our collections on a map, as well as by more
> traditional means such as subjects, genres, names, etc.
>
> Part of the reason we began doing this is that we saw how hungry
> various UCLA GIS projects were for resources that had coordinates.
> Initially, all we could give them were maps, since the existing
> metadata already contained coordinates. Then we branched out to
> enhancing the metadata for our Los Angeles Times photograph
> collection, because so many of the locations were easily identified
> either by the photograph itself (e.g. street addresses or
> intersections), the existing metadata, or by a quick check of the
> article the photographs originally ran with (accessed via the ProQuest
> Los Angeles Times database). Since then, we have expanded to other
> digital collections as part of our standard practice whenever we are
> creating or enhancing metadata for digital collections.
>
> We ask our catalogers to try to identify the spot where the
> photographer was standing, if possible, or an exact address for the
> location. If that degree of specificity is not possible, we try to
> identify the location within the equivalent of a block or two. If we
> can only identify the city, we don’t geotag that particular resource;
> at some point, we hope to automate the geotagging of resources that
> don’t have coordinates already in the metadata—although we are still
> exploring the best way to do that!
>
> Currently we’re using this tool to help identify coordinates:
> <http://itouchmap.com/latlong.html>
>
> We’re in the midst of migrating from a locally-created DAMS to
> Islandora, so this metadata is stored in a variety of ways now, but
> eventually we are planning to map it all to MODS.

Next post:\
Report from the [Best Practices in Geospatial metadata at
DLF](http://sched.co/1qrffQn).

 

 

Notes for the non-librarian on Authority files:

(If you’re a librarian and can suggest ways I can make this simpler or
clearer or more accurate, I’d appreciate it)

“authority files” are closely kept lists of terms that serve as the
Authority for catalogers who create metadata. An over-simplified (and
possibly somewhat inaccurate) example follows. When she published
something that needed cataloging, a name authority file was created for
[danah boyd](http://lccn.loc.gov/no2009022548). It includes her birth
data, and is linked to another variation of her name. That way, when
further works of hers are cataloged, the catalogers will know exactly
how to spell her name, and the appropriate “see” references will make
their way into local catalogs for her.

In general, cataloging practices for a particular collection will
describe the [metadata
standards](http://en.wikipedia.org/wiki/Metadata_standards#Available_metadata_standards)
that will be used (Dublin Core, MARC, MODS,  VRA Core, etc), as well as
the authority files to which the catalogers should look to get the
names.
