+++
date = "2016-04-25T14:51:00+00:00"
description = "Set default front matter for new pages and posts."
draft = false
tags = []
title = "Defaults Fields"

+++
Forestry will make UI fields out of the front matter of your posts, pages and collections/sections. 

You can set up  your site so Forestry will use default fields for new pages or posts. In the following example, we want all new pages to include a *Banner* image, a *Categories* field (array), and a *Description* field.

<img src="/docs/assets/images/forestry-default-fields.png">

## Jekyll Default Fields 
If you want these fields to show up in front matter (and forestry UI) for new posts, you can define them in your <code>_config.yml</code> file (see the <a href="https://jekyllrb.com/docs/configuration/#front-matter-defaults">Jekyll docs</a> for more info).

In the example below, all new posts (no matter what the path is) will get these fields.

<pre><code class="language-yml">
defaults:
  - scope:
      path: ""
      type: posts
    values:
        thumbnail: ''"
        categories: []
        description: ''"
</code>
</pre>

Be sure to include at least one page or post that uses an image file as a value for the *thumbnail* front matter.  This way, when Forestry parses your site, it will know to treat that field as an image upload field. 

## Hugo

Archetypes