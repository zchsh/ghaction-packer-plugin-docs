# Overview

This action is meant to be run in Packer plugin repositories on releases.

This action takes a snapshot of documentation files so they can be rendered on the Packer website. This involves copying all `.mdx` files from any of the component directories within the docs directory - namely, `builders`, `datasources`, `post-processors`, and `provisioners`. Only directories with these names will be recognized as valid docs directories.

Snapshots of each component docs directory are copied into a `.generated` folder. This action also collects the `nav_title` from each `.mdx` file within the component docs directory, and generates a `nav-data.json` file, which is placed at the root level of the component docs directory. The folder structure of each directory is preserved.
