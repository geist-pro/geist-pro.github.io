# GEIST Website
=========================
This repository contains the source for the Giest lab website, which can be accessed at [http://geist.pro](http://geist.pro).

The way to add new content to the sections of the website is described below. 
Please follow the instructions and avoid editing any layout or asset files.

This website uses [Jekyll](https://jekyllrb.com) and is hosted using [GitHub Pages](https://pages.github.com). 
Please refer to the official documentation if you intend to make any changes that go beyond addding new content.

Ask [@kirill](https://geist-hq.slack.com/messages/D3B4S9C2V/team/U3B3VTAU8/) for help when stuck.
=========

# News
To add an article in the News section, add a Markdown file into the *_posts* folder.
The name of the file must follow this pattern: *YYYY-MM-DD-articlename.markdown*
At the top of the file, the following block must be present:
```yaml
---
layout:     update
title:      "Lessons from the Dagstuhl Seminar on Eyewear Computing"
date:       2018-03-30 00:00:00
author:     "Kai Kunze"
header-img: img/news/sample_sq.png
---
```

Edit *title*, *date*, *author* and *header-img* as you see fit. Upload the new header image into the img/news folder, ommit *header-img* completely if the article has no image.

# Projects
There are two ways to add a new project into the Projects section.

## 1. By downloading the source code
```bash
git clone https://github.com/geist-pro/geist-pro.github.io.git
cd geist-pro.github.io
./project
# follow the script instructions
git add .
git commit -m "Added the project (PROJECT_NAME)"
git push origin master
```

## 2. Directly on GitHub
1. First, decide on a short unique alias for the project that will be used in its url (e.g. http://geist.pro/projects/banana). For this example, let's choose *banana* as our alias.
2. Create a /img/projects/banana folder. Upload your images there.
3. Create a /projects/banana.html file with the following content:
  ```yaml
  ---
  layout: project
  project: banana
  ---
  ```
4. Describe your project by adding the follwing entry to the \_data/projects.yaml file:
  ```yaml
  - id: banana
    title: The Glorious Banana Project
    description: |
      Descibe your bananas here
    date: 2018 - today
    main_image: img/projects/banana/main.jpg
    images:
      - img/projects/banana/1.jpg
      - img/projects/banana/2.jpg
    videos:
      - https://www.youtube.com/watch?v=sFukyIIM1XI
  ```

# Other
## Publications, Collaborators, Geist Members, Geist Description
To edit any of the above, modify the corresponding *.yaml file within the *_data* folder.
