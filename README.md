# Debugging in Drupal 8
Note:
- KG
- Hello Everyone! We are going to talk about "Debugging in D8"



## Slides
[bit.ly/pain-points-slides](http://bit.ly/pain-points-slides)

Note:
I have posted slides with speaker notes online and bit.ly
link for this session is. You can follow along the slides.




## Kalpana Goel

<a href="https://www.drupal.org/u/kgoel"><i class="fa fa-drupal"></i> kgoel</a>

<a href="https://twitter.com/kalpanagoel"><i class="fa fa-twitter"></i> kalpanagoel</a>

Note:
- KG
- Developer at Forum One
- Forum One is full service digital agency and does lot of work in Drupal for
Government and non-profit organizations.



<!-- .slide: data-background="custom/images/" data-background-size="" data-state="show-header" data-header="" -->



<!-- .element: class="heading" -->
<!-- .slide: data-background="custom/images/09September_1.jpg"  data-state="show-header" data-header="" -->
## First mention of bug and debugging
<!-- .element: class="heading" -->

Note:
- KG
- First reported bug in 1947
- Bug and debugging terms are attributed to Grace Hopper when she was working on computer at Harward University.
- Someone discovered moth stuck and stop the operation, she made a remark that they are debugging the system 
- and since then we are using that term.





## Debugging steps 
Note:
- Write tests so there are minimal chances of bug in your code
- if a bug does exist, reproduce a problem
- use debug in your code. In D7 - var_dump(), dpm
- find the source of the problem and fix it.





## Debugging in Drupal 8
Note:
- 





## <!-- .slide: data-background="custom/images/website_error.png" data-background-size="" data-state="show-header" data-header="" -->
Note:
- If you see this sort of error (in my case long back while installing standard installation)
- doesn't give much information about error




## www.drupal.org/node/2313059
Note:
- No error shown by default
- NR would be great




## $config['system.logging']['error_level'] = 'verbose';
Note:
- Add this in settings.php
- where?




## www.drupal.org/node/2320959
Note:
- Active/developer tricks/tools for D8




## Twig debugging 
Note:
- services.yml 
- if not cp sites/default/services.yml to services.yml



## parameters:
  twig.config:
    debug: true
Note:
- enable twig debugging



## Benefits of enabling debugging in Twig
Note:
- Default: false
- dump() output template variables
- template file name suggestions
- turn it off while running automated tests otherwise fail for tests checking rendered HTMl example?
- Turn off in production



## Twig auto-reload
Note:
- automatically recompile Twig templates if source code changes
- Turn off in production



## Twig cache
Note:
- 



## Drupal render cache
Note:
- Render caching enable by default to speed up page load



## Disable render cache
if (file_exists(__DIR__ . '/settings.local.php')) {
  include __DIR__ . '/settings.local.php';
}
Note:
- uncomment from settings.local.php
- drush cr




## $settings['cache']['bins']['render'] = 'cache.backend.null';
$settings['cache']['bins']['dynamic_page_cache'] = 'cache.backend.null';
Note:
- uncomment from settins.local.php
- drush cr
- explain why




##
Note:
- KG





## 
Note:
-




## 




## 
Note:





##
Note:





## 





##

Note:
-




##

<img src="custom/images/apache_contributors.png" />
Note:
-




##

<img src="custom/images/Apache_timeline.png" />
Note:






##

<img src="custom/images/long_tail.png" />

<small>photo credit: </small>
Note:





##
*
*
Note:
-



##




## Thank You!
## Don't forget to rate session


