# Uni Web Topics Notes

Notes for the Spezielle Themen für Web-Anwendungen (special topics for web applications) course at HdM Stuttgart.

[![hydrun CI](https://github.com/pojntfx/uni-webtopics-notes/actions/workflows/hydrun.yaml/badge.svg)](https://github.com/pojntfx/uni-webtopics-notes/actions/workflows/hydrun.yaml)

## Overview

You can [view the notes on GitHub pages](https://pojntfx.github.io/uni-webtopics-notes/) or [download them from GitHub releases](https://github.com/pojntfx/uni-webtopics-notes/releases/latest).

## Contributing

To contribute, please use the [GitHub flow](https://guides.github.com/introduction/flow/) and follow our [Code of Conduct](./CODE_OF_CONDUCT.md).

To build and open a note locally, run the following:

```shell
$ git clone https://github.com/pojntfx/uni-webtopics-notes.git
$ cd uni-webtopics-notes
$ make depend
$ make dev-pdf/your-note # Use Bash completion to list available targets.
# In another terminal
$ make open-pdf/your-note # Use Bash completion to list available targets.
```

The note should now be opened. Whenever you change a source file, it will automatically be re-compiled.

## License

Uni Web Topics Notes (c) 2021 Felicitas Pojtinger and contributors

SPDX-License-Identifier: AGPL-3.0
