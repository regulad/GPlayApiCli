# GPlayApiCli

GPlayApiCli is a command line interface to the Google Play API.

It uses [a JVM-compatible fork](https://github.com/regulad/GPlayApi) of the [AuroraOSS `gplayapi`](https://gitlab.com/AuroraOSS/gplayapi) library.

## Usage

`GPlayApiCli` exposes a CLI with a complete help output and documented options.

You can either download it from the nightly.link [here](https://nightly.link/regulad/GPlayApiCli/workflows/build/master/shadow-jar.zip) or use `./gradlew shadowJar` to compile it locally.

```bash
java -jar ./GPlayApiCli.jar --help
```

## Supported Commands

* [x] `download` - Download a free app from Google Play.
* [ ] `search` - Search for apps on Google Play.
* [ ] `trending` - Get the top apps on Google Play.
* [ ] `reviews` - Get the reviews for an app on Google Play.
* [ ] `appinfo` - Get the app info for an app on Google Play and place it in a machine-readable format.

## Examples

Example use-cases:
* Download a free app from Google Play for deployment on a device without GMS.
* Get the app info for an app on Google Play and place it in a machine-readable format for data analysis.
* Get files without a middleman like APKMirror for CI pipelines that need APKs for modding/LLM-assisted automated RE.

```bash
curl -L https://nightly.link/regulad/GPlayApiCli/workflows/build/master/shadow-jar.zip -o /tmp/download.zip
unzip /tmp/download.zip -d /tmp

java -jar /tmp/GPlayApiCli.jar download com.cpuid.cpu_z
java -jar /tmp/GPlayApiCli.jar download com.instagram.android
```

## License

`GPlayApi` is available under `GPL-3.0-or-later`.

`GPlayApiCli` is available under `AGPL-3.0-or-later`.
