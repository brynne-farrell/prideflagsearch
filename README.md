# Contributing

## General Principles

The basic process for contributing to this project is:

1. Fork the repository
1. Make a branch named after the work you're doing
1. Commit and push that branch to your repository
1. Make a merge request to merge your branch into the main project's master branch

While a full explanation of using git, GitHub, or any of the technologies used in this website is beyond the scope of this document, email Brynne Farrell at brynne.farrell@gmail.com and she'll be happy to help you get started.

## Contributing New Flags

*Recommended skills: svg editing, json editing, ability to run a django website*

A side objective of this site is to not just collect flags, but make high quality svg files of the flags available for use on other places. In rare cases, it may not be possible to render a flag properly in svg, in which case alternate file types will be accepted. 

To get a flag accepted in a merge request, you'll need to:

1. Have or make an svg version of the flag that automatically scales
1. Find or create a page in Wikimedia with that file
1. Add the flag to `prideflags.json` (with the flag details as described below!) and `search/static/data/img`
1. Mage a merge request into master

### Places to Find New Flags

- Progress pride flag
- Bigender: https://66.media.tumblr.com/3d86267d5d6ee6a42b9424c2aa514a6c/tumblr_inline_nwlg22va1T1snljqo_500.png?fbclid=IwAR2brjJLiNYDTfgYKWnFv_6nowHpiq2EtcTtkOion1ARfux8WQB1qPpVXKg
- Bigender: https://66.media.tumblr.com/91941b330fbbfa81a94408d1035fc1a4/tumblr_inline_nwlgbgLNlI1snljqo_500.png?fbclid=IwAR1nQ7E_cWE4TS_KHpoLTJPBYVJtUteGt84_R6O2DAyr-yd7mXNT44p20N4
- https://www.deviantart.com/pride-flags?fbclid=IwAR1etYmg5R84Reed3MT1aX4wlhjTBlJVQ2uPy-aGkDTu9O-9Nm5oE94YJ-M
- https://beyond-mogai-pride-flags.tumblr.com/?fbclid=IwAR3vsLCXQ2bwKxAuyvUt8shy3ZzxLw6L97572EtTjCTzoOskaHC56Jt-cjI
- https://pride-flags-for-us.tumblr.com/?fbclid=IwAR3ETJfoNNeMMnfa17GdhYt_Amb2zbnHfIlkZiLik8_4As0sVHDuqhxuXR8
- http://gender.wikia.com/wiki/Pride_Flags

## Contributing Flag Details

*Recommended skills: json editing, ability to run a django website*

Flag details sections need to be fleshed out with a description of the identity, name of the author, year of creation, and citations if available. For the more well-known identities Wikipedia can be a great source. However it's not always an accurate or informational source. Above all, make sure the description is how the community's members would describe themselves. 

The `prideflags.json` file uses the following keys in the `citation` key for each flag:

`text` - This is a plain text description of the identity with the target audience being people who have never heard of the identity and don't know any queer theory. It should be written in a Wikipedia-like tone and style. All information should be cited using numbered citations (like `[1]`) corresponding to the list of sources in the `sourceList` key. If there is no description, this value should be set to false.

`sourceList` - This is an ordered list of citations for the text in the `text` key. It is a list of strings that are citations in a modified APA format. Links to websites should be provided in markdown format within this citation to avoid printing a long url on the screen. The domain name, including `www` but excluding `http(s)://` should be inside the square brackets and the full url should be inside the parenthesis. If there are no sources because there is no description, this value should be set to false.

`flagImageSource` - This is a citation in the modified APA format described above. It should be a link to the source svg image. If the svg form of the image seems to be an original work done for this project, that svg image should be uploaded to Wikimedia and Wikimedia should be cited. As a result of the policy of uploading images to Wikimedia, this should never need to be false.

`firstAuthoring` - This is a citation in the modified APA format described above. It should be the first published source for the flag, as best you can determine. If this source cannot be determined, the value should be set to false.

# Planned Features

- Make sure tab accessibility works properly
- Make sure screen readers work properly
- Implement a sorting system, or extra filter to distinguish between more and less common flags
- Browser compatibility initial review
- Add feature for flag alternates (like versions of the gay pride flag)
- Flags to Add to WikiMedia
  - Update the UK Gay Pride Flag wiki with our scalable version https://commons.wikimedia.org/wiki/File:Gay_Pride_flag_of_the_United_Kingdom.svg

