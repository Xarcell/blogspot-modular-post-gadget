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

## INSTANCE SETTINGS & POSSIBLE VALUES ##
|SETTING|VALUE|DEFAULT|DESCRIPTION|
|-------|-------|-------|-------|
|:---|:----:|:----:|:---|
|className|string|default|The class name of the gadget so it can be styled by CSS.|
|showPosts|"asRandom", "asRandomByLabel", "asRecent", "asRecentByLabel"|asRecent|reserved|
|showOrderBy| “published”, “updated”|"published"|reserved|
|showStandardPostCount|integer|3|This is the number of posts to show.|
|showAdditionalPost| “asNone”, “asLoadMore”|asNone|reserved|
|showAdditionalPostCount|integer|3|This is the number of posts to show if more posts are loaded via Ajax.|
|showPostLabel|string|"test"|Shows posts that have a specific label(category or tag). This only works with `showPost` values: `asRandomByLabel` or `asRecentByLabel`.|
|showPostImage|boolean|true|This is self-explanatory.|
|showInPostImageSize|integer|320|This uses the first image found in a post. This only shows if `showPostImage` value is set to `true`.|
|showInPostYouTubeImageSize|"default", "mqdefault", "hqdefault", "maxresdefault"|"maxresdefault"|This is only for YouTube video thumbnail size. This only shows if `showPostImage` value is set to `true`.|
|showPostTitle|boolean|true|This is self-explanatory.|
|showPostTitleAmount|integer|180|The amount of characters to show for the post title. This only shows if `showPostTitle` value is set to `true`.|
|showPostAuthor|boolean|true|This is self-explanatory.|
|showPostCategory|boolean|true|Shows only first label(category or tag) alphabetically.|
|showPostDate|boolean|true|This is self-explanatory.|
|showPostContent|boolean|true|This is self-explanatory.|
|showPostContentAmount|integer|360|The amount of characters to show for the post content. This only shows if `showPostContent` value is set to `true`.|
|showPostContentTruncation|boolean|true|This adds an ellipsis(...) when the `showPostContentAmount` value is reached, or when a jump-link is detected in the post.|
|showPostTags|boolean|true|Shows a list of all labels(category or tags) used for the post.|
|showPostComments|boolean|true|This is self-explanatory.|
|showCategoryArchive|boolean|true|This shows a link to a list of posts by label equal to the `showPostLabel` value. This only shows if the `showPosts` value is equal to `asRandomByLabel` or `asRecentByLabel`.|

## EXAMPLE INSTANCE ##
The following below is an example of every setting with it's default value. Use only what you need in an instance, or settings that are different than default.

```
<script>
  // <![CDATA[
  myModule.addSection("THIS_INSTANCE_UNIQUE_NAME", { 
    className: "default",
    showPosts: "asRandom",
    showOrderBy: "published",
    showStandardPostCount: 3,
    showAdditionalPosts: "asLoadMore",
    showAdditionalPostCount: 3,
    showPostLabel: "test",
    showPostImage: true,
    showInPostImageSize: 320,
    showInPostYouTubeImageSize: "maxresdefault.jpg",
    showPostTitle: true,
    showPostTitleAmount: 180,
    showPostAuthor: true,
    showPostCategory: true,
    showPostDate: true,
    showPostContent: true,
    showPostContentAmount: 360,
    showPostContentTruncation: true,
    showPostTags: true,
    showPostCommentCount: true,
    showCategoryArchive: true,
  })
  myModule.run("THIS_INSTANCE_UNIQUE_NAME")
  // ]]>
</script>
```

### Changelog ###
Version 1.0
