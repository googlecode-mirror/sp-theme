# Introduction #

[Revision 7f73d6e306](http://code.google.com/p/sp-theme/source/detail?r=7f73d6e306276caa4e768c1bec11b3c32fec4e45) removed the built-in page navigation menu and the direct check for a plugin, in favor of the _blocks_ feature supported in the user-configurable [Page Menu plugin](https://trac.habariproject.org/habari-extras/browser/plugins/pagemenu). Support for the _areas_ into which _blocks_ display content was added to sp in [revision 87e92d3531](http://code.google.com/p/sp-theme/source/detail?r=87e92d3531ec3f69c530e9e128fdf9f27d4fc4ae).


# Details #

Install, activate, and configure the **Page Menu** plugin. Use the **Areas** section in **admin**->**Themes** to add a new **Block** named _Pages_, then drag it to the sidebar area and **Save** your changes.

Create a file in your sp theme directory named `block.pagemenu.php`, with the following contents:

```
<h3><?php echo $content->title; ?></h3>
<ul id="pagelist">
<?php foreach($content->menupages as $page) : ?>
<li class="<?php echo $page->activeclass; ?> block-<?php echo Utils::slugify($content->title); ?>">
<a href="<?php echo $page->permalink; ?>"><?php echo $page->title; ?></a>
</li>
<?php endforeach; ?>
</ul>
```