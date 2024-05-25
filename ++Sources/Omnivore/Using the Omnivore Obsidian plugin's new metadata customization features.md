---
id: 8d8cd528-b51f-486a-9520-356c18b13cf4
date: 2024-05-25 16:57:03
---

### Learn how to customize the front matter when importing your reading from Omnivore to Obsidian

One of the important features of the [Omnivore Obsidian plug-in](https://github.com/omnivore-app/obsidian-omnivore) is the ability to customize your imported data with templates. Using templates you can customize the layout of the imported article data and highlights. You can read more about [customizing the data imported into Obsidian here](https://docs.omnivore.app/integrations/obsidian.html#controlling-the-layout-of-the-data-imported-to-obsidian).

==With our latest release== (1.4.0) we’ve added new ways of customizing your [metadata](https://help.obsidian.md/Editing+and+formatting/Metadata) with Front Matter Settings. 

Our philosophy is to always give users as much control of their data as possible, but start with sensible defaults and tools for users that want things to just work.

But remember, with great flexibility…

[![](https://proxy-prod.omnivore-image-cache.app/340x0,syyjXW72lVJ3DvPA_UoMAbiYNuCWToCx9MF3UjGnZtJk/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F594dc10b-831f-4051-a5bf-6231df2eeb25_974x1324.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F594dc10b-831f-4051-a5bf-6231df2eeb25%5F974x1324.png)

==With the new front matter tools there are now three levels of customization you can choose from:==

1. List the values you’d like imported
2. Use aliases in the front matter list
3. Create a custom front matter template

## ==List the front matter values you’d like imported==

In the Omnivore plugin settings you can list the metadata items you’d like imported into Obsidian. The defaults will import items like title, author, and tags. If you’d like to add or remove some of the default items you can see the [available list of items in our docs](https://docs.omnivore.app/integrations/obsidian.html#variables-available-in-the-template).

[![](https://proxy-prod.omnivore-image-cache.app/554x0,sjrWJ3LDz_jkJ-Ou0z7FW6b8YH5WPrQFuphAd69StzQ4/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6befdf05-4f29-4677-a87f-42338d5f1674_1190x426.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F6befdf05-4f29-4677-a87f-42338d5f1674%5F1190x426.png)

Some of these values will not always be available: for example tags are only available if you have set labels on the item in Omnivore. If not set, these values will not be added. 

These values will be set in the front matter of your markdown files, so you will see them at the top of a page, like this:

[![](https://proxy-prod.omnivore-image-cache.app/552x0,sIPQYsyFAKwwrBn5tpHijsgxSXu7T5bLUGqDlXSfC6a0/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bc86ad2-6447-493c-af32-9e11f9026260_1306x590.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F5bc86ad2-6447-493c-af32-9e11f9026260%5F1306x590.png)

note: Omnivore adds the id value for internal usage.

## Use aliases in the front matter list

If you’d like to rename a value you can use aliasing in the front matter settings. For example, to change “date\_saved” to “date saved” you could alias the value like this: “date\_saved::date saved”

[![](https://proxy-prod.omnivore-image-cache.app/626x0,sKPxJWAy_oUtyk55XKkVL00hHHHXMmvcPknH0As24tTY/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4f87d63-eaa9-4734-9ed5-22df958bf4f7_1172x416.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Ff4f87d63-eaa9-4734-9ed5-22df958bf4f7%5F1172x416.png)

## Create a custom front matter template

If you need to further customize your metadata you can go into the Omnivore Advanced Settings in Obsidian and create a custom template. (See example below).

Note: When creating a custom template, it is important to render valid [YAML](https://yaml.org/). It is very easy to create invalid YAML with templates and imported data. Omnivore will validate the rendered data, and if it is invalid data it will create front matter with an   
”omnivore\_error” element. For example, the template listed below will create an error if the title has a “ symbol in it. 

This template:

[![](https://proxy-prod.omnivore-image-cache.app/626x0,sLH2LLL6ZhZTkCxP5IYyXmDigVPa5f08dxExEGCFMlm8/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6c52a6e-1efb-406c-ac89-972e13321eaa_1158x454.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb6c52a6e-1efb-406c-ac89-972e13321eaa%5F1158x454.png)

Created the following metadata:

[![](https://proxy-prod.omnivore-image-cache.app/616x0,sPmEpcT-T5w0Pe8dS-0O1H84Vyb1o4lF8IQWcLpPElww/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2be547c4-d70f-4204-8718-dfc5205bb945_1180x314.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F2be547c4-d70f-4204-8718-dfc5205bb945%5F1180x314.png)

To avoid escaping errors in templates, its recommended to use YAML multiline strings, for example:

[![](https://proxy-prod.omnivore-image-cache.app/606x0,sb3YayG3t__EyghC5np0m9B-TBs_7u2cfdTVwSYSJ3wE/https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd78cd76-ce21-4e2a-9e6b-a02706855808_1182x426.png)](https://substackcdn.com/image/fetch/f%5Fauto,q%5Fauto:good,fl%5Fprogressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fbd78cd76-ce21-4e2a-9e6b-a02706855808%5F1182x426.png)

## Feedback Appreciated

We made these metadata changes based on community feedback. If there is a way we can make the Omnivore Obsidian plugin work better for you and your desired workflow, please [join our discord and let us know](https://discord.gg/h2z5rppzz9), or [file a GitHub issue](https://github.com/omnivore-app/obsidian-omnivore/issues).


---
[Read on Omnivore](https://omnivore.app/me/using-the-omnivore-obsidian-plugin-s-new-metadata-customization--18fb0415858)
[Read Original](https://blog.omnivore.app/p/customize-omnivore-obsidian-metadata)
---