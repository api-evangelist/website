---
layout: post
title: "Version Control Your API Documentation with Github"
url: 'http://apievangelist.com/2012/10/24/version-control-your-api-documentation-with-github/'
image: 'http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/blog/github-logo-text-horizontal.png'
---

[<img class="c1" src="https://s3.amazonaws.com/kinlane-productions/api-evangelist/github/github-logo.png" alt="" width="200" align="right" />][1]

Out of date API documentation is by far the most common mistake API providers make, and also the [number one pain point for API developers][2]. It makes sense that you will want to keep your API documentation in sync with each version of your API, and one way to handle this is to version them both, using Github.

To use Github for your API documentation, all you need to do is create an single public repository, which you can use to manage HTML versions of your API docs. By putting your API documentation in its own repository you can keep the version of the API code repository in sync with it's corresponding documentation.

With the API documentation in Github, you can then easily publish to your API area or just allow developers to go directly to the Github repository and browse documentation there.

To help you edit your API documentation, you can use tools like [prose.io][3], which will allow even non-developers to assist in maintaining API documentation, with all changes stored neatly in a central Github repository.

Storing API docs in Github will also make them more portable. Some developers may wish to download a copy for offline work, or just prefer having locally for their own reference.

With the right approach to managing your API docs with Github, you can easily keep them up to date, in sync with your API, while also making them easily accessible by all API consumers--without much of the headache often associated with managing API documentation.

   [1]: https://github.com/ (Github)
   [2]: http://blog.programmableweb.com/2010/08/12/web-api-documentation-best-practices/
   [3]: http://prose.io/
