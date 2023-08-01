** Robotic Actuation Lab

1. revised ` {% if page.permalink != '/' -%}` to `{% if page.permalink != '/none' -%}` which blocked the site tile or the site logo for the about pages. 
1. Added slick for the slide image, I had to debug, the reason might be that the `link` is not at the `head`, I followed https://stackoverflow.com/questions/62099145/uncaught-typeerror-jquery-slick-is-not-a-function-in-wordpress-custom-temp
3. change the style of the publication and add teh video functions
4. for the news Entries in the 
