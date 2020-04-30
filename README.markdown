Here's my Pandoc letterhead template, adapted from [Scott Hartley](https://blog.hartleygroup.org/2015/08/01/a-pandoc-template-for-letterhead/). Requires the IISG logo and a copy of Stuart's signature to be placed in a support-file directory. It also requires [Fira Sans](https://github.com/bBoxType/FiraSans) and [ETBembo](https://github.com/edwardtufte/et-book) fonts, both of which are available for free (as in freedom).

See `test.markdown` for an example letter. The important part is the metadata block in the beginning and the letter header.

Here's the metadata block:

    ---
    size: 11pt
    sig:
     include: yes
     sign: yes
     post: yes
    cc:
    ---

`Size` is the font size. 11pt is pretty good, 12 starts to get a bit big.

There are several signature options in the `sig` chunk. Each of these can be turned off by leaving them blank or turned on by adding any text to the line.

- `include`: should the signature block (i.e., the "Sincerely", signature image, and job title) be included?
- `sign`: should the signature image be included?
- `post`: should my job title printed after my name?

`cc:` any text here will be rendered in a cc line at the end of the letter.


Here's the header:
    \today
    
    | Someone
    | 123 Some St.
    | Anywhere, IN 12345
    
`\today` prints today's date and the lines prefaced with `|` create the address block for the recipient.