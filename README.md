# ASR for Alakazam

A plugin for [Alakazam](https://github.com/markspan/Alakazam): Artifact Subspace Reconstruction, from EEGLAB's clean_rawdata plugin: channels that are flat or poorly predicted by their neighbours are interpolated, and bursts of artefact are repaired, or rejected, against a clean stretch of the recording itself.

It was part of Alakazam until it became a plugin of its own, so that it can be
installed, upgraded and documented on its own.

## Manual

The manual is on this repository's pages:
<https://markspan.github.io/AlakazamASR/>.

## Installing

In Alakazam, **Install plugins** on the Alakazam tab lists this repository:
select it and press **Install**. It installs the latest release. A zip from
the [releases](https://github.com/markspan/AlakazamASR/releases), or one built with
`build`, installs the same way through **From a link**, and so does the link
to this repository. The tool appears on the Tools tab, as it did before.

It needs an Alakazam that no longer carries `ASR` itself (newer than
V0.4.5.2). Workspaces and templates made with the built-in tool open and
recalculate as before once the plugin is installed; Alakazam offers to
install it when one needs it.

## Building and testing

```matlab
build()                                    % dist/ASR-<version>.zip
runtests('tests')                          % the tool's tests and the install
```

The tests need Alakazam's source: the folder in `ALAKAZAM_ROOT`, or the
Alakazam repository beside this one.

It runs EEGLAB's clean_rawdata plugin, which comes with EEGLAB. The tests need it, and skip without it.

## Licence

GPL-3.0, as Alakazam.
