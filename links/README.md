# Short links for URLs in the book

## The problem: link rot

_Fluent Python, Second Edition_ has more than 1000 links to external resources.
Inevitably, some of those links will rot as time passes.
But I can't change the URLs in the print book!

## The solution: indirection

I replaced almost all URLs in the book with shortened versions that go through the `fpy.li` site which I control.
The site has an `.htaccess` file with *temporary* redirects.

When I find out a link is stale, I can thange the redirect in `.htaccess` to a new target,
so the link in the book is back in service via the updated redirect.

## Help wanted

Please report broken links as bugs in the [`FPY.LI.htaccess`](FPY.LI.htaccess) file.
Also, feel free to send pull requests with fixes to that file.
When I accept a PR, I will redeploy it to `fpy.li/.htaccess`.

## Details

Almost all URLs in the book are replaced with shortened versions like
[`http://fpy.li/1-3`](http://fpy.li/1-3)—for chapter 1, link #3.

There are also custom short URLs like
[`https://fpy.li/code`](https://fpy.li/code) which redirects to the example code repository.
I used custom short URLs for URLs with 3 or more mentions, or links to PEPs.

Exceptions:

- URLs with `oreilly` in them are unchanged;
- `fluentpython.com` URL (with no path) is unchanged;

The `FPY.LI.htaccess` is deployed at the root folder in `http://fpy.li`.