project_path: /web/_project.yaml
book_path: /web/updates/_book.yaml
description: A round up of the deprecations and removals in Chrome 58 to help you plan.

{# wf_updated_on: 2017-03-16 #}
{# wf_published_on: 2017-03-16 #}
{# wf_tags: deprecations,removals,chrome58 #}
{# wf_featured_image: /web/updates/images/generic/warning.png #}
{# wf_featured_snippet: A round up of the deprecations and removals in Chrome 58 to help you plan. #}

# Deprecations and Removals in Chrome 58 {: .page-title }

{% include "web/_shared/contributors/josephmedley.html" %}

In nearly every version of Chrome, we see a significant number of updates and
improvements to the product, its performance, and also capabilities of the Web
Platform. This article describes the deprecations and removals in Chrome 58,
which is in beta as of March 16. This list is subject to change at any time.

## Remove case-insensitive matching for usemap attribute

The `usemap` attribute was formerly defined as caseless. Unfortunately
implementing this was complicated enough that no browsers implemented it
correctly. Research suggested that such complicated algorithm is unnecessary,
and even ASCII case-insensitive matching is unnecessary. 

Consequently, the specification was updated so that case-sensitive matching is
applied. The old behavior was deprecated in Chrome 57, and is now removed.

[Intent to Remove](https://groups.google.com/a/chromium.org/d/topic/blink-dev/8pHdFzN0YQc/discussion) &#124;
[Chromestatus Tracker](https://www.chromestatus.com/feature/5760965337415680) &#124;
[Chromium Bug](https://bugs.chromium.org/p/chromium/issues/detail?id=659464)

## Remove legacy caller for HTMLEmbedElement and HTMLObjectElement

That an interface has a legacy caller means that an instance can be called as a
function. Currently, `HTMLEmbedElement` and `HTMLObjectElement` support this
functionality. In Chrome 57 this ability was deprecated. Calling now throws an exception.

This change brings Chrome in line with recent spec changes. The legacy behavior
is not supported in Edge or Safari, and it is being
[removed from Firefox](https://bugzilla.mozilla.org/show_bug.cgi?id=909656).

[Intent to Remove](https://groups.google.com/a/chromium.org/d/topic/blink-dev/AiDZ7ru9mGg/discussion) &#124;
[Chromestatus Tracker](https://www.chromestatus.com/feature/5715026367217664) &#124;
[Chromium Bug](https://bugs.chromium.org/p/chromium/issues/detail?id=663662)

<<../../_deprecation-policy.md>>

{% include "comment-widget.html" %}