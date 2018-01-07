# Verdaccio-GitLab

Use [GitLab Community Edition](https://gitlab.com/gitlab-org/gitlab-ce)
as authentication provider for the private npm registry
[verdaccio](https://www.verdaccio.org), the sinopia fork.

The main goal and difference to other sinopia/verdaccio plugins is:

- no admin token required
- user authenticates with Personal Access Token

> This is experimental!

## Use it

```sh
npm install -g verdaccio-gitlab
```

configure the following within your `~/.config/verdaccio/config.yaml`

```yaml
auth:
  gitlab:
    url: https://gitlab.com
```

authenticate with your gitlab username and your [Personal Access Token](https://gitlab.com/profile/personal_access_tokens)

## Todo

- [x] authenticate with personal access token
- [x] compare provided user name and GitLab username
- [ ] get user groups from GitLab
- [ ] authorize based on group member ship
  - [ ] publish
  - [ ] pull
- [ ] use openid connect for web ui
- [ ] improve linting, eslint vs. jshint, etc.
- [ ] pass repolinter
- make it perfect ;-r

## Inspired by

- [verdaccio-ldap](https://github.com/Alexandre-io/verdaccio-ldap)
- [node-bacstack](https://github.com/fh1ch/node-bacstack)
- [verdaccio-bitbucket](https://github.com/idangozlan/verdaccio-bitbucket)

## License

[MIT](https://spdx.org/licenses/MIT)