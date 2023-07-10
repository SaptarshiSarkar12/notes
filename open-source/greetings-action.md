# Greetings Action

```yml
name: Greetings

on: [pull_request_target, issues]

jobs:
  welcome:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v3
        - uses: EddieHubCommunity/gh-action-community/src/welcome@main
          with:
            github-token: ${{ secrets.GITHUB_TOKEN }}
            issue-message: '<h3>Hello 👋! Thank you very much for raising an issue 🙌! The maintainers will get back to you soon for discussion over the issue! 🚀</h3>'
            pr-message: '<h3>Yeah! You did it 🎉 Now, Relax 😉, Grab a drink ☕, and wait for the maintainers to check your contributions. Meanwhile, you can discuss on other issues and solve them 😀. Thank You 😃!</h3>'
            footer: 'Meanwhile you can also discuss about the project in our <a href="https://discord.gg/DeT4jXPfkG">Discord Server</a> 😀</h3>'
```
