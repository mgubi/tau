# Tau

<img src="https://raw.githubusercontent.com/mgubi/texmacs/wip_tau/src/misc/tau/web/icon-192.png" width="96" align="right" alt="">

**https://mgubi.github.io/tau/**

Tau is [GNU TeXmacs](https://www.texmacs.org) in the browser: the editor and
its Scheme run in a Web Worker, without widgets or windows, and the interface
(menus, icon bars, dialogs, tabs, panes) is HTML in the page. It is an
experiment, not a release of TeXmacs.

This repository only publishes the page. The sources are in the branch
[`wip_tau`](https://github.com/mgubi/texmacs/tree/wip_tau) of
`mgubi/texmacs` (see its README and `src/docs/tau-design.md`), and issues
belong there.

The page is built by `.github/workflows/pages.yml`, which checks out the
sources, builds them with Emscripten and deploys the result to GitHub Pages.
A push to the sources does not publish: start the workflow again with

    gh workflow run pages.yml -R mgubi/tau

(`-f ref=…` for another branch, tag or commit of the sources).

Documents are kept in the browser (IndexedDB), on the machine of the reader:
nothing is sent to a server.
