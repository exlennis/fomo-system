---
title: "How to Use Tags"
source: "https://karl-voit.at/2022/01/29/How-to-Use-Tags/"
author:
  - "[[Karl Voit]]"
created: 2025-03-13
description: "How to Use Tags"
tags:
  - "clip"
  - "research"

---
- Updates
- 2024-01-22: Business example with large number of tags in Rule 2
- 2024-04-28: Added rule 9 and 10

[I do have some academic background with tagging](https://karl-voit.at/tagstore/en/papers.shtml), the process of assigning labels or tags to entities such as headings in my knowledge system or file names. I designed [tagstore](https://karl-voit.at/tagstore/) as a research platform to study tagging behavior in different configurations and I developed the concept of TagTrees which I also used in [my filetags method and tool-collection](https://karl-voit.at/managing-digital-photographs) which is the basis of my personal file management.

However, this article here is something I came up with **personal experience** while using [tags](https://en.wikipedia.org/wiki/Tag_\(metadata\)) and tagging methods over many years in my own setup. From this experience, I derived some general rules I do think that may be applied to any personal tagging workflows.

Disclaimers: The things mentioned here can not be applied to [social or collaborative tagging](https://en.wikipedia.org/wiki/Folksonomy) in general. I refer to file tagging many times but it is just as an example use-case. The rules mentioned here should apply to personal tagging with other types of entities as well.

To my surprise, we tend to think in hierarchical categories all the time. As I have written in my article on [Logical Disjunct Categories Don't Work](https://karl-voit.at/2017/04/18/classification), **the real world does not fit into disjunct categories.**

Therefore, we should embrace multi-classification more often. If you do want to learn more about the rationale, you may as well read [the first chapters of my PhD thesis](https://karl-voit.at/tagstore/downloads/Voit2012b.pdf) or [the book "Everything is Miscellaneous"](https://www.everythingismiscellaneous.com/) by David Weinberger, just to give you two resources of many.

Long story short: tagging does take away the burden of finding one single spot in a strict hierarchy of entities which is actually a heavily intertwined network of concepts we do find in the real world. It's far from being a neat hierarchy. Everybody who tries to put "the world" into a strict hierarchy will fail.

Unfortunately, tagging is no process that works flawlessly as soon as there is a tool which allows you to apply tags to entities of some sort. **It seems like tagging is intuitive but it is not.**

I want to give you one example that should be able to explain why tagging behavior is something that needs to be curated itself as well. Imagine you do have some sort of [personal tagging tool for local files](https://karl-voit.at/managing-digital-photographs). Imagine furthermore that you tag your files after a double minus separator similar to that example:

```
 Tom and Julie -- people couple holiday tom julie relatives portraits nice.jpeg	  
```

For this particular photograph, you entered all potential tags that came to your mind. The rationale is that those "descriptive tags" help you re-find the image when you're looking for files with relatives from any holiday and so forth. Actually, this is something we all would like to have and use.

In the long run, you will notice that you've ended up with at least hundreds of different tags. Retrieving files now got very tedious because you can't remember them. In particular, you won't use all matching tags on matching files. Therefore you may end up with something like that:

```
 Julie hugs Tom -- persons beautiful funny vacation uncle faces.jpeg	  
```

As you can see, this file is extremely similar to the first example. Yet, you have tagged it using a totally different set of tags. There is not even one single tag matching the other set of tags. If you think of any tag-based retrieval process, you can not get both pictures with one search query based on those tags - as similar as they are.

I do think at this moment, we can agree that tagging does need some sort of guidelines in order to get a helpful tool for information retrieval. And **information retrieval is the main reason why we do apply tags** in the first place. Never forget that in this context.

In [the 45 minute video of a talk I gave](https://media.ccc.de/v/GLT18_-_321_-_en_-_g_ap147_004_-_201804281550_-_the_advantages_of_file_name_conventions_and_tagging_-_karl_voit) which is liked [on my filetags article](https://karl-voit.at/managing-digital-photographs), I came up with an initial list of best practices on how to tag. I took that list as a basis and extended it with further tips. Here is the current set of rules of no particular order. I'll keep maintaining the list of rules here. Come back for any potential future updates.

1. Use as few tags as possible.
2. Limit yourself to a self-defined set of tags.
3. Tags within your set must not overlap.
4. By convention, tags are in plural.
5. Tags are lower-case.
6. Tags are single words.
7. Keep tags on a general level.
8. Omit tags that are obvious.
9. Use one tag language.
10. Explain your tags.

I will elaborate on each rule in the upcoming sections because I do think that rules are of very limited use if you don't understand the rationale behind.

The example in the previous section should made clear why too many tags leads to a bad retrieval situation.

It is very difficult to recommend numbers here. If you do tag hundreds of files that are from similar situations, you may be able to stick with maybe a dozen different tags. If you only want to mark files with "confidential", "internal" and "public" you end up with exactly three different tags. If you are curating thousands of photographs of animals, you may want to have hundreds of different tags and still got an efficient tool for tag-based retrieval.

Therefore, my recommendation is to start with only a few tags and add more tags if you **really** do come up with good reasons for them.

Related to rule number one, a so-called [controlled vocabulary](https://en.wikipedia.org/wiki/Controlled_vocabulary) is able to help you curating that finite set of self-chosen tags.

While a handful of tags can easily be memorized, any higher number of tags lead to situations where only good tool-support is able to help you. If you're using a tagging tool that allows to maintain this controlled vocabulary, it might as well accept only pre-defined tags at the actual tagging process. This is a good thing to have when you want to maintain tag consistency.

I also recommend you to maintain a curated list of tags and their definition. Concepts can be misunderstood and they change over time. By having one central definition per tag helps yourself and your peers.

Using a controlled vocabulary also prevents you from accidentally using [synonyms](https://en.wikipedia.org/wiki/Synonym), [homonyms](https://en.wikipedia.org/wiki/Homonym) or mixing up singular and plural forms which we discuss in rule number four.

I would like to add that there may be good reasons for a larger number of tags in your controlled vocabulatory in certain situations. For example, if you think of a company using the filetags method, I do think that a fairly long list of customer, supplier and project tags in your controlled vocabulatory is not a bad idea in the first place.

The reason is that you will most probably not ending up with applying more than one or two customers for one particular file even if you do have hundred customers in your controlled vocabulatory. You'd only get issues when you'd like to tag a newsletter file with, e.g., all client tags - that would be cumbersome and may lead to bad retrieval and also technical issue due to long file names. You could think of a tag like "allcustomers" for situations like that.

But still: start with as few tags as possible even here so that you don't end up with more than - let's say - five to seven tags for any given file. That's the actual goal here.

Tags need to be clearly distinctive from each other. Furthermore, tags should not overlap with respect to their meaning. If you do use "sports" and "soccer", you might tend to use "sports" for some soccer files instead of both or only "soccer".

There is one exception: tag hierarchies are able to provide some relations between different tags. For example, you may be able to use a tagging solution that allows you to define the following set of tags:

```
 sports (soccer volleyball biking)	  
```

The idea behind tag hierarchies is that when you retrieve files via the "sports" tag, you get also files that are tagged with "biking" and not "sports". Many people do think this is a great help. I personally prefer not to use such a feature because it complicates many use-cases. Furthermore, all retrieval methods need to support those tag hierarchies which usually limits my possibilities.

The reason for this rule is simple: when applying tags or trying to come up with a tag-based search query, you should not be confused if it is "bicycle" or "bicycles". A simple solution is that you either choose the singular form or you stick to the plural form.

When I was looking into that issue many years ago, I realized that most (social) tagging systems settled for the plural form back then. I was not particular happy about that but I've learned that going against well-established conventions may cause pain later-on. So I adapted the plural convention for myself as well.

You can argue that the plural form does make sense if you think of «a bicycle is part of the set named "bicycles"». Furthermore, it would be a bit weird to tag an item related to a handlebar with "bicycle" because this could be interpreted as «a handlebar is a bicycle» which is not true. However, it seems to be a clean approach when you interpret it as «a handlebar is associated to the set related to "bicycles"».

Of course, your mileage may vary here. If [you decide to stick to the singular form](https://helpdeskheadesk.net/help-desk-head-desk/2022-01-24/) it perfectly fine as long as you stay consistent within your own tagging system.

It is noteworthy that I do not follow the plural rule that strictly. If there is a word that is well fitting such as "[education](https://karl-voit.at/tags/education)", "[cloud](https://karl-voit.at/tags/cloud)" or "[emacs](https://karl-voit.at/tags/emacs)", it might be a perfect tag as well although they are not in a plural form.

The thing with lower case is related to avoiding conflicts just like the previous rule. It should avoid situations like «did I choose "Emacs" or was it "emacs"?».

Of course, this only applies for tools that are [case-sensitive](https://en.wikipedia.org/wiki/Case_sensitivity). And yes, even when your main tool is case-insensitive, allowing "emacs" and "Emacs" for the same result set, you need to think of all retrieval methods you might be using in the future. Some of them might not be case-insensitive and then you do get an issue.

Just like the previous rule, the "only a single word" rule is a workaround to avoid tool-related issues. Some tagging solutions are perfectly fine with spaces and even special characters like emoticons. I would not assume that this holds true for the majority of tagging solutions. If you want to be on the safe side, you should stick to single words.

As you can see in my "[restaurants\_bars](https://karl-voit.at/tags/restaurants_bars)" tag, I connect them with underscores. With "[tugraz](https://karl-voit.at/tags/tugraz)" for "TU Graz" I somehow decided to omit the space and connected the two parts without any character in-between. As a general rule, I probably would settle for "-" or "\_" to separate different words within a tag.

In order to comply with rule number one (as few tags as possible), you need to accept that you can't use tags that are too specific and describe every aspect of the entity about to be tagged.

Therefore, tags need to be as general as possible. I merged the tags "automobile", "airplane" and similar to the one tag "[transportation](https://karl-voit.at/tags/transportation)".

Yes, I still stick to "[bicycles](https://karl-voit.at/tags/bicycles)" which could be merged as well here but since I blog more about bicycle-related stuff than about the rest of "transportation", I made this decision deliberately. Readers might be confused here, I agree.

Back to this rule. I would recommend you to prefer categorizing tags over descriptive tags. Omit "volleyball" when you can use "sports". Try to tag things with a more general category than you would probably think. This makes much sense since as an extreme example "each document has its own tag" would not support retrieval tasks properly.

I once read an interesting quote from [WallyMetropolis](https://www.reddit.com/user/WallyMetropolis/) on [reddit](https://www.reddit.com/r/emacs/comments/hg2m5s/zettelkastenorgroamorgbrain_is_crap/). It was in the context of knowledge management using tags and links between different notes:

> Tags are doors and links are corridors. Tags are how you enter a building, and links are how you navigate around once you're in. So you'll in general have few tags and not every note will have a tag. But you'll want many links.

That is a nice picture, I think.

I once called this rule «don't use tags that can be derived from the [filename extension](https://en.wikipedia.org/wiki/Filename_extension)». Since I can think of other obvious tags, I generalized this rule even more.

According to this, I would not recommend using tags like "images", "spreadsheets" or "photographs".

As a matter of fact, I actually do use a file-tag "presentations" which seems to contradict the rule. The reason for this is that I may store all kinds of material in different file formats that refer to presentations somehow: classical `.pptx` or `.odp` presentation files, photographs of slides during talks, sound recordings and videos of talks, presentation slides as PDF files, and so forth. Without the "presentations" tag, I would not be able to retrieve slide material according to file format filters and similar.

This rule is directly related to the rules number 2 (few tags) and 7 (generic tags). It follows a similar pattern like rule number 3 (tags shouldn't overlap), 4 (tags in plural) and 5 (lower case tags).

To avoid having similar concepts as separate tags you should stick to one single language. For my personal use-case, I've decided to stick to tags in the English language even though I've got substantial content in German. This way, I don't need to remember my tag language during the retrieval process.

Curating a list of tags also means that you remember the reason and the context for a specific tag over a long period of time.

In order to help your future self particular with tags you don't use that often, you should write down brief descriptions for each tag. You'll be surprised how easily you'll misinterpret your own choices in future.

In case your tagged items are consumed by other people as well, you really should put great effort into good explanations of your controlled vocabylary. This is why I created "tag pages" with descriptions for [most of my tags on my blog](https://karl-voit.at/tags/).

If you read about [the vocabulatory problem](http://dl.acm.org/citation.cfm?id=32212&dl=ACM&coll=DL&CFID=752355508&CFTOKEN=83542636), you will understand that this is much more important than you might think. I also talked about that in my video from [the Worklab 2023](https://karl-voit.at/2023/11/05/worklab23).

In this section, I would like to elaborate on a few things that might turn up when talking about tagging.

I honestly don't know if there is an official term for this. What I do mean are tags that consist of keys and associated values. Here are some examples:

```
 size:big • size:small
 security:public • security:internal • security:confidential	  
```

They are a simplified form of the "triple tags" mentioned [here on Wikipedia](https://en.wikipedia.org/wiki/Tag_\(metadata\)#Special_types). And the "triple tags" are directly related to [the semantic triples](https://en.wikipedia.org/wiki/Semantic_triple).

Google lets you search for `foobar type:pdf site:.at` which returns only documents of the file format PDF which are provided by web servers whose [TLD](https://en.wikipedia.org/wiki/Top-level_domain) is from Austria.

Personally, I love those key-value tags and I would like to re-use the well-established `key:value` form. Unfortunately, tagging files is an important part of my personal tagging workflows. While the colon is a perfectly fine character for my main systems which run GNU/Linux, I would not be able to copy those files to a much more restricted [file system from Microsoft where colons are not allowed at all](https://docs.microsoft.com/en-us/windows/win32/fileio/naming-a-file).

Currently, I don't use key-value tags in my personal tagging systems. Most probably because I avoided the additional complexity in tool-support when it comes to implementation and handling details.

To me, a file name like the following is quite disturbing to me:

```
 Business Report v0.3.5 final2 with changes.docx	  
```

I do have some questions here.

What does version 0.3.5 stand for? Did this document really go through 0.0.1, 0.0.2, 0.0.3, ..., 0.1.0, 0.1.1, 0.1.2, ... , 0.2.0, ... , 0.3.0, 0.3.1, 0.3.2, 0.3.2, 0.3.3, 0.3.4 and 0.3.5? If so: when is the third number incremented? When the second and when the first?

Why is "final2" still a thing? Of course, the author might have added some changes to the version he or she marked with "final" already.

And "final2 with changes" clearly indicates that naming files this way is not very efficient.

After providing that example which is - to my personal experience - unfortunately a realistic one, I would propose an alternative. How about that?

```
 2022-01-28 Business Report -- final submitted.docx	  
```

The previous stages of that particular file might have been:

```
 2021-12-29 Business Report -- draft.docx
 2022-01-05 Business Report -- draft.docx
 2022-01-17 Business Report -- draft.docx
 2022-01-27 Business Report -- final.docx	  
```

As you can see, the status is indicated by the file-tags, the order and history by the leading date-stamps.

On January 27th, the author tagged the document as final. Then, there were some last-minute changes that lead to yet another final version on 2022-01-28. According to the end result, the version from 2022-01-28 got submitted to the client. Everything is much clearer to me.

I like to think, that this file name history gives much more clues for anybody. Those version numbers didn't add helpful clues anyway and served no particular purpose except defining a linear order with unclear in-between steps.

I referred to aspects like this and much more [in my article on how to design file management for companies](https://karl-voit.at/2021/01/11/company-file-management).

When people start to embrace tagging, they not only tend to violate most rules above. They also tend not to think of many other benefits of tagging or adding meta-data in general.

Just to give you some food for thought, I would like to mention a few of my file-tags and what they do represent for me.

**"selection"**: Imagine you've been abroad for a fine vacation and came back with 1428 photographs you want to keep. Despite the fact that you're an exponentially gifted photographer, it would be cruel to present all photographs to your friends and relatives who feel socially obliged to stay during your eight-hour session with three minutes for each photograph on average. For cases like that, I prefer to add the tag "selection" to a much smaller sub-set of must-see photographs for those sessions. This way, I may keep the whole set and be able to present a much smaller selection when appropriate. See the "Tag Filter" feature of filetags mentioned further down.

**"taxes"**: Once in a year, I need to collect all the files that are relevant for my tax adjustment report. Files related to bills all over the year that are tagged with this tag do easy the pain to a great extend.

**"acquisitions scrap"**: When I get new hardware, I usually take some photographs. Partly because of sheer new owner's joy, partly to document things like computer stickers that might get unreadable with time. Those files are tagged with "acquisitions". At the other side of hardware life-time, taking fare-well photos does easy the pain of letting go. I do have something for my memory. Those are tagged with "scrap". It also helps if I'm unsure if I still own an old thing or if I tossed it away.

**"cliparts"**: Images that may be used in presentations or blog articles to represent something specific as a clipart. That tag helps me a lot when looking for visuals.

**"heritage"**: I collect (too) much data in my yearly archive folders. Files tagged with "heritage" are things that I consider very important or representative, similar to physically printed photos in an album. If I'm looking for things of subjective or sentimental value, I may filter for that tag.

**"manuals"**: [After going digital](https://karl-voit.at/2015/04/05/digitizing-paper), I keep my hardware manuals only in digital form. When looking for instructions with a gadget, I can filter for that tag.

**"scan screenshots"**: Scanned documents are tagged with "scan", screenshots from my computer or mobile with "screenshots".

**"confidential internal public"**: The usual security tags.

For [this web site "public voit"](https://karl-voit.at/) and for [my blogging solution "lazyblorg"](https://github.com/novoid/lazyblorg), tags are an essential part of the user experience I try to provide. They are mentioned in [my how to use this blog efficiently](https://karl-voit.at/how-to-use-this-blog), they are the dominant element of my landing page, they are available in the sidebar and they've got [their own tagcloud page](https://karl-voit.at/tags/):

![alterantive-text for the image](https://karl-voit.at/2022/01/29/How-to-Use-Tags/2022-01-28T20.23.01%20Karl-Voit%20tagcloud%20--%20screenshots%20publicvoit%20-%20scaled%20width%20578.png)

A screenshot of my tag cloud from 2022-01-28.

As usual with [tag clouds](https://en.wikipedia.org/wiki/Tag_cloud), the relative size of the tags do represent the amount of blog articles that are tagged with this tag.

Since the tags "hardware" and "software" dominated the tag cloud for the longest part of this site, I've omitted those two tags from the tag cloud.

I would love to see readers using the tags to navigate through my web site. Unfortunately, I don't have the tools to verify my assumption.

To be honest, I don't have all those tags in my head when writing new blog articles. Especially older tags may vanish from my memory. I try to compensate this by deliberately using the tag overview of the pre-defined tags in my Emacs when I choose the tags.

[Here is an article about tag gardening on public voit](https://karl-voit.at/2021/01/02/tag-gardening-publicvoit).

All in all, it's not a perfect result but I do think that it offers good value to my readers. Please do write me a comment if you want to give me some feedback.

After writing so much about tagging and my recommended way to use tags for information retrieval, I would like to mention my personal tool-set when it comes to tagging local files. Some has been mentioned and linked above. If you want an introduction, please [do read my article about filetags and its accompanying tools](https://karl-voit.at/managing-digital-photographs). If you are not interested in reading about my tagging tools, you can skip this promotion with clever and partly unique tagging and retrieval features and jump to the conclusions at the bottom.

[My implementation of filetags](https://github.com/novoid/filetags) supports the tagging process in many ways. I have optimized the user experience over the years so that it does require minimal effort.

Either when you do use the command line or you prefer to use filetags integrated into a graphical file browser, you can select multiple files and add a set of tags to them.

For example, when I go through my new photographs, I select all images that share a tag in [my image browser](https://karl-voit.at/apps-I-am-using), invoke my keyboard shortcut for tagging and add the tags in one go for many files. (Same holds true for [appendfilename](https://github.com/novoid/appendfilename/), by the way.)

When you create a file named `.filetags` in any sub-hierarchy of your file system, filetags is using that as a controlled vocabulary for that sub-hierarchy. Each tag is written in one line. Simple as that.

With a controlled vocabulary defined in a `.filetags` file in the current directory or any parent directory, you will get [tab completion](https://en.wikipedia.org/wiki/Tab_completion) for those tags. If you press `Tab` twice, you get a list of those pre-defined tags.

Even when you want to untag a file for an already assigned tag, tab completion is helping you there. You just have to precede the tag to remove with a minus character like "-foo" and tab completion is able to complete it. After confirming, those tags with a minus character do get removed from the file name.

This is probably the most important feature in order to avoid "inventing new tags" in an unintended fashion.

The `.filetags` file can not only contain one tag per line. If you do write multiple tags in one line, those tags are declared as mutually exclusive tags.

Consider following content of `.filetags`:

```
 draft final
 confidential internal public
 scan screenshots	  
```

Now, let's consider an example file like the following:

```
 2022-01-29 Business Report -- draft internal.pdf	  
```

Furthermore, you would like to finalize this version and mark it as suitable for the public, changing its security level. With filetags, you just invoke your preferred way of tagging and add just the two tags "public" and "final". After that, the file name now looks like that:

```
 2022-01-29 Business Report -- public final.pdf	  
```

As you can see, the tags "draft" and "internal" got replaced because they have been defined as mutually exclusive with "final" and "public" respectively.

I think you get the idea of that and can think of ways this might support your own workflows.

Already mentioned above when I explained the example tag "selection", I would like to write about my filter by tags feature.

Consider you have a directory that contains many of files.

If you want to retrieve a file whose tags you know, you can skim through all the files. However, filetags offers you a more elegant possibility: you can filter the files according to one or more tags.

For example, we take a look at following situation:

```
 $HOME/my party/
 |_ 2021-06-25 Party invitation -- scan correspondence.pdf
 |_ 2021-07-31 Guest list -- correspondence.txt
 |_ 2021-08-01T11.51.44 Uncle Bob arrives.jpg
 |_ 2021-08-01T12.31.42 Sheila with her new boyfriend -- friends.jpg
 |_ 2021-08-01T14.12.23 Start of BBQ with the big steak.jpg
 |_ ...
 |_ 2021-08-01T23.53.19 Even uncle Bob desides to go home -- fun.jpg
 |_ 2021-08-05 Lessons learned for planning a party -- scan.pdf
 |_ 2021-08-06 Thank-you letter Bob -- scan.pdf
 |_ Bills/
   |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
   |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf	  
```

Following command and interaction would generate following temporal link structure:

```
 filetags --filter	  
```

User gets asked to enter one or more tags and she enters "scan". What now happens is that filetags creates a directory whose content consists of links to all matching files from your query. By default, the resulting directory is `.filetags_tagfilter` in your home directory. After invoking for our example, the content of this retrieval directory looks like that:

```
 $HOME/.filetags_tagfilter/
 |_ 2021-06-25 Party invitation -- scan correspondence.pdf
 |_ 2021-08-05 Lessons learned for planning a party -- scan.pdf
 |_ 2021-08-06 Thank-you letter Bob -- scan.pdf	  
```

This way, our user is quickly able to skim through all scanned documents to locate the one desired to retrieve.

To locate all matching files in all sub-directories as well, the user is able to add the parameter `--recursive` ...

```
 filetags --filter --recursive	  
```

... and chooses to enter the tag "scan" which would generate following temporal link structure:

```
 $HOME/.filetags_tagfilter/
 |_ 2021-06-25 Party invitation -- scan correspondence.pdf
 |_ 2021-08-05 Lessons learned for planning a party -- scan.pdf
 |_ 2021-08-06 Thank-you letter Bob -- scan.pdf
 |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
 |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf	  
```

This way, filetags supports selective file retrieval based on tags in an elegant way.

This functions is somewhat sophisticated as it is not a very well-known thing to have. If you're really interested in the whole story behind the visualization/navigation of tags using TagTrees, feel free to read [my PhD thesis](http://karl-voit.at/tagstore/downloads/Voit2012b.pdf) about it on [the tagstore webpage](http://karl-voit.at/tagstore/). It is surely a piece of work I am proud of and the general chapters of it are written so that the average person is perfectly well able to follow.

In short: this function takes the files of the current directory and generates hierarchies up to level of `$maxdepth` (by default 2, can be overridden via `--tagtrees-depth`) of all combinations of tags, [linking](https://en.wikipedia.org/wiki/Symbolic_link) all files according to their tags.

Too complicated? Then let's explain it with some examples.

Consider having a file like:

```
 My new car -- car hardware expensive.jpg	  
```

Now you generate the TagTrees, you'll find [links](https://en.wikipedia.org/wiki/Symbolic_link) to this file within sub-directories of `~/.filetags`, the default target directory: `car/` and `hardware/` and `expensive/` and `car/hardware/` and `car/expensive/` and `hardware/car/` and so on. You get the idea.

The default target directory can be overridden via `--tagtrees-dir`.

Therefore, within the folder `new/expensive/` you will find all files that have at least the tags "new" and "expensive" in any order. This is **really** cool to have.

Files of the current directory that don't have any tag at all, are linked directly to `~/.filetags` so that you can find and tag them easily.

I personally, do use this feature within [my image viewer of choice](https://karl-voit.at/apps-I-am-using). I mapped it to `Alt-T` because `Alt-t` is occupied by `filetags` for tagging of course. So when I am within my image viewer and I press `Alt-T`, TagTrees of the currently shown images are created. Then an additional image viewer window opens up for me, showing the resulting TagTrees. This way, I can quickly navigate through the tag combinations to easily interactively filter according to tags.

Please note: when you are tagging linked files within the TagTrees with filetags, only the current link gets updated with the new name. All other links to this modified filename within the other directories of the TagTrees gets broken. You have to re-create the TagTrees to update all the links after tagging files.

The option `--tagtrees-handle-no-tag` controls how files with no tags should be handled. When set to `treeroot`, untagged files are linked in the TagTrees target directory directly. The option `ignore` does not link them at all. The option `FOLDERNAME` links them to a directory named accordingly to the value which is a sub-directory of the TagTrees target directory.

With the option `--tagtrees-link-missing-mutual-tagged-items` you can control, whether or not there will be an additional TagTrees folder that contains all files which lack one of the mutually exclusive tags. Using the example `winter spring summer autumn` from above, all files that got none of those four tags get linked to a TagTrees directory named "no\_winter\_spring\_summer\_autumn". This way, you can easily find and tag files that don't participate in this set of mutually exclusive tags.

Using the example files from above:

```
 $HOME/my party/
 |_ 2021-06-25 Party invitation -- scan correspondence.pdf
 |_ 2021-07-31 Guest list -- correspondence.txt
 |_ 2021-08-01T11.51.44 Uncle Bob arrives.jpg
 |_ 2021-08-01T12.31.42 Sheila with her new boyfriend -- friends.jpg
 |_ 2021-08-01T14.12.23 Start of BBQ with the big steak.jpg
 |_ ...
 |_ 2021-08-01T23.53.19 Even uncle Bob desides to go home -- fun.jpg
 |_ 2021-08-05 Lessons learned for planning a party -- scan.pdf
 |_ 2021-08-06 Thank-you letter Bob -- scan.pdf
 |_ Bills/
   |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
   |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf	  
```

... and the command line ...

```
 filetags --tagtrees --tagtrees-handle-no-tag "has_no_tag" --tagtrees-depth 2 --recursive	  
```

... filetags generates the temporal link structure:

```
 $HOME/.filetags_tagfilter/
 |_ scan/
   |_ 2021-06-25 Party invitation -- scan correspondence.pdf
   |_ 2021-08-05 Lessons learned for planning a party -- scan.pdf
   |_ 2021-08-06 Thank-you letter Bob -- scan.pdf
   |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
   |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf
   |_ correspondence/
     |_ 2021-06-25 Party invitation -- scan correspondence.pdf
   |_ taxes/
     |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
     |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf
 |_ correspondence/
   |_ 2021-06-25 Party invitation -- scan correspondence.pdf
   |_ 2021-07-31 Guest list -- correspondence.txt
   |_ scan/
     |_ 2021-06-25 Party invitation -- scan correspondence.pdf
 |_ friends/
   |_ 2021-08-01T12.31.42 Sheila with her new boyfriend -- friends.jpg
 |_ fun/
   |_ 2021-08-01T23.53.19 Even uncle Bob desides to go home -- fun.jpg
 |_ taxes/
   |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
   |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf
   |_ scan/
     |_ 2021-07-30 Beverages by FreshYouUp -- scan taxes.pdf
     |_ 2021-08-03 Bill of the butcher -- scan taxes.pdf
 |_ has_no_tag/
   |_ 2021-08-01T11.51.44 Uncle Bob arrives.jpg
   |_ 2021-08-01T14.12.23 Start of BBQ with the big steak.jpg
   |_ ...	  
```

This looks complicated because there are many links generated the user does not really need. The beauty of this solution is that the user is able to navigate to a file using a wide set of different paths (the TagTrees) and she is able to choose the one path that suits the current cognitive model.

For example, she might want to retrieve "the one document from the last party which she remembers of having scanned and which she used for the invitation correspondence". With this mind-set, she most likely retrieves the document via `$HOME/.filetags_tagfilter/scan/correspondence/` or `$HOME/.filetags_tagfilter/correspondence/scan/` (does not matter which).

The large number of other TagTrees can be ignored for this retrieval task.

Another retrieval task example would be "all photos that do have no tag in order to continue tagging the photos". In this example, the user visits `$HOME/.filetags_tagfilter/has_no_tag/`, fires her image viewer (which has filetags integrated already - see below) and continues with the tagging activity. Since filetags synchronizes the tags within TagTrees linked files and the original files, the original files get renamed accordingly.

Just invoke `filetags --tag-gardening` or `filetags --recursive --tag-gardening` and read its output to learn about helpful analysis results to curate your tags. My personal favorites are:

- I am able to find typos in tags (tag count is low and similar tags are found).
- I can determine tags I seldom use and therefore might be removed from CVs.
- Statistics on tag usage like, e.g.:
- Distribution of mutually exclusive tag options.
- Fraction of files that are not tagged.
- Tags I have used which are not in my CVs.
- Unused tags.

This feature is really powerful when it comes to maintenance of your file tags or get some insight related to your tagging patterns.

My concepts and tools around filetags and its tools were also described in two [publications of mine](https://karl-voit.at/clippings). [LinuxUser 03.2020](https://www.linux-community.de/magazine/linuxuser/2020/03/) (German) and [The Linux Magazine](https://www.linux-magazine.com/) featured my workflows in [its July 2020 issue](https://www.linux-magazine.com/Issues/2020/236). My article was even the main headline on [the title page](https://www.linux-magazine.com/Issues/2020/236). ;-)

If you are interested in synchronized tags between two different tools, you might be also interested in the papers by Richard Boardman and his research group from around 2000-2005. The way I'm using blog articles and files, a merged set of tags does not make sense that much to me. My two sets overlap only to a certain degree and are distinct otherwise. Yours might differ, of course.

It is important to know that the tagging method itself (independent of any tool implementation) is something that is not straight forward. You can start using tags in a way that does not give you as many benefits as you may be able to get with a better tagging concept.

Parts of this can be described with general recommendations which I tried to collect and present here.

Other parts of that story you have to find out yourself. This is the part that everybody needs to explore themselves. It's hard to give recommendations for the overall process because it heavily depends on the data used and the set of the exact retrieval situations.

Remember: **you don't tag for the filing process, you should always and only tag for your future retrieval processes**. This involves "knowing yourself", "observing yourself" and - unfortunately - also "predicting the future" of some sorts.

- 2022-01-29: [Discussion on reddit](https://www.reddit.com/r/datacurator/comments/sfn9fw/how_to_use_tags/)