---
title: "Semantic Directory Names (Singular or Plural)"
source: "https://stackoverflow.com/questions/17034823/semantic-directory-names-singular-or-plural"
author:
  - "[[Stack Overflow]]"
created: 2025-03-13
description: "Does the name of a directory title 'the container' or the 'contents'? This question nags at me because if the name of a directory semantically titles 'the container' then the name should be singula..."
tags:
  - "clip"
  - "research"

---
Does the name of a directory title 'the container' or the 'contents'? This question nags at me because if the name of a directory semantically titles 'the container' then the name should be singular. (By analogy: When referring to an actual physical bag that contains your groceries - one would probably refer to it as a 'grocery' bag and not the 'groceries' bag.) Conversely if one were to assert that the name of the directory titles the contents of the directory then it would make more sense to use a plural form.

I understand that there are common-sense and even usability concerns associated with this question; however, although I would like to hear the practical results of these two options I am more concerned with semantics.

So in summary: does the name of a directory serve as a title for the container or the contents?

## 4 Answers

### Answer 1

A directory on its own needs no name as a directory without any content is useless. Directories exist to group a set of files together. Even if a directory is currently empty, it represents such a group, just that there are currently no files in this group and that's why it is empty. So the name of a directory should always describe what you can find within that directory.

Assume you have a drawer with boxes and you use these boxes to group physical objects together. To know what is inside each box without having to first open it and look inside, you label the boxes. How would you label these boxes?

If a box contains pencils, you'd label it *Pencils* and not Pencil, correct? If a box contains paper clips, you'd label it *Paper Clips* and not Paper Clip, wouldn't you? That's because in these cases the label only describes *the **kind** of item to be found within the box*. Same goes for directories. A directories containing pictures should most likely be named *Pictures*, so you know that the files you can find inside it are of type picture.

But sometimes you group items together, not because they are of the same kind but because they belong to the same "entity". E.g. if you have a large box that contains all items related to your trip to Japan in 2012, you would label it "*Trip to Japan, 2012*" or maybe just "*Japan, 2012*". Actually you could label it "*Trip to Japan in 2012 Items*" but "Items" is redundant, as it is obvious you will find items inside. The same way it is redundant to add "Files" to a directory name. So if you are not grouping files because the files itself have something in common but because they belong to a common "entity", you usually name the directory after that entity and since is only one such entity, it would be singular.

A directory with the pictures of Peter's Birthday would most likely be named *Pictures/Peter's Birthday*. On the other hand, if you keep pictures of every birthday of Peter, year after year, you would rather use a structure like *Pictures/Peter's Birthdays/2016*. Note how it suddenly became "Birthday**s**" as now the directory name again describes the kind of items found inside and not an individual event/purpose.

**As a general rule of the thumb:** Always name directories in such a way that the reader of the directory name has a very good idea of what kind of files and other directories they can expect to find inside that directory, so they can decide whether it's interesting to "go there" or not by just having read the directory name.

If you name a directory *Recipe*, what will the reader expect to find inside? I would expect to find one or more files, all belonging to a single recipe, e.g. a short ingredient list, a longer instruction text and maybe some supporting photos. Contrary, if you name the directory *Recipes*, what will the reader expect to find there? I would expect several recipes, either multiple files and every file contains one recipe or multiple sub-directories and each one contains the files that belong to one recipe. As you can clearly see by this simple example, whether you choose plural or not has an effect on the expectation of the reader.

### Answer 2

My first impulse is to say that you name a generic container based on its contents. But I'll dig a little deeper just for the fun of it. (Scroll to the end if you just want the summarised conclusion.)

Firstly, I don't think Tum's car and cake examples help us very much. Sure, they are made from simpler components, but only for the purpose of creating new and self-contained objects. The grocery bag is a collection of molecules—so what. The more meaningful thing to ask is: is the object's fundamental purpose to hold other objects? In other words, is it a generic container, like the folder in a file system? You would definitely answer *no* to the cake. You would probably answer *no* to the car (even though it does, admittedly, hold people). You would certainly answer *yes* to the grocery bag.

In your grocery bag example, you said we would refer to it as a *grocery* bag and not the *groceries* bag. Sure. The following sentences are all grammatically correct and natural sounding:

1. Would you help me bring the *bags* in?
2. Would you help me bring the *grocery bags* in?
3. Would you help me bring the *groceries* in?
4. Would you help me bring the *shopping* in?’

The first sentence is only meaningful if the listener knows we just went shopping and can infer the contents of said bags without us telling them. Without that information, the bags might, for all we know, contain venomous snakes. The second sentence is the most descriptive, but includes redundant information. Anyone familiar with groceries and the process of buying them can reasonably infer that they will be contained in bags. The third sentence tells us all we need to know in the most succinct manner.

The forth sentence takes a different approach entirely, labelling the singular activity that produced the groceries. But it doesn't tell us what kind of product we shopped for, so it’s not as descriptive. (Sometimes this approach *is* the best option as will be seen in other examples.)

If you look at the user's home folder on any new Windows PC or Mac, you'll find it pre-populated with folders like Documents, Downloads, and Pictures. A folder labelled 'Pictures' tells us all we need to know. You could choose to suffix all your directory names with 'dir', 'folder' or something similarly redundant, but it adds nothing meaningful. (I'm old enough to remember seeing Mac users of yesteryear add the 'ƒ' character—generated by pressing Option-F—to the end of folder names. Crazy times.)

Ah, but there are exceptions! On my Mac, Apple (in its infinite wisdom, of course) chose *singular* names for three subfolders: Desktop, Library and Public. The rationale, one suspects, is that no one knows what the Desktop contains—not even the user oftentimes! Similarly, the Public folder might contain anything. To get all scholarly, we would call it a *heterogeneous* collection. It’s like that big box of stuff you pull out at Christmas time, which contains a hotchpotch of stuff like tinsel, baubles, stockings, wrapping paper and fake snow—easier to just label it ‘Christmas’, according to its purpose and theme.

The Library folder is an interesting one—not so much because Apple didn't name it according to its contents, but because it gives us an interesting real-world example. Is the purpose of a library to hold other objects, or is it a functional object in its own right? I'd say it's somewhere in the middle. Let’s say we decide to label a real-world library based on contents. We could call it ‘Books’. (Most libraries contain more than books, but to keep it simple we'll imagine that our library only contains books.) A library could hang a big sign out front that just said 'Books'—but then you might assume the books were for sale, rather than free to borrow. You'd probably assume this because you live in a capitalist society where most big signs are trying to peddle something. So the question of semantics is also one of *context*.

There's one more question of context that you didn't supply in your question. Where are these directories stored? Are they on your personal computer, or are they on a web server? Why does it matter? Well, on your PC, you're probably viewing each folder in a GUI, where the label is attached to an individual icon. But if the directories are part of a website structure, it's more likely that users will only ever see the names as part of a file path (if they notice them at all). The question here is, do you care, and if so, do you want the file path to read like a sentence? This is best illustrated by an example:

```
http://acme.com/order/explosive/detonator/dx3000
```

While each category *could* be plural, the path reads more like an English sentence by using singular directory names. While this seems a bit forced perhaps, you do see this approach on some websites.

**TL;DR:** When the function or theme of a container is more descriptive than its contents, a singular label (e.g. Library, Desktop, Christmas) can work best. The more heterogeneous a collection, the more likely this approach will make sense. But in most cases, labelling the plural contents (e.g. Documents, Downloads, Pictures) of the collection is easier and more descriptive.

### Answer 3

If you look at a class as a substitute for a tag name (something you would do when using a `<div>` or a `<span>`, which have no semantic meaning), your class would have to describe the contents of the element.

But at the same time, the element it self *is* the content. If you look at a car you say 'this is a car', you don't say 'these are car parts'. Or, if you eat a cake you call it 'cake' and not 'ingredients'.

So I guess a semantic class name would be singular and not plural, because it is always only one element. This might result in using a lot of 'wrapper' in your class names, because finding a fitting name for your element is not always that easy.

I hope this answers your question, if not you might want to read this: [http://css-tricks.com/semantic-class-names/](http://css-tricks.com/semantic-class-names/)

### Answer 4

The convention proposed by user Mecki is coherent, but I wonder whether it is really useful in the context of file organization.

In my experience, a very useful convention is to see file path components as a collection of searchable **tags**. This aids in classifying and **finding** files, which, for me is the main purpose of establishing a convention for directory and file names.

For example, one file could be named `camera-MODEL-manual.pdf` (where MODEL is the concrete model). There could be also a directory that contains various manuals. Or perhaps there are multiple manuals for a particular device. In that case, they could be kept in `manual/DEVICE/...`. Naming directories that contain manuals with the tag "manual" in singular helps searches for manuals.

Within this convention, one can search for file paths containing "birthday" and "peter" without having to remember whether the directory is "2022-birthday-peter" or "birthday/peter/2022". Or one can search for all PDF files whose path contains "car" to find some car-related document.

While in English most plural forms are simply created by adding an "s" suffix, so that a search for "birthday" may bring up "birthdays", this is not true in many other languages. And even in English, it may be preferable to search for whole words, such that a search for "birth" does not bring up "brithday".

- [semantics](https://stackoverflow.com/questions/tagged/semantics "show questions tagged 'semantics'")

See similar questions with these tags.