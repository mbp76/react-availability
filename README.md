# react-availability

Availability search for the web in React.

## Installation

Start by downloading and building the project when necessary. The following
commands will do the job on most Debian based Linux distributions.

```bash
git clone https://github.com/marcbperez/react-availability
cd react-availability
sudo ./gradlew
```

## Usage

Run the following script to start a development server. After this the
application will be available at `http://127.0.0.1:3000`.

```bash
npm start
```

To get and run a production build use the script below. The contents will be
placed inside `build`. Tests can be executed via docker-compose (described in
the section below) or executed manually with NPM and Jest.

```bash
npm test
npm build
npm run build
```

## Testing

Test checks are executed automatically every time the project is built. Builds
can be done remotely or continuously on a development context. For continuous
integration and development use docker-compose. This is recommended to keep the
system clean while the project is built every time the sources change.

```bash
sudo docker-compose up
```

For continuous integration and development without any dependencies use the
Gradle wrapper. This is the best option if the wrapper is available and the
Docker context is not valid. For a full list of tasks, see
`sudo ./gradlew tasks --all`. For a CI cycle use `sudo ./gradlew --continuous`.

For continuous integration and development without Docker or the project wrapper
use Gradle directly. This will create the wrapper in case it is not present.
Similar to the above, for a CI cycle use `sudo gradle --continuous`. Gradle
3.4.1 is required for this to work. Plain Docker is also available for remote
integration tasks and alike. Build the image with `sudo docker build .` and run
a new container with it. Information on how to install Docker and docker-compose
can be found in their [official page][install-docker-compose]. A similar
installation guide is available [for Gradle][install-gradle].

## Troubleshooting

The [issue tracker][issue-tracker] intends to manage and compile bugs,
enhancements, proposals and tasks. Reading through its material or reporting to
its contributors via the platform is strongly recommended.

## Contributing

This project adheres to [Semantic Versioning][semver] and to certain syntax
conventions defined in [.editorconfig][editorconfig]. To get a list of changes
refer to the [CHANGELOG][changelog]. Only branches prefixed by *feature-*,
*hotfix-*, or *release-* will be considered:

  - Fork the project.
  - Create your new branch: `git checkout -b feature-my-feature develop`
  - Commit your changes: `git commit -am 'Added my new feature.'`
  - Push the branch: `git push origin feature-my-feature`
  - Submit a pull request.

## Credits

This project is created by [marcbperez][author] and maintained by its
[author][author] and contributors.

## License

This project is licensed under the [Apache License Version 2.0][license].

[author]: https://marcbperez.github.io
[issue-tracker]: https://github.com/marcbperez/react-availability/issues
[editorconfig]: .editorconfig
[changelog]: CHANGELOG.md
[license]: LICENSE
[semver]: http://semver.org
[install-docker-compose]: https://docs.docker.com/compose/install/
[install-gradle]: https://gradle.org/install
