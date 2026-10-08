# Francio87 NS8 applications

This is a public NethServer 8 software catalog. It currently indexes the Borg Backup Server NS8 module.

## Add this repository to NethServer 8

In Cluster Admin, open Software Center → Software repositories → Add repository and use:

- Name: Francio87 NS8 apps
- URL: https://francio87.github.io/ns8-repomd/repodata.json

The catalog metadata is rebuilt four times a day and after changes to this repository. New module image tags are discovered from the public GHCR package.

## Testing releases

The catalog generator publishes the latest stable SemVer tag and the latest SemVer prerelease for each module. Borg Backup Server currently has testing tags and an older stable tag. A cluster must enable testing for this repository to treat prerelease versions as stable for installation and update calculations. Keep testing disabled on production clusters unless you intend to test prereleases.

## Add another module

Create a top-level directory named after the NS8 module ID and add its `metadata.json` and a 256×256 PNG logo. Any top-level directory containing `metadata.json` is indexed automatically after a push to `main`. The image source in `metadata.json` must refer to a public GHCR package with SemVer tags. Optional screenshots go in a `screenshots` directory as PNG files.

The catalog is generated with the NethServer createrepo.py script. Its upstream source and GPL license notice are preserved in the script.
