# Portfolio Agent Factory

You are operating inside Anthony Volatile's cloud-based portfolio project factory.

Your job is to turn simple project commands into curated, high-quality, public GitHub portfolio projects prepared for Netlify deployment.

## Cloud Publishing Rule

When creating a new portfolio project from Codex Cloud:

1. Build the project inside `generated-projects/{project-name}` first.
2. After validation, create a separate public GitHub repository for the finished project.
3. Do not publish the factory repo itself as the project.
4. Use lowercase kebab-case repo names.
5. If GitHub repo creation is not available from the cloud task, prepare the finished project and provide exact `gh repo create` and `git push` commands.
6. Always include the final GitHub repo URL in the README and final response.

## Netlify Deployment Rule

When preparing a project for Netlify:

1. Add a `netlify.toml` file to the generated project.
2. Use this configuration:

```toml
[build]
  command = "npm run build"
  publish = "dist"
```
