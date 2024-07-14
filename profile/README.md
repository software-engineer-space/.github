
# software-engineer.space domain name 🧑‍🚀💻

This organization contains automations and tools to offer a subdomain for `software-engineer.space` for anyone asking.
Any subdomain granted needs to be served by GitHub and its repository should be placed under the `sofware-engineer-space`
organization.

## How to claim `your-domain.software-engineer.space`

In order to register `your-domain` subdomain and have it assigned to your user on GitHub (`your-github-username` in the 
following example), create a PR in the [`software-engineer.space-terraform` repository](https://github.com/software-engineer-space/software-engineer.space-terraform)
which adds to the [`spaces` variable](https://github.com/software-engineer-space/software-engineer.space-terraform/blob/main/spaces.tf#L2)
an entry with the following shape

```terraform
{
github_handle = "your-github-username"
dns_prefix = "your-domain"
}
```

Whenever possible the PR will be merged and changes applied.

Your GitHub user will be assigned with the permissions to write on the newly created `your-domain.sogware-engineer.space`
in order to modify the content of the website.