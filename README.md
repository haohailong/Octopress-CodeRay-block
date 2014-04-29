# Octopress CodeRay Block

- Author: Hailong Hao (http://shengmingzhiqing.com/) based on the work of Jan Stevens (http://fritz-hut.com), Kat Hagan (http://codebykat.com), and Brandon Mathis. 

- Description: Modified version of Jan Steven and Kat Hagan's code_block.rb that uses CodeRay for syntax highlighting. The Original Version by K. Hagan has the Github style caption, but cannot add line nubmers, the 2nd Version by J. Steven has line number option, but with a new style which looks conflict to the Octopress classic theme. If you use J. Steven's version with original CSS/SASS, the capiton style cannot be displayed well. This plugin fixed the problem.

## Installing the Plugin

### 1. Install kramdown, CodeRay and The Plugin
First of all we need to install the kramdown and coderay gems in our octopress blog.

You can add the following two lines of code to the **Gemfile** in Octopress root folder.
    
    gem 'kramdown'
    gem 'coderay'

Then execute this command in Terminal:

	bundle install

Next we adapt our **_config.yml** file so we can enable our newly installed gems.

    markdown: kramdown
    kramdown:
        use_coderay: true
        coderay:
            coderay_line_numbers: table
            coderay_css: class

If you want to enable **coderay_line_numbers** then leave it on table. If not then change it to nil.

### 2. Add style sheet.

Copy the file ```/sass/custom/_coderay.scss``` to your own ```/sass/custom/``` folder.

**Add the code** in ```/sass/custom/_styles.scss``` to your own ``` /sass/custom/_styles.scss``` file.

Done.

## How to use the plugin

This plugin is easy to use. The syntax is as followed, by default line numbers are not shown, which defined by the option ```linenos:```.

    {% coderay lang:ruby %}
    { % coderay [lang:lang] [linenos:true|false(default)] [title] [url] [link text] % }
    code snippet
    { % endcoderay % }
    {% endcoderay %}
    
As you noticed, it is simliar with the syntax of **codeblock** plugin, but with a more beautiful style (in my opinion ^_^) like:

- without line numbers or caption:

![CodeRay without linenos or caption](http://s.olo.la/ZOiz+)

- with line numbers:

![CodeRay with linenos](http://s.olo.la/BmiH+)

- with caption:

![CodeRay with caption](http://s.olo.la/FmCZ+)


## More
For more information visit my blog at [生命之氢](http://shengmingzhiqing.com), or Contact me via email: haohailong@gmail.com

