# EEA Client Specification Source Code Conventions


The [source for the client Specification](docs/spec.html) is written in
"Github-flavored Markdown", a combination of HTML with some simple formatting,
that is converted to HTML for publication as the editor's draft by a tool called
ReSpec.

## Source Files

The Specification source file is [docs/spec.html](docs/spec.html), along with
images in the `images/` directory.

The files in the `docs/` directory are the published editors' draft, and are
updated by the Specification editors.

Other files in the repository are information for contributors. To archive a
file, such as an MS Word document describing a change proposal (as opposed to
making a Pull Request or an Issue comment), please use the Technical
Specification Working Group (TSWG) pages in the
[EEA Member Collaboration site](https://member.EntEthAlliance.org/).

## General Style

### Headings


Section headings at all levels should be written using combined section and
heading HTML elements, with an `id` attribute beginning with "sec-" in the
section element. The `id` should be distinctive enough so as not to be
accidentally duplicated. Headings should be indented by two spaces. For
subheadings, use nested section elements with appropriate heading elements. For
example:

```
<section id="sec-breaking-changes">

  <h2>Breaking Changes</h2>
...

<section id="sec-more-breaking-changes">

  <h3>More Breaking Changes</h3>
...

</section>

</section>
```

If _changing_ the text of a heading, do **not** change the `id` in the section
tag. This will result in broken references in the Specification, a problem that
will increase with time.

### Paragraphs

For enhanced readability and editability when working on the source text,
paragraphs should wrap at 80 characters. Use a return at the end of a word as
close as possible to 80 characters. Do not include a space at the end of the
line.

Where a term definition or some other kind of link extends over 80 characters,
insert a return so as to keep the definition or link together all on one line.
In cases where the link takes up more than 80 characters, leave it on a line all
by itself.

Where paragraph elements are used (`<p>` and `</p>`), isolate the elements onto
separate lines at the beginning and the end of the paragraph text, indented by
two spaces, then include the paragraph text on the lines between the elements.
Do not indent the paragraph text.

See below for some examples.

```
  <h2>Example Heading (intended by two spaces)</h2>

This is an example paragraph where the text in the paragraph exceeds 80
characters. A return (no space) is used after `80`.

  <p>
This example paragraph uses paragraph elements. `<p>` and `<\p>` are both on
separate lines and indented by two spaces. The paragraph text itself is not
indented, and returns (no spaces) are used after the words `on` and `not`.
  </p>

This example includes a term definition, such as
<a>Enterprise Ethereum Client</a>, which causes the line to exceed 80
characters. In this case, use a return (no space) after `as` to keep the term
definition together on the one line.
```

#### References to Sections

Inline references to sections are written as shown in the following example:

```
More information about breaking changes is described in Section
<a href="#sec-breaking-changes">11.1 Breaking Changes</a>.
```

### Code samples

Code highlighting is applied for HTML, JavaScript, Solidity, and ABNF if code is
wrapped in a `pre` element and has a class corresponding to the language. For
example:

```
<pre class="solidity">
pragma solidity ^0.4.24;

interface Jokers {
  // This is a dummy.
  function getStyle() external view returns (string);
}
</pre>
```

Note the following about code samples:

* Indents and close brackets, etc. as shown in the example above
* Use two spaces, not tabs
* Keep line length below 80 characters
* Keep comments to a single line
* Use one line per instruction

If you need several lines of explanation, link to text outside the example:

```
<pre class="js" id="code-aces-one">
function Aces(suits) {
  // This is a joker.
  getStyle(<a href="param-aces-suits">suits</a>);
}
</pre>

  <p id="param-aces-suits">
The `suits` parameter takes one of the following values:
  </p>

* `not you`
* `sharp`
* `clubs`
* `lounge`  
```

### Examples

Examples must be within an element with the class `example`, and have a title:

```
  <aside class="example" title="a unique title">
This is an example of a unique title - being the only example in this document

I could have code here too...

<code>*B*^II^I G</code>
  </aside>
```

Any element suitable for the example can be the container, for example `ul`,
`p`, `div`, and so on.

### Notes

Informative notes that have no impact on conformance should be in an element
with the class 'note'

```
  <aside class="note">
This approach is copied from other specifications, such as W3C's Web standards.
  </aside>
```

### Change History

Ensure all changes affecting conformance of clients are recorded in the Revision
History section.

### Conformance Requirements

The terms MUST, SHOULD, MUST NOT and SHOULD NOT have very specific meanings in
the specification. Only use them to make explicit conformance requirements on
Enterprise Ethereum Clients.

Each requirement has a label, so people can refer to it, and an `id` attribute
to give it a URL. For example:

```
  <p id="req-priv-23">
<b>[P] PRIV-23</b>: Implementations MUST NOT publish user passwords in public
profiles.
  </p>
```

Where "[P]" denotes the requirement as one that applies to keep the blockchain
itself functioning, "PRIV-23" is the requirement's label, and its URL is
https://entethalliance.github.io/client-spec/spec.html#req-priv-23.

Identifiers for requirements are managed by the editors, and will not change.
Requirements that are removed will be recorded in the specification change
history. All conformance requirements have a URL Fragment identifier that begins
with the string "req-".

## ReSpec

The
[Editors' draft of the client specification](https://entethalliance.github.io/client-spec/spec.html)
is built using ReSpec, a tool for managing the Table of Contents, References,
term definitions, and styling.

Specifically, there is some HTML at the top of the
[source file](docs/spec.html), and some javascript at the end for configuring
publication information. In general, only Specification editors need to change
this content.

### Definitions

For all terms defined by the specification, the definition should be located at
the _most appropriate_ place in the document. That place might be where the term
is first used, or it might be in a section where the term is discussed in more
detail, has examples about the term, and so on. If in doubt, ask one of the
editors.

To define a new term, use the HTML `dfn` element. For example,
`<dfn>Goose Bridle</dfn>`. You can link to a definition using the HTML `a`
element. For example, `Lorem ipsum <a>Goose Bridle</a> dolor sit amet...` links
the text "Goose Bridle" to that definition.

Use the `data-lt` attribute to add alternative link terms likely to appear in
the text. For example,
`<dfn data-lt="goose bridling|goose bridler">Goose Bridle</dfn>`. Text for the
`data-lt` attribute is not case sensitive. The text
`Lorem <a>Goose Bridling</a> ipsum <a>Goose Bridler</a> amet, consectetur <a>Goose Bridle</a>`
creates three links to the same definition.

**Please Note** If you add or remove a definition, you need to manually update the index of terms.

### References

References are enclosed in double square brackets. `[[reference-name]]` for
informative references, or with an exclamation point `[[!reference-name]]` for
normative references that impact conformance requirements.

`reference-name` can be an RFC, a reference defined in
[SpecRef](https://www.specref.org/), or a reference described in the
`localBiblio` configuration object at the end of the Specification source file.

To add a new reference, provide the relevant information in the `localBiblio`
object, in the following format:

```
"reference-name" : {
  title : "The Formal Title",
  author : "A. Writer",
  publisher : "Organisation name",
  href : "http://example.org/my/great-paper.wp"
}
```

All parameters are optional. The format is JSON, where getting the commas
correct is **very important**. (If you make a single error, the spec will not be
parsed by ReSpec and will appear in raw form).
