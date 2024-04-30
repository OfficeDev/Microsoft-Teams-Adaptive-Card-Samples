# Contributing
`need to update this page`


We follow a [code of conduct](http://www.google.fr/ "Named link title") when participating in the community. Please read it before you make any contributions.

- If you plan to work on an issue, mention so in the issue page before you start working on it.
- If you plan to work on a new feature, create an issue and discuss it with other community members/maintainers.
- Ask for help in our community room.

  
## Ways to contribute
- **Stars on GitHub**: If you're a refine user and enjoy using our platform, don't forget to star it on GitHub! 🌟
- **Improve documentation**: Good documentation is imperative to the success of any project. You can make our documents the best they need to be by improving their quality or adding new ones.
- **Give feedback**: We're always looking for ways to make refine better, please share how you use refine, what features are missing and what is done good via GitHub Discussions or Discord.
- **Share our repro**: Help us reach people. Share the [Teams card repository](https://github.com/OfficeDev/Microsoft-Teams-Card-Samples "Teams card repro") with everyone who can be interested.
- **Contribute to codebase**: your help is needed to make this project the best it can be! You could develop new features or fix existing issues - every contribution will be welcomed with great pleasure!

Commit convention
refine is a monorepo. For a monorepo, commit messages are essential to keep everything clear. We use conventional commits to keep our commit messages consistent and easy to understand.

<type>(optional scope): <description>

Examples:

feat: allow provided config object to extend other configs
fix: array parsing issue when multiple spaces were contained in string
docs: correct spelling of CHANGELOG
Git branches
next – contains next version (1.x.0), most likely you would want to create a PR to this branch
master – current stable version
Changeset
Changesets are designed to make your workflows easier, by allowing the person making contributions to make key decisions when they are making their contribution. Changesets hold two key bits of information: a version type (following semver), and change information to be added to a changelog.

Follow the steps below to create a changeset:

npm run changeset

After that you need to,

select the package(s) you are modifying
choose one of major/patch/minor according to your change
add explanation about the changes
explanation should follow the same format with commit convention with some extra description:
