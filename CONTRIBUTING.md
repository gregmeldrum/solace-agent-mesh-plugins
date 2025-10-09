# How to Contribute to Solace Community Agent Mesh Plugins

We'd love for you to contribute and welcome your help. Here are some guidelines to follow:

- [New Plugin Submission](#new)
- [Issues and Bugs](#issue)
- [Submitting a Fix](#submitting)
- [Feature Requests](#features)
- [Questions](#questions)

## <a name="new"></a> Do You Want to Submit a New SAM Community Plugin?
A Solace Agent Mesh Plugin is a distributable abstraction for SAM Agents, Gateways, and custom integrations.  

To create a new plugin for the SAM Community, follow these steps:

#### Step 1: Understand a SAM Plugin
- Browse the [SAM Documentation for Plugins](https://solacelabs.github.io/solace-agent-mesh/docs/documentation/concepts/plugins)
- Understand the process to [Build Your Own SAM Agent](https://solacelabs.github.io/solace-agent-mesh/docs/documentation/tutorials/custom-agent)

#### Step 2: Browse the Repo

Check that the Agent or Gateway that you would like to create is not already exposed as a Community plugin or as a [core plugin for SAM](https://github.com/SolaceLabs/solace-agent-mesh-core-plugins).

#### Step 3: Follow Steps 1 and 2 of [Submitting a Pull Request](#submitting)

You should now have your own fork and branch of the Community Plugins repo to work on. 

#### Step 4: Initialize a New SAM Plugin
```bash
sam plugin create <your-plugin-name> --type <agent or gateway>
```
SAM plugins may contain custom code under the `/src` directory, or they may be entirely contained in the `config.yaml` file depending on the complexity and requirements of your plugin. 

#### Step 5: Build Your SAM Plugin
In this step, we need to add the contents to your newly initialized plugin directory in your branch.

**Option 1**: Create the logic implementation from scratch (if required) and customize the generated `config.yaml` to build your plugin functionality, [see the following guides](https://solacelabs.github.io/solace-agent-mesh/docs/documentation/tutorials/custom-agent). You will choose this option if you have not done any work on your SAM Agent or Gateway elsewhere.

**Option 2**: Merge your implementation and `config.yaml` from another location into this plugin directory. Contributors may choose this option if they previously created a SAM Agent just for their own use in SAM but later decided to contribute it to the Solace Agent Mesh Community as a Plugin.

To merge your existing agent, you will:
1. Copy the contents of your existing `config.yaml` from the `app:` tag to the end of the file.
2. Copy any necessary source code into the `/src` structure of your repository.
3. Update the `README.md` file in your plugin directory to comply with the [README Template](./PLUGIN_README_TEMPLATE.md).
4. Update the project root [README](./README.md) to include your new plugin in the table.

#### Step 6: Your Plugin Is Ready to Submit
Pick up at Step 3 in the [Submitting a Pull Request](#submitting) steps to add your changes to the SAM Community Plugin catalog. 


## <a name="issue"></a> Did You Find an Issue with an Existing SAM Community Plugin?

* **Ensure the bug was not already reported** by searching on GitHub under [Issues](https://github.com/solacecommunity/solace-agent-mesh-plugins/issues)

* If you're unable to find an open issue addressing the problem, [open a new one](https://github.com/solacecommunity/solace-agent-mesh-plugins/issues/new)

## <a name="submitting"></a> Do You Have New Code or Fixes to Submit to SAM Community Plugins?

Open a new GitHub pull request with the patch following the steps outlined below. Ensure the PR description clearly describes the problem and solution or new plugin. Include the relevant issue number if applicable.

Before you submit your pull request, consider the following guidelines:

* Search [Pull Requests](https://github.com/solacecommunity/solace-agent-mesh-plugins/pulls) for an open or closed Pull Request that relates to your submission. You don't want to duplicate effort.

### Submitting a Pull Request

Please follow these steps for all pull requests. These steps are derived from the [GitHub flow](https://help.github.com/articles/github-flow/).

#### Step 1: Fork

Fork the current repository and clone your fork
locally.

```sh
git clone https://github.com/solacecommunity/solace-agent-mesh-plugins
```

#### Step 2: Branch

Make your changes on a new git branch in your fork of the repository.

```sh
git checkout -b my-fix-branch main
```

#### Step 3: Commit

Commit your changes using a descriptive commit message.

```sh
git commit -a -m "Your Commit Message"
```

Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

#### Step 4: Rebase (if possible)

Assuming you have not yet pushed your branch to origin, use `git rebase` (not `git merge`) to synchronize your work with the main repository.

```sh
git fetch upstream
git rebase upstream/main
```

If you have not set the upstream, do so as follows:

```sh
git remote add upstream https://github.com/solacecommunity/solace-agent-mesh-plugins
```

If you have already pushed your fork, then do not rebase. Instead, merge any changes from main that are not already part of your branch.

#### Step 5: Push

Push your branch to your fork in GitHub:

```sh
git push origin my-fix-branch
```

#### Step 6: Pull Request

In GitHub, send a pull request to `solace-agent-mesh-plugins:main`.

When fixing an existing issue, use the [commit message keywords](https://help.github.com/articles/closing-issues-via-commit-messages/) to close the associated GitHub issue.

* If we suggest changes then:
  * Make the required updates.
  * Commit these changes to your branch (ex: my-fix-branch)

That's it! Thank you for your contribution!

## <a name="features"></a> Do You Have Ideas for a New Feature or a Change to an Existing One?

* Open a [GitHub issue](https://github.com/solacecommunity/solace-agent-mesh-plugins/issues/new) and label it as an *enhancement* and describe the new functionality.

## <a name="questions"></a> Do You Have Questions About the Source Code?

* Ask any question about the code or how to use Solace technologies in the [Solace Community](https://solace.community).
