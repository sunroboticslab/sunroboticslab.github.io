** Robotic Actuation Lab

1. revised ` {% if page.permalink != '/' -%}` to `{% if page.permalink != '/none' -%}` which blocked the site tile or the site logo for the about pages. 
1. Added slick for the slide image, I had to debug, the reason might be that the `link` is not at the `head`, I followed https://stackoverflow.com/questions/62099145/uncaught-typeerror-jquery-slick-is-not-a-function-in-wordpress-custom-temp
3. change the style of the publication and add teh video functions
4. for the news Entries in the 
5. Added CNMAE file. 
6. This site only works with v0.9. I have downloaded the specific docker image. 
7. Revised people card width in line 483.  .grid-sizer, .grid-item { width: 220px;
8. Somehow the auto generation is down. Solution: I added --force_polling to the `docker-compose.yml` and it fixed this problem. 
9. revise docker-compose.yml, add `v0.9.0`
10. How to run this website. clone this website, then `run docker compose up`
11. I previously ignored `Gemfile.lock` in the `.gitignore`. It recently starts to cause problem. I now added this back. 
