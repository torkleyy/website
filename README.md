# Amethyst Website

[![Build Status][s1]][tc] [![Join us on Discord][s2]][di]

[s1]: https://travis-ci.org/amethyst/website.svg?branch=master
[s2]: https://img.shields.io/discord/425678876929163284.svg?logo=discord

[tc]: https://travis-ci.org/amethyst/website
[di]: https://discord.gg/amethyst

This is the source code for the Amethyst website and blog, accessible from
either https://amethyst.github.io/website/ or https://www.amethyst.rs/. The HTML
is generated by [Zola][za] and hosted online with [GitHub Pages][gp].

[za]: https://www.getzola.org/
[gp]: https://pages.github.com/

Any changes to the `master` branch of this repository should automatically
trigger a rebuild and republish of the site through [Travis CI][tc].

## Structure

| Content                     | Source Path               | Website Path |
| --------------------------- | ------------------------- | ------------ |
| Main Content                | `src/content`             | `/`          |
| News from Amethyst          | `src/content/blog`        | `/blog/`     |
| Amethyst Book               | [`amethyst/book/src`][bs] | `/book/`     |
| Generated API Documentation | [`amethyst/src/`][ds]     | `/doc/`      |

[bs]: https://github.com/amethyst/amethyst/tree/master/book/src
[ds]: https://github.com/amethyst/amethyst/tree/master/src

## Building Locally

To generate a complete local copy of the website with documentation, run:
```
$ ./generate.sh
```

Note that this is a long process.  If you are looking to get up and running quickly for development, first install [Zola](https://www.getzola.org/documentation/getting-started/installation/) and then run the following:


```
$ cd src && zola serve
```

This will generate temporary files in `src/public` as well as start a local server with live updates.  When the server is stopped, all generated files will be cleaned up and deleted.

Alternatively, you can run `./quick_build`.  This is similar to ```cd src && zola build```.  Note that this folder is in the project root under `build`, and will not automatically delete itself.  The homepage can be found at `public/index.html`.

## Contributing

We are a community project that welcomes contribution from anyone. If you're
interested in helping out, please read the [CONTRIBUTING.md][cm] file before
getting started. Don't know what to hack on? Feel free to search though
[our issue tracker][it].

[cm]: https://github.com/amethyst/amethyst/blob/master/CONTRIBUTING.md
[it]: https://github.com/amethyst/website/issues
