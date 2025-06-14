# Q-Stack

a micro-framework html webstack that is focused for developers

## Why am I making this stack?

with the recent popularity of no-JS frameworks to simplify the web developer experience with tools like HTMX and datastar, I wanted to explore a new way to make a pretty website with **simplicity** in mind

clear advantages of a simple stack. content that is generated from AI still needs representation and styling. however, the overhead to the build and deployment process massively complicates maintenance.

## The Stack

### Core components

- markdown: this will be the source material
- [cmark](https://github.com/commonmark/cmark): conversion from markdown to html
  ```
  cmark $input_file -t html > $output_file
  ```
- [picocss](https://picocss.com/): a minified classless css

### Alternatives

- yaml in place of markdown: full yq insertion functionality and structured data
- [pandoc](https://pandoc.org/) in place of cmark: pandoc is a more fully-fledged tool but it does far more than what is needed. 40MB -> 300kB binary size reduction by using cmark while accomplishing a good 80% of what is needed is also several orders of magnitude improvement in efficiency
- replacing picocss with a whole host of classless css for more functionality and beautification. here is a nice [blog post](https://benhoskins.dev/classless-css/) for a few examples and a larger collection here: [Classless CSS](https://github.com/dbohdan/classless-css)

### Dev Experience

- [entr](https://github.com/eradman/entr): watch file for changes to improve development experience
- [go-task](https://taskfile.dev/): a taskrunner to run some commands for build and deploy
- [yq-go](https://github.com/mikefarah/yq): if we are using go-task and making a yaml for the commands, you might as well do some neat menu tricks for the developer
- [fzf](https://github.com/junegunn/fzf)/[gum](https://github.com/charmbracelet/gum): TUI menu helper

### Deployment

- [envs](https://envs.sh): a neat little open source "host" of assets like images and even full webpages
- [curl](https://github.com/curl/curl): utility to post content to envs.sh
- [DrivetoWeb](https://www.drv.tw/): Neat way to turn spare storage in cloud drives into website and a neat way to share content
  ```
  curl -F'file=@yourfile.png' https://envs.sh
  ```

### Nice to haves

- [nix](https://nixos.org)
- [tgpt]():
- [awk]():
- [graph-easy]()

## Inspiration and Appendix

[the monospace web](https://owickstrom.github.io/the-monospace-web/)
