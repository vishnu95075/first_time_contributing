<h1> 👋Hi <br> Wellcome </h1>

# REC Student Fill free to contribute

![recdownload](https://user-images.githubusercontent.com/75454756/135025400-a7309072-02c3-4001-9bd5-8643a4570bf8.jpg)


# First Contributions
# Configuring git

The first time you tried to commit using git, you might have gotten a prompt like the one below:

bash
$ git commit
*** Please tell me who you are.

Run
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.
```

Git needs to know who you are when you create a commit. When you are working collaboratively, you should be able to see who modified what parts of the project and when, and thus, git has been designed to create commits tied to a name and an email.

There are multiple ways to provide the `git commit` command with your email and name, and we'll go through some of them below.

### Global Config

When you store something in the global config, it is accessible system wide in all the repositories you work on. This is the preferred way and works for most use cases.

To store something in the global config, you use the `config` command as follows:

`$ git config --global <variable name> <value>`

In the case of user details, we run it as follows:

```
$ git config --global user.email "you@example.com"
$ git config --global user.name "Your Name"
```

### Repository Config

As the name says, these configurations are scoped to your current repository. If you want to commit to a particular repository, say, a work related project, with your company's email, then you could use this method.

To store something in the repository config, you use the `config` command  by emitting the `--global` flag as follows:

`$ git config <variable name> <value>`

In the case of user details, we run it as follows:

```
$ git config user.email "you@alternate.com"
$ git config user.name "Your Name"
```

### Command-line Config

These type of configurations are scoped to the current command only. All git commands take `-c` arguments before the action verb to set temporary configuration data.

To store something in the command line config, run your command as follows:

`$ git -c <variable-1>=<value> -c <variable-2>=<value> <command>`

In our example, we would run the commit command as follows:

`git -c user.name='Your Name' -c user.email='you@example.com' commit -m "Your commit message"`

### Note on Precedence

Among the three methods described here, the precedence order is `command-line > repository > global`. This means that, if a variable is configured in the command-line as well as globally, the command-line value would be used for the operation.

## Beyond User Details

We have dealt with only the user details till now while working with the config. However, there are several other configuration options available. Some of them are:

1.  `core.editor` - to specify the name of the editor used for writing commit messages, etc.
2.  `commit.template` - to specify a file on the system as the initial commit template.
3.  `color.ui` - to specify a boolean value for using colors in git's output.

We have abstracted some details for ease of understanding. For further reading, head over to [git-scm.com](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration).



This project aims to simplify and guide the way beginners make their first contribution. If you are looking to make your first contribution, follow the steps below.

_If you're not comfortable with command line, [here are tutorials using GUI tools.](#tutorials-using-other-tools)_

<img align="right" width="300" src="https://firstcontributions.github.io/assets/Readme/fork.png" alt="fork this repository" />

#### If you don't have git on your machine, [install it](https://help.github.com/articles/set-up-git/).

## Fork this repository

Fork this repository by clicking on the fork button on the top of this page.
This will create a copy of this repository in your account.

## Clone the repository

<img align="right" width="300" src="https://firstcontributions.github.io/assets/Readme/clone.png" alt="clone this repository" />

Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the _copy to clipboard_ icon.

Open a terminal and run the following git command:

```
git clone "url you just copied"
```

where "url you just copied" (without the quotation marks) is the url to this repository (your fork of this project). See the previous steps to obtain the url.

<img align="right" width="300" src="https://firstcontributions.github.io/assets/Readme/copy-to-clipboard.png" alt="copy URL to clipboard" />

For example:

```
git clone https://github.com/this-is-you/first-contributions.git
```

where `this-is-you` is your GitHub username. Here you're copying the contents of the first-contributions repository on GitHub to your computer.

## Create a branch

Change to the repository directory on your computer (if you are not already there):

```
cd first-contributions
```

Now create a branch using the `git checkout` command:

```
git checkout -b your-new-branch-name
```

For example:

```
git checkout -b add-alonzo-church
```

(The name of the branch does not need to have the word _add_ in it, but it's a reasonable thing to include because the purpose of this branch is to add your name to a list.)

## Make necessary changes and commit those changes

Now open `Contributors.md` file in a text editor, add your name to it. Don't add it at the beginning or end of the file. Put it anywhere in between. Now, save the file.

<img align="right" width="450" src="https://firstcontributions.github.io/assets/Readme/git-status.png" alt="git status" />

If you go to the project directory and execute the command `git status`, you'll see there are changes.

Add those changes to the branch you just created using the `git add` command:

```
git add Contributors.md
```

Now commit those changes using the `git commit` command:

```
git commit -m "Add <your-name> to Contributors list"
```

replacing `<your-name>` with your name.

## Push changes to GitHub

Push your changes using the command `git push`:

```
git push origin <add-your-branch-name>
```

replacing `<add-your-branch-name>` with the name of the branch you created earlier.

## Submit your changes for review
