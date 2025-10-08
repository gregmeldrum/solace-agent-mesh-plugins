# How to contribute to Solace Community Agent Mesh Plugins

We'd love for you to contribute and welcome your help. Here are some guidelines to follow:

- [New Plugin Submission](#new)
- [Issues and Bugs](#issue)
- [Submitting a fix](#submitting)
- [Feature Requests](#features)
- [Questions](#questions)

## <a name="new"></a> Do you want to submit a new SAM Community Plugin?
A Solace Agent Mesh Plugin is a distributable abstraction for SAM Agents, Gateways and custom integrations.  

To create a new plugin for the SAM Community follow these steps:
#### Step 1: Understand a SAM Plugin
- Browse the [SAM Documentation for Plugins](https://solacelabs.github.io/solace-agent-mesh/docs/documentation/concepts/plugins) 
- Understand the process to [Build your own SAM agent](https://solacelabs.github.io/solace-agent-mesh/docs/documentation/tutorials/custom-agent)

#### Step 2: Browse the Repo

Check that the Agent or Gateway that you would like to create is not already exposed as a Community plugin or as a [core plugin for SAM](https://github.com/SolaceLabs/solace-agent-mesh-core-plugins)


#### Step 3: Follow Steps 1 and 2 of [Submitting](#submitting)

You should now have your own fork and branch of the Community Plugins repo to work on. 

#### Step 4: Initialize a new SAM Plugin
`sam plugin create <your-plugin-name> --type <agent or gateway>`
SAM plugins may contain custom code under the `/src` directory or they may be entirely contained in the `config.yaml` file depending on the complexity and requirements of your plugin. 

#### Step 5: Build your SAM Plugin
In this step we need to add the contents to your newly initialized plugin directory in your branch.  

*Option 1*: Create the implementation and `config.yaml` from scratch.  You will choose this option if you have not done any work on your SAM Agent or Gateway elsewhere.  
*Option 2*: Merge your implementation and `config.yaml` from another location into this plugin directory.  Contributors may choose this option if they previously created a SAM Agent just for their own use in SAM but later decided to contribute it to the Solace Agent Mesh Community as a Plugin.  
To merge your existing agent you will:
1.  Copy the contents of your existing `config.yaml` from the `app:` tag to the end of the file. 
2. Copy any necessary source code into `/src` structure of your repository. 
3. Update the README.md file in your plugin directory to comply with the [Readme Template](./PLUGIN_README_TEMPLATE.md)
4. Update the project root [Readme](./README.md) to include your new plugin in the table. 

#### Step 4: Your Plugin is ready to Submit
Pick up at step 3 in the [Submitting](#submitting) steps to add your changes to the SAM Community Plugin catalog. 


## <a name="issue"></a> Did you find an issue with an existing SAM Community Plugin?

* **Ensure the bug was not already reported** by searching on GitHub under *Issues*

* If you're unable to find an open issue addressing the problem, open a new one

## <a name="submitting"></a> Do you have new code for fixes to submit to SAM Community Plugins?

Open a new GitHub pull request with the patch following the steps outlined below. Ensure the PR description clearly describes the problem and solution or new plugin. Include the relevant issue number if applicable.

Before you submit your pull request consider the following guidelines:

* Search *Pull Requests* for an open or closed Pull Request
  that relates to your submission. You don't want to duplicate effort.

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

Assuming you have not yet pushed your branch to origin, use `git rebase` (not `git merge`) to synchronize your work with the main
repository.

```sh
$ git fetch upstream
$ git rebase upstream/main
```

If you have not set the upstream, do so as follows:

```sh
$ git remote add upstream https://github.com/solacecommunity/solace-agent-mesh-plugins
```

If you have already pushed your fork, then do not rebase. Instead merge any changes from master that are not already part of your branch.

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

## <a name="features"></a> **Do you have an ideas for a new feature or a change to an existing one?**

* Open a GitHub issue and label it as an *enhancement* and describe the new functionality.

##  <a name="questions"></a> Do you have questions about the source code?

* Ask any question about the code or how to use Solace technologies in the [Solace community](https://solace.community).
