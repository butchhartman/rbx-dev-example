# Getting Started

## Setup
First, you must download [foreman](https://github.com/Roblox/foreman). It is a package manager for Roblox. It allows us to easily install Roblox development tools on a per-project basis, ensuring all collaborators are using the same version of each tool on each project. It also frees us from having to manually download and set environment variables for each tool.

Download the foreman executable and place it in a folder on your hard drive. Add that folder to your PATH environment variables. Then, make sure it is working by typing:
```
foreman list
```
into your terminal. You should see the following output:
```
Installed tools:

```
Now that we know foreman is working, navigate to your users directory and add `/.foreman/bin` to your PATH environment variables. This will allow us to run the tools foreman installs.

## The Repository
Now, clone this repository as follows:
```
git clone https://github.com/butchhartman/rbx-dev-example
```
Notice that the repository is bare. There are only three .toml files. These are configuration files for each of the tools we will use. Look in `foreman.toml` and notice that each entry is a tool this project will use.
Once you've looked around to your heart's content, run the following in your console (while in the folder you cloned the repository into):
```
foreman install
```
Foreman will now install all the tools listed in the `foreman.toml` file. Try typing the names of the tools into your console. They should now give you some output.

## Creating the Project
Notice the tool named Rojo. This is what our editor will use to communicate with Roblox Studio. It is what enabled us to have a filesystem based project as opposed to Roblox's typical cloud-based approach. To create the initial project, type the following into your console:
```
rojo init
```
You should now see some new files in the project folder. Go into the `src` directory and look through the subdirectories in there. The `client`, `server`, and `shared` directories correspond to StarterPlayer, ServerScriptService, and ReplicatedStorage respectively. Make some changes to these scripts and continue once you are done.

## Building the Project
All that's left to do is to build the project. All you must do is run the following command in your terminal:
```
rojo build -o "rbx-dev-example.rbxlx"
```
You should now see a .rbxlx file in the repository. Open it and observe how it contains your script changes. Try and make some live code changes using the rojo plugin and vscode.
