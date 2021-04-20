# Publisher
Publisher improves content management for static site generators like [Jekyll](https://github.com/jekyll/jekyll) by programmatically exporting a markdown note and its assets to a desire format. It can be used as CLI or API and supports Jekyll posts and PDFs. Although custom rules can be configured to create new integrations and support a large variety of inputs and outputs. 

## Use cases
### Export to Jekyll
You have a markdown note that you want to publish on your site without having the trouble of manually copying, organizing and renaming links following Jekyll structure. 

### Export to PDF
You have a markdown note that you want to export PDF for printing or sharing. 

## Design
- Metadata is parsed from the [YAML front matter](https://jekyllrb.com/docs/front-matter/) in the markdown note.
- It follow links on notes to get assets and provide then statically.
- Images are automatically optimized for web or printing. 

## Usage
*work in progress*

```python
import publisher
...
```

```sh
# implicit rules
publisher note.md file.pdf

# explicit rules
publisher --jekyll note.md site/

# ignore external links (eg: https://google.com/image.jpg)
publisher --ignore-external note.md site/

# export blank (eg. a post with today's date and defaults)
publisher site/
```

## Development Roadmap
- [X] README.md
- [ ] Testing samples (input: MD note and assets; output: Jekyll post and assets)
- [ ] IO handling (read, write copy files)
- [ ] YAML front matter parsing
- [ ] Assets crawling
- [ ] Rules for Jekyll post
- [ ] Image optimization
- [ ] Export to PDF (try [m2pdf](https://github.com/jmaupetit/md2pdf))
