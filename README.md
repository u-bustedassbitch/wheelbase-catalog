# wheelbase-db
source information for the wheelbase application

This repository contains the source configuration files used to define manufacturers, brands, models, and other information which
may update more frequently than the **[wheelbase]** application itself.

## FAQ

<dl>
  <dt>Why are these files separate from the source code itself?</dt>
  <dd>It's intended that these files will be used in at least three separate scenarios: <ol>
    <li>"statically"&mdash;compiled into the executable itself;</li>
    <li>"dynamically"&mdash;updated after install by user action;</li>
    <li>"organically"&mdash;these files are human-readable and publicly-accessible for a reason, after all. &#x1f609;</li>
  </ol>
  </dd>
  <dt>Why use TOML for these files instead of something more common like JSON or YAML?</dt>
  <dd><a href='https://toml.io/'><abbr>TOML</abbr></a> (<em>Tom's Obvious Minimal Language</em>)
      offers several advantages for configuration files, particularly in this use case.
    <ul>
      <li>Defined syntax: unlike INI or other free-form configuration formats, TOML has a defined set of allowed types and usage syntax.</li>
      <li>Human readability: while less concise than YAML, TOML is considerably less verbose than JSON.</li>
      <li>Safe(r) parsing of untrusted input: TOML does not provide any reference or macro expansion features.<br />
          This prevents an entire class of input attacks targeting the parser itself.</li>
    </ul>
  </dd>
</dl>

[wheelbase]: https://github.com/u-bustedassbitch/wheelbase/
