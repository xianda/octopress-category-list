Tag Cloud for Octopress
=======================

Description:
------------
Easy output tag cloud and category list.

Files:
------

    .
    ├─ plugins/
    │  └── category_list.rb
    └─ source/
       └─ _includes/
          └─ custom/
             └─ asides/
                ├─ category_list.html
                └─ category_cloud.html

Syntax:
-------

    {% category_cloud [counter:true] %}
    {% category_list [counter:true] %}
    {% top_category_list [counter:true] %}

Example:
--------

In some template files, you can add the following markups.

### source/_includes/custom/asides/category_cloud.html ###

    <section>
      <h1>Tag Cloud</h1>
        <span id="tag-cloud">{% category_cloud %}</span>
    </section>

### source/_includes/custom/asides/category_list.html ###

    <section>
      <h1>Categories</h1>
        <ul id="category-list">{% category_list counter:true %}</ul>
    </section>

### source/_includes/custom/asides/top_category_list.html ###

    <section>
      <h1>Top Categories</h1>
        <ul id="top-category-list">{% top_category_list counter:true %}</ul>
    </section>

This will list your categories by the number of posts in descending order. The default number of categories listed in the top category list is 10. Change this by setting "top_category_limit: <num>" in _config.yml.

alswl 的改进
---------

支持 utf-8，使用 `category_cloud` 替换 `tag_cloud` ，
以避免和 [真正的标签云](https://github.com/robbyedwards/octopress-tag-cloud) 冲突。

Notes:
------
Be sure to insert above template files into `default_asides` array in `_config.yml`.
And also you can define styles for 'tag-cloud', 'category-list', or 'top-category-list' in a `.scss` file.
(ex: `sass/custom/_styles.scss`)

Licence:
--------
Distributed under the [MIT License][MIT].

[MIT]: http://www.opensource.org/licenses/mit-license.php
