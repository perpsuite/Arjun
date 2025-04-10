
<h1 align="center">
  <br>
  <a href="https://github.com/s0md3v/Arjun"><img src="https://image.ibb.co/c618nq/arjun.png" alt="Arjun"></a>
  <br>
  Arjun
  <br>
</h1>

<h4 align="center">HTTP Parameter Discovery Suite</h4>

<p align="center">
  <a href="https://github.com/s0md3v/Arjun/releases">
    <img src="https://img.shields.io/github/release/s0md3v/Arjun.svg">
  </a>
  <a href="https://pypi.python.org/pypi/arjun/">
    <img src="https://img.shields.io/pypi/v/arjun.svg">
  </a>
  <a href="https://github.com/s0md3v/Arjun/issues?q=is%3Aissue+is%3Aclosed">
      <img src="https://img.shields.io/github/issues-closed-raw/s0md3v/Arjun?color=dark-green&label=issues%20fixed">
  </a>
  <a href="https://travis-ci.com/s0md3v/Arjun">
      <img src="https://img.shields.io/travis/com/s0md3v/Arjun.svg?color=dark-green&label=tests">
  </a>
</p>

![demo](https://i.ibb.co/p3VKSRJ/arjun-demo.png)


### TODO ###


### What's Arjun?

Arjun can find query parameters for URL endpoints. If you don't get what that means, it's okay, read along.

Web applications use parameters (or queries) to accept user input, take the following example into consideration

`http://api.example.com/v1/userinfo?id=751634589`

This URL seems to load user information for a specific user id, but what if there exists a parameter named `admin` which when set to `True` makes the endpoint provide more information about the user?\
This is what Arjun does, it finds valid HTTP parameters with a huge default dictionary of 25,890 parameter names.

The best part? It takes less than 10 seconds to go through this huge list while making just 50-60 requests to the target. [Here's how](https://github.com/s0md3v/Arjun/wiki/How-Arjun-works%3F).

### Why Arjun?

- Supports `GET/POST/POST-JSON/POST-XML` requests
- Automatically handles rate limits and timeouts
- Export results to: BurpSuite, text or JSON file
- Import targets from: BurpSuite, text file or a raw request file
- Can passively extract parameters from JS or 3 external sources

### Installing Arjun
The recommended way to install `arjun` is as following:
```
pipx install arjun
```
> Note: If you are using an old version of python, use pip instead of pipx.

### How to use Arjun?

A detailed usage guide is available on [Usage](https://github.com/s0md3v/Arjun/wiki/Usage) section of the Wiki.

Direct links to some basic options are given below:

- [Scan a single URL](https://github.com/s0md3v/Arjun/wiki/Usage#scan-a-single-url)
- [Import targets](https://github.com/s0md3v/Arjun/wiki/Usage#import-multiple-targets)
- [Export results](https://github.com/s0md3v/Arjun/wiki/Usage#save-output-to-a-file)
- [Use custom HTTP headers](https://github.com/s0md3v/Arjun/wiki/Usage#use-custom-http-headers)

Optionally, you can use the `--help` argument to explore Arjun on your own.

##### Credits
The parameter names wordlist is created by extracting top parameter names from [CommonCrawl](http://commoncrawl.org) dataset and merging best words from [SecLists](https://github.com/danielmiessler/SecLists) and [param-miner](https://github.com/PortSwigger/param-miner) wordlists into that.\
`db/special.json` wordlist is taken from [data-payloads](https://github.com/yehgdotnet/data-payloads).
