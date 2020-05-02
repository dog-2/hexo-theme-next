定制Hexo Next主题的vendors，加入darkmode.js。[中文说明]()。

Customize vendors of the [Hexo]() Theme [Next](), add [darkmode.js]() into it.

Steps:

- modify .gitignore and add a line as below:
  ```
  !source/lib/darkmode-js
  ```
- add darkmode.js to submodule as your Next repository `{blog_dir}/themes/next/`
  ```bash
  git submodule add https://github.com/sandoche/Darkmode.js.git source/lib/darkmode-js/
  ```
- modify the config file as follows according to your preference (see code [here]())
  - {blog_dir}/themes/next/languages/en.yml
  - next config file, which may have two different types according to [the official doc](https://theme-next.org/docs/getting-started/configuration)
- add darkmode.js into vendors and customize it (see code [here]())
  - add code to {blog_dir}/themes/next/layout/_scripts/vendors.swig
  - add & set options below into next config file
    - make sure the default option `darkmode` is set to `false`
    - add `darkmode-js` option
    - add `darkmode-js` CDN specify option into `vendors`
