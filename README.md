# snap-roo
Installing the Roo programming language on Linux as a Snap.

## Steps for each new Roo build
1. Compress the files and `packages` folder created by the Xojo build process into a `.zip` file and rename to `roo-X.X.X-linux64.zip` (where `X.X.X` is the version number). Make sure the version number is bigger than the previous one for Homebrew and Scoop to work correctly.
2. Draft a new release for Roo and upload the Windows, Linux and macOS files. Copy the URL for the Linux download
3. Update the `version` key to the new version number
4. Set the `parts:roo:source` key in `snapcraft.yaml` to the Linux zip URL
5. Commit and push the changes in the YAML file to GitHub.
6. In Linux, `cd` to the directory containing the `snap` folder which contains the `snapcraft.yaml` file (on my VM that's `cd '/media/psf/Home/Repos/snap-roo' 
`)
7. Type `snapcraft`
8. Type `snapcraft push NAME_OF_DOT_SNAP_FILE_CREATED --release=stable`
