# What this revival changed

`prakhar1989/awesome-courses` has not taken a commit since November 2022. This
fork carries the maintenance and runs the gate from
<https://github.com/olitreadwell/awesome-list-template>.

The list is a snapshot of university course pages from 2014 to 2016, and most of
those pages have moved or gone. The gate is green because every remaining
plain-http URL is recorded in `links.allowlist`; `make links` is where the rot
shows, and it reports 645 dead links out of 1216.

## The readme

- The awesome badge pointed at `cdn.rawgit.com`, a dead CDN.
- A second table of contents sat under `Introduction`, and both `Introduction`
  and `Courses` were setext headings. The second list is gone and the headings
  are ATX.
- Ten dotted rules (`-------`) are three dashes, and sixteen list items had two
  spaces after the marker.
- The Legend showed the icon before its label, and a list item whose first child
  is HTML has no link, so the label leads now.
- `## Introduction` was listed as a section that holds entries. It is prose, so
  it is out of `awesome.toml`.

## Entries

- Ninety-two links repeated a URL that the list already carries, mostly a
  course's own page listed again as "Syllabus", "Lectures", or "Assignments",
  and three more differed only by a trailing slash or `index.php`. The labels
  stay and the markup went, so each URL appears once.
- Two hundred and thirty-three entries ran the description into the link or
  ended without a period. Each took the same mechanical repair: insert ` - `,
  capitalise the first word, end with a period. No word was added, removed, or
  reordered. Where the line ends in the icon images, the period sits before the
  first one, because the reader sees text there.
- The Statistics section hung its description and links at section level instead
  of under the course, and one paragraph about the RPISEC course had drifted
  under a different course. Both are back where they belong.
- Four `indiana.edu` links moved from http to https. The other 136 plain-http
  URLs are in `links.allowlist`: some answer on http only, and most are gone.
  A maintainer should repoint or drop those rather than leave the allowlist this
  long.

Left alone:

- No description was written. Where upstream had no words, there are still no
  words.
- Fourteen spell-check warnings stay, along with the list's own typos in prose.
- The repository has no licence. The linter reports that, and choosing one is
  the maintainer's call, so nothing was added.

## Tooling

The fork runs the same gate the engine ships, pinned to engine revision
`311c719`. `make check` covers the list rules, the Contents block, the GitHub
stars and activity snapshot, the exports, and the tests in
`tests/test_readme.py`.
