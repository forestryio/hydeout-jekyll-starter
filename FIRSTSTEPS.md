# Hyde / Hydeout

Hydeout updates the original [Hyde](https://github.com/poole/hyde)
theme for [Jekyll](http://jekyllrb.com) 3.x and adds new functionality.

![Desktop](https://github.com/fongandrew/hydeout/blob/master/_screenshots/1.png?raw=true)

### Keep It Simple

In keeping with the original Hyde theme, Hydeout aims to keep the overall
design lightweight and plugin-free. JavaScript is currently limited only
to Disqus and Google Analytics (and is only loaded if you provide configuration
variables).

Hydeout makes heavy use of Flexbox in its CSS. If Flexbox is not available,
the CSS degrades into a single column layout.

## First Steps

### 1. Deployment

Currently your site is only visible to you but there's a few options to quickly make your site available to the world.

The easiest option in our opinion is Netlify. It's quick to setup and relatively easy to maintain.

1. Go to <a href="https://app.netlify.com/start" target="_blank">https://app.netlify.com/start</a>
2. Connect your Git provider and provide Netlify access to your repository (e.g. username/hydeout)
3. Select and Click on your repository
4. Enter your build settings.
   * Build Command: `bundle exec jekyll build`
   * Publish Directory: `_site`
5. Click on `Deploy Site`

![](https://forestry.io/img/theme/netlify-step-4.gif)

6. Lastly copy your URL (e.g. https://something-something-123456.netlify.com/) and add it as your URL in your [`Site Configuration`](#/pages/config-toml).

The more powerful option is deployment to AWS and makes sense if you have experience with S3 and Cloudformation. You can find detailed documentation and a deployment template [here](https://forestry.io/docs/hosting/s3-cloudfront-stack/).

For other deployment options please check out our list [here](https://forestry.io/docs/hosting/) (including Webhooks, FTP/SFTP and Github Pages).

### 2. Advanced Settings

#### Theme

Theme colors can be configured in [Site Configuration](#/pages/_config-yml) under `Theme Colors`. Choose the Sidebar Background and Foreground color as well as the Link color.

See the [variables](https://github.com/fongandrew/hydeout/blob/master/_sass/hydeout/_variables.scss) file for other variables you can override.

#### Replace Favicon

You can replace the favicon (the small icon that shows up in the tab of your page in a browser) by going to the [Media Library](#/media/) and removing `favicon.png` and `favicon.ico` and replacing them with your own version. 

#### Reverse layout

![Hydeout with reverse layout](https://f.cloud.github.com/assets/98681/1831230/42b0d3ac-7384-11e3-8d54-2065afd03f9e.png)

To reverse page orientation activate `Reverse Layout` in `Site Configuration`.

#### Commentary with Disqus

You can optionally enable a comment system powered by Disqus for your posts. Simply add your Disqus Shortname in `Site Configuration` -> `Additional Settings` -> `Disqus Shortname`.

If you don't have a Disqus Account you can sign up for an account [here](https://disqus.com/).

#### Google Analytics

Google Analytics can be enabled by assigning your tracking code to `Site Configuration` -> `Additional Settings` -> `Google Analytics Tracking Code`.

If you don't have a Google Analytics Account you can sign up for an account [here](https://marketingplatform.google.com/about/analytics/).

### 3. Editing in Forestry

Your site is completely editable in Forestry. The Hydeout theme is a simple responsive blog completely based on posts and a sidebar menu.

#### Creating and Editing A New Page/Post

Pages and Posts are separated into two different categories.

To create a new page or post click on *Create New* and select *Post* (or *Page* depending what section you are in). Enter a title and click *Create* to proceed to the editor. 

![](https://forestry.io/img/theme/create-new.png)

On the left side you'll find general settings (e.g. title, subtitle, date etc.) and on the other side you have access to the Forestry Editor. The toolbar at the bottom of the editor will help you format and more easily navigate the editor.

![](https://forestry.io/img/theme/toolbar.png)

#### Add and Edit the Sidebar

To add new links and edit existing ones navigate to [Pages](#/menus/main), select a page and activate `Sidebar Link`. 

You are also able to reorder links by setting the `Sidebar Sort Order` value with a position number (1 is the highest position). The position is set in relation to the other pages (e.g. 1 is above 10 is above 35).

#### Create Categories

Categories are the only pages that automatically show in your Sidebar. To add a new category navigate to [Categories](#/sections/categories/) and click on `Add New` -> `New Page`. By default the title will be used as the Category but you can also define a different category name. The content of the page will be shown above the posts that are assigned this category. You can assign a post a specific category by adding it in the post's `categories` field.

#### Special Pages (Tags & Search)

In the [Pages](#/sections/pages/) section you can add a Tags page and a Search page. These will show up as icons in the bottom of your Sidebar by default. If you have no need for them you can simply remove these and the icons will be removed from your Sidebar as well.

If you have accidentally removed them you can always add them back in by creating a new page in [Pages](#/sections/pages/) and selecting the appropriate Template.

#### Preview

You can preview any post or page to see what it looks like before you publish your changes. Simply click on <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"><g fill="none" fill-rule="evenodd" stroke="currentcolor" stroke-width="1.2"><path d="M12 18c6 0 10-6 10-6s-4-6-10-6-10 6-10 6 4 6 10 6z"></path><circle cx="12" cy="12" r="2"></circle></g></svg> in the top-right corner of your editor.

#### Publish

All new posts/pages start out as draft. To publish a post/page you'll have to turn **Draft** to **OFF** and click on **Save**. If you've set up the site as outlined in the **Deployment** section, Forestry will no build your site and your hosting provider (Netlify, AWS, etc.) is going to update your website shortly.

![](https://forestry.io/img/theme/publish.png)

*More Information on Editing with Forestry [here](https://forestry.io/docs/editing/markdown-editor/)*  
*The full documentation for Developers using Forestry can be found [here](https://forestry.io/docs/)*

***

### Author

**Mark Otto**

* [https://github.com/mdo](https://github.com/mdo "https://github.com/mdo")
* [https://twitter.com/mdo](https://twitter.com/mdo "https://twitter.com/mdo")

**Andrew Fong**

* [https://github.com/fongandrew](https://github.com/fongandrew "https://github.com/fongandrew")
* [https://twitter.com/fongandrewc](https://twitter.com/fongandrewc "https://twitter.com/fongandrewc")

### License

Open sourced under the [MIT license](LICENSE.md).

<3
