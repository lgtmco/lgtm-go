Download the package:

```
go get -u github.com/lgtmco/lgtm
```

In order to create a client you need to provide your API token. You can get an API token using the command line utility. See [lgtm-cli](https://github.com/lgtmco/lgtm-cli) for detailed instructions.

```Go
addr := "http://lgtm.co"
token := "ba945cbb285df8b6bdacb3820c9bf405351acc"

client := lgtm.NewClientToken(addr, token)
```

Get a list of repositories:

```Go
repos, err := client.Repos()
```

Get a repository maintainers file:

```Go
maintainers, err := client.Maintainer("octocat/hello-world")
```

Activate and de-activate a repository:

```Go
err := client.RepoActivate("octocat/hello-world")
err := client.RepoDeactivate("octocat/hello-world")
```
