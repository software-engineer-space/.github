
# software-engineer.space domain name 🧑‍🚀💻

This organization contains automations and tools to offer a subdomain for `software-engineer.space` for anyone asking.
Any subdomain granted needs to be served by GitHub and its repository should be placed under the `sofware-engineer-space`
organization.

## How to claim `your-domain.software-engineer.space`

In order to register `your-domain` subdomain and have it assigned to your user on GitHub (`your-github-username` in the 
following example), create a PR in the 
[software-engineer.space-terraform repository](https://github.com/software-engineer-space/software-engineer.space-terraform)
which adds to the root of the repository a file named `your-domain.software-engineer.space.tf`.

The content of the file should be the following:
```terraform
module "your-domain" {
  source             = "./modules/software-engineer-space"
  domain_prefix      = "your-domain"
  github_handle      = "your-github-username"
  cloudflare_zone_id = cloudflare_zone.software-engineer-space.id

  providers = {
    cloudflare = cloudflare
    github = github
  }
}
```
Whenever possible the PR will be merged and changes applied.

Your GitHub user will be assigned with the permissions to write on the newly created `your-domain.sogware-engineer.space`
in order to modify the content of the website.