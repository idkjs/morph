# morph

[![Build Status](https://dev.azure.com/reason-native-web/morph/_apis/build/status/reason-native-web.morph?branchName=master)](https://dev.azure.com/reason-native-web/morph/_build/latest?definitionId=1&branchName=master)

A tiny framework for developing HTTP stuff in reason native using Httpaf and H2.

## Documentation

https://reason-native-web.github.io/

_The documentation is not as fleshed out as it should be, the repos is under heavy development._

## Build and run examples

```
esy install
esy build
esy examples
$(esy examples-path)/hello_world.exe
$(esy examples-path)/with_router.exe
$(esy examples-path)/simple_proxy.exe
```

## Example

**Server:**

```ocaml
let http_server = Morph_server_http.make();
Morph.start(~servers=[http_server], _request => Http.Response.Ok.make)
|> Lwt_main.run;
```

Slightly larger example using ocaml-routes: https://github.com/reason-native-web/morph/blob/master/examples/with_router.re

## Sponsors

Thank you to [@imbsky](https://github.com/imbsky) for sponsoring my work on Morph
