## Landscape theme for Ghost

Landscape for Ghost is based on our Landscape WordPress theme by BlankThemes.com: http://wordpress.org/themes/landscape

## Copyright & License

Original Designed and development by BlankThemes.com.
Copyright (c) 2014 BlankThemes.com - Released under the GPL License.

This is now continued by me, Bart Willems, also released under GPL.

Header image by Ansel Adams and is licensed under the Public Domain:
http://commons.wikimedia.org/wiki/File:Adams_The_Tetons_and_the_Snake_River.jpg


## How to install Landscape

Ghost themes live in `content/themes/`
After you have downloaded Landscape, extract it and place it in content/themes alongside the Casper default theme.

To switch to your newly added theme:

 * Restart Ghost. At the moment, Ghost won't notice that you've added a new folder to content/themes so you'll need to restart it

 * Login to your Ghost admin, and navigate to `/ghost/settings/general/`

 * Select your Theme name in the 'Theme' options dropdown

 * Click 'Save'

 * Visit the frontend of your blog and marvel at the new theme

If you are new to using Ghost, we recommend checking out the following:
 * Ghost Guide: http://docs.ghost.org/
 * Switching Themes: http://docs.ghost.org/themes/
 * Publishing with Ghost: http://docs.ghost.org/usage/writing/

## Editing the Main Menu

If you are using Landscape for your personal blog, you should use tags for pages in stead of the normal navigation.

``` html
<header class="site-head"> 
    <nav role="navigation">
        <ul>
            <li>
                {{#if @blog.logo}}
                <img src="{{@blog.logo}}" class="logo-nav" alt="Blog Logo"/>
                {{/if}}
                <a href="{{@blog.url}}">Fox<span class="ampersant">&nbsp;&amp;&nbsp;</span>Raven</a>
            </li>
            {{#get "tags" limit="all"}}
            {{#foreach tags}}
            <li>
                <a href="{{url}}" title="{{name}}">{{name}}</a>
            </li>
            {{/foreach}}
            {{/get}}
            <li>
                <a href="/contact">Contact</a>
            </li>
        </ul>
    </nav>
</header>
```