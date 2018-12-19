# chive-action

Create a NOTICE attribution file based on your package-lock.json as a github action!

- uses https://www.npmjs.com/package/tiny-attribution-generator and https://clearlydefined.io to generate
- devDependencies filtered out (todo: add argument to bring them in)
- optional argument for path to template to use for generation (todo)
- optional argument for filename to use

add ./github/main.workflow to your repo

```
workflow "NOTICE file generate" {
  on = "push"
  resolves = ["Chive Action"]
}

action "Chive Action" {
  uses = "dabutvin/chive-action@master"
  secrets = ["GITHUB_TOKEN"]
}
```
