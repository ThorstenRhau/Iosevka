# Iosevka

I use this repository for my personal Iosevka configuration and documentation.

## Documentation

[Building Iosevka from Source - GitHub](https://github.com/be5invis/Iosevka/blob/main/doc/custom-build.md)
[Iosevka Customizer](https://typeof.net/Iosevka/customizer)

### Dependencies

Clone source repo

```sh
git clone --depth 1 https://github.com/be5invis/Iosevka.git
```

Install needed software (on Mac)

```sh
brew install node ttfautohint
```

### Build Iosevka

Go to the directory where the Iosevka source code directory and install _node_
dependencies.

```sh
cd Iosevka
npm install
```

Copy or link the **_private-build-plans.toml_** file to the git repo root
directory. When you have done that you can build the Iosevka font. Please note
that in the example below I use 6 build processes. These consume about 1GB or
RAM and 1 CPU core each.

```sh
npm run build -- ttf::IosevkaCustom --jCmd=6
```

The font files are now located in the _dist_ directory
