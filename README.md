# OpenBikeSensor Website and Documentation 

You can find this site at [https://www.openbikesensor.org/](https://www.openbikesensor.org/).

## Contributing

Please phrase your contributions as pull requests to the `main` branch. Once you have passed the review
and your commit is merged they will be built by github pages and appear on https://test.openbikesensor.org.
After validating that everything renders OK on the test site, they are ready to be merged to the `production`
branch which in turn feeds the main site.

If you are new to git, GitHub, Hugo and the process of creating merge requests, there is
a (German language) help article for beginners over at the OpenBikeSensor Forums, which might help you get started:

https://forum.openbikesensor.org/t/mitwirken-an-der-website-dokumentation-so-gehts/115

## Development

Make sure to clone the repository with the `--recursive` flag, or if you forgot that, initialize submodules like this:

```bash
git submodule update --init --recursive
```

Install postcss and other postprocessing tools using npm:

```bash
npm install
```

To build the site for development, you can choose between docker and a locally installed version of hugo.

### Run hugo with docker

All you need to do is:

```bash
docker-compose up
```

* Wait a moment, until you see `Web Server is available at`
* Open http://localhost:1313

### Run hugo locally

Install [hugo](https://gohugo.io/) (extended version!) and then run:

```bash
hugo server -D
```

### Dependency versions

We try to keep up to date with hugo and docsy. The current docsy version is
referenced in the submodule, so we're not sticking to any releases there. The
current hugo version is specified in the [github flow
file](.github/workflows/gh-pages-staging.yml).

Since hugo does not introduce many breaking changes, it should be fine to work
with other versions locally. If you run into trouble, try to install the exact
version referenced in the github flow file, as that is used to build this site
for production. Always make sure to install hugo's *extended version*.

As for Node.js, we currently use version 12 for installing the dependencies
(postcss etc., see above). However, any newer version that is supported on your
operating system should work just as well, since we're not really using node
itself, just the package manager (npm).

If you want to update any of these components, feel free to do so and change
the places where it is referenced in the github flow or submodule, as well as
this documentation. It makes sense to stay up to date, but isn't really
required for a site of this size and scope. When updating, please create a
separate pull request to change the canonical version(s) in this repository.

## License
  
    Copyright (C) 2020-2021 OpenBikeSensor Contributors
    Contact: https://openbikesensor.org
    
    The OpenBikeSensor Website and Documentation is free software: you can
    redistribute it and/or modify it under the terms of the GNU Lesser General
    Public License as published by the Free Software Foundation, either version
    3 of the License, or (at your option) any later version.
    
    The OpenBikeSensor Website and Documentation is distributed in the hope
    that it will be useful, but WITHOUT ANY WARRANTY; without even the implied
    warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU Lesser General Public License for more details.
    
    You should have received a copy of the GNU Lesser General Public License
    along with the OpenBikeSensor Website and Documentation. If not, see
    <http://www.gnu.org/licenses/>.

See also [`COPYING`](./COPYING) and [`COPYING.LESSER`](./COPYING.LESSER).

Some content in this repository may be redistributed content and not subject to
the terms of this license. The license applies to all content generated by
OpenBikeSensor Contributors for and published as part of the OpenBikeSensor
Website.
