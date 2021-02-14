# Nextrip :airplane:
A place to put down some travel ideas :notebook::man_pilot:

## Getting Started
### Install Hugo
Nextrip is built using [Hugo](https://gohugo.io). They do the installation process far more justice than I can in one Readme... I suggest following their installation instructions: [Install Hugo](https://gohugo.io/getting-started/installing/)

### Clone the Repo
When cloning our repo look out as we use submodules. Make sure to include `--recurse-submodules`:

```bash
git clone --recurse-submodules https://github.com/TomLawson/nextrip.git
```
### Run the local dev server
Start a local dev server with -
```bash
hugo -D serve
```
use `-D` to include pages marked as draft.

### Building
To build the site use -
```bash
hugo
```
The output should be in the `./public/` directory.

Use the `-D` flag to include draft pages in your build e.g. `hugo -D`. 

## Contributing
### Content structure
```bash
./content
 ├── <trip_name>/
     ├── index.md # Trip post content
     ├── <images> # Include the images for a post in the same directory
 ├── <trip_name_2>/  
 ├── <trip_name_3>/
 ├── <trip_name_n+1>/
```

### New pages
Add new pages using the `hugo new` command.
Usage is:
```bash
hugo new [path]
```
For example, to create a new trip called Berlin, use the following: 
```bash
hugo new trips/berlin/index.md
```

### Metadata
#### Default
Each page created with the `hugo new` command will come with the following metadata at the top:
```yaml
---
title: "Berlin"
date: 2021-02-14T17:13:48Z
draft: true
---
```
The three characters before and after the metadata denote the markup language:
* `---` is used for [YAML](https://yaml.org). 
* `+++` is used for [TOML](https://toml.io/en/).

#### Useful Fields
##### Cover Image
To include a cover image include the following in the metadata: 
```yaml
image: <image_name>
```

##### Tags
Tags are shown at the end of the document, and in the sidebar of the home page. To include tags:
```yaml
tags:
  - "tag1"
  - "tag2"
```

##### Categories
Categories are included under the title/subtitle on the post, and the home feed. Include them like so:
```yaml
categories:
  - "category1"
  - "category2"
```
