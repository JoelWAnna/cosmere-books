# Oathbringer

Tor.com is publishing Oathbringer in serialized form till Chapter 32. This script
downloads all of these posts and converts them into a publishable format, including
epub, mobi, pdf and html. You can find the tor.com announcement at https://www.tor.com/2017/08/15/brandon-sanderson-oathbringer-serialization-announcement/

For obvious reasons, the converted ebook is not part of this repo. You must download
and run the script on your own machine to generate the copies.

The code for this is mostly adapted from [hoshruba](https://github.captnemo.in/hoshruba).

You can download sample files (Lorem Ipsum) from <http://ge.tt/8R61oXm2> to see a sample of how the generated files look.

## Requirements

- Ruby
- Nokogiri gem installed (`gem install nokogiri`)
- Unix system with `wget` installed
- `pandoc` installed and available (for all 3 formats)
- (mobi only): `ebook-convert` (from calibre) available to generate the mobi file
- (pdf) `wkhtmltopdf` for converting html to pdf
- (pdf) `pdftk` to stitch the final PDF file
- (pdf) `imagemagick` to convert jpg to PDF

- The final 3 tools can be skipped if you don't care about the PDF generation.
- You can also skip calibre if you only want the EPUB file.
- Edit the last line in `setup.rb` to `:epub` / `:mobi`, `:pdf` to only trigger the specific builds

# Setup

After downloading the repo and installing the requirements, just run

    ruby setup.rb

All the generated files will be saved with the filename `Oathbringer.{epub|pdf|mobi|html}`

# LICENSE

This is licensed under WTFPL. See COPYING file for the full text.
