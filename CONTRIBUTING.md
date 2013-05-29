Contributing
============

> How can I contribute to this project?

* Pull requests are always welcome
* Address issues wherever possible
* Prefix commit messages with [#XX] if addressing an existing issue number
* Use the present tense in commit messages
* Shorten commit messages to 50 characters with bulleted details

> In which format should my contributions be submitted?

* Pull requests should be in JSON format
* Resources should be of the format:

```
{
    "title": "Read Learn Objective-C on the Mac",
    "uri": "http://amzn.to/learn-objective-c-mac",
    "publisher": "http://www.apress.com/9781430218159",
    "ibook": "itms-books://itunes.apple.com/us/book/learn-objective-c-on-the-mac/id492011030?mt=11"
}
```

* Book resources only have to include a "publisher" link if the "uri" is an Amazon link.
* If the book is available in the iBookstore, you can include that link under "ibooks" and replace the "https" scheme with "itms-books".
* Validations should be of the format:

```
{
    "title": "Define a method."
},
{
    "title": "Invoke a method."
}
```

* A resource or validation's "id" will be automatically generated after you `rake` so you shouldn't include it yourself.

> How do I validate the trail JSON files after I've added to them?

* Run the tests, ID generator, and validator with `rake`
* For more detailed output, use [JSONlint.com](http://jsonlint.com).
* Considering using [this regex](https://gist.github.com/4068038) for converting Markdown to JSON

Merging Pull Requests (for admins)
----------------------------------

    git remote add username git://github.com/username/trail-map.git
    git fetch username
    git cherry-pick aabbcceeddffgg...(this is the SHA)

Then, edit the commit as necessary and then edit the commit message:

    git add -A
    git commit --amend -v

Reasoning [detailed by Linus](https://github.com/torvalds/linux/pull/17).
