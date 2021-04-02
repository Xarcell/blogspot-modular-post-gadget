## SUMMARY ##

This script is used to show recent or random posts from your Blogspot site, in a specific manner or way, on your Blogspot site. It is modular in design, meaning you can have multiple instances of the script running, without reposting the whole script over and over again. 

## INSTALLATION ##

Installation is not hard and can be completed in three simple steps. Be sure to backup a copy of your template just in case you mess up or there is some kind of a script incompatibility.

1. Add the CSS code. There are two methods, choose one:

   - Method One: Go to your “Blogger > Admin > Theme > Customize > Advanced”. Select “Body” from the non-obvious dropdown selection and change it to “ Add CSS”. Then simply copy & paste the contents of the file “modular-posts-gadget-css.min.md” into the textarea and save. **NOTE:** This step may, or may not, need to be repeated if you update your template, depending on how you update your template.

   - Method Two: In your Blogger/Blogspot template, simply copy & paste the contents of the file "modular-posts-gadget-css.min.md" just above the closing `]]> </b:skin>` tag. **NOTE:** There may more than one of these tags, be sure to choose the one that has the bulk of CSS that applies to your whole site. Also, this step may, or may not, need to be repeated if you update your template, depending on how you update your template.

2. In your Blogger/Blogspot template, simply copy & paste the contents of the "modular-posts-gadget-core.min.md" just below the opening `<body>` tag. **NOTE:** This step may, or may not, need to be repeated if you update your template, depending on how you update your template.


3. To call an instance of the script, simply copy & paste the contents of the "modular-posts-gadget-instance.md" in a HTML Gadget via your Blogger/Blogspot admin. Be sure to rename the “THIS_INSTANCE_UNIQUE_NAME” to something not used elsewhere. You can add any many instances of the script as you want as long as they have a unique name.

## NOTES ##
This project came into fruition because of the lack of up-to-date and efficient recent/random post gadget, that I needed for my templates. I started the script with alot of jQuery, but then started hiring two other people on Fiverr to take over because of my limited Javascript knowledge. After about a year and alot of money, this script has been updated to be 100% vanilla Javascript and as efficient as possible. I decided to release this script publicly because I did not want it to become lost as so many other Blogger/Blogspot scripts have become.

If you are a theme developer, it should be obvious that you can just bake the instances anywhere into your template. It is important that you realize that the "core" MUST come before ANY "instance" calls.

I designed this script to work with my templates that “I” design. If you don’t like it, keep it to yourself. Anyway, as a result: 

* The images in this script are loaded as background images. This allows overall better control of fluid/responsive design. Without the proper CSS, they will not show.

* The additional text in this script like: "Author:", "Date:", any button text, etc…, to be handled via CSS(as a pseudo element). This is done for better localization control or if you want to use font icons instead.

* More CSS is coming for changing layout, if people actually care about using this script. I have other projects that I work on and don’t want to waste my time further building a script that no one uses.

* This is my first Github project, so please bare with me.

## SETTINGS & VALUES ##
Setting|value|Note
-------|-------
className|"default"|
showStandardPostCount|3|
showAdditionalPostCount|3|
showPostLabel|"test"|
showPostContentAmount|800|
showPostTitle|true|
showPostTitleAmount|80|
showInPostImageSize|320|
showInPostYouTubeImageSize|"maxresdefault.jpg", "default", "mqdefault", "hqdefault", "maxresdefault.jpg"|only for YouTube Video Thumbnail
showPostComments|true|
showPostDate|true|
showPostAuthor|true|
showPostImage|true|
showPostCategory|true|
showPostTags|true|
showPostContent|true|
showCategoryArchive|true|
showPostContentTruncation|true|adds a ellipsis(...) when showPostContentAmount value is reached, or when a jump-link is detected in the post
postContentTruncationHTML|'Read More'|
showPosts|"asRandom", "asRandom", "asRandomByLabel", "asRecent", "asRecentByLabel"|
