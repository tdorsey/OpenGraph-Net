OpenGraph-Net
=============
[![AppVeyor](https://img.shields.io/appveyor/ci/GeoffHorsey/opengraph-net.svg)](https://ci.appveyor.com/project/GeoffHorsey/opengraph-net)
[![Nuget](https://img.shields.io/nuget/v/OpenGraph-Net.svg)](http://www.nuget.org/packages/OpenGraph-Net/)
[![License](https://img.shields.io/badge/license-MIT-orange.svg)](https://raw.githubusercontent.com/ghorsey/OpenGraph-Net/master/LICENSE)

A simple .net assembly to use to parse Open Graph information from either a URL or an HTML snippet. You can read more about the
Open Graph protocol @ http://ogp.me.

Usage
=====
Synchronously parse a url:

    OpenGraph graph = OpenGraph.ParseUrl("http://www.amazon.com/Spaced-Complete-Simon-Pegg/dp/B0019MFY3Q");

Use `async/await` to parse a url:

    OpenGraph graph = await OpenGraph.ParseUrlAsync("http://www.amazon.com/Spaced-Complete-Simon-Pegg/dp/B0019MFY3Q");

You can access each open graph value by passing in value key to the open graph dictionary.  For example:
`graph["Description"]` will return the description.

The four required Open Graph properties for all pages are available as direct properties on the OpenGraph object.

* graph.Type
* graph.Title
* graph.Image
* graph.Url

The original url used to generate the OpenGraph data is available from the `OriginalUrl` property
`graph.OriginalUrl`.
