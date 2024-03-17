# Hyprscratchpad
Hyprscratchpad simplifies the process of creating scratchpad workspaces in Hyprland.
### Installation
Run the following command to create a symbolic link to hyprscratchpad in the /usr/local/bin/ directory:
```bash
sudo ln -sf "$(realpath hyprscratchpad)" /usr/local/bin/
```
### Usage
To use Hyprscratchpad, execute the hyprscratchpad command followed by three arguments:  
```bash
COMMAND # The command to execute within the scratchpad workspace.  
CLASS # The class of the window.  
WORKSPACE # The name of the workspace.  
```
For example:
```bash
hyprscratchpad "alacritty --class my_terminal" "my_terminal" "terminal"
```
Another example in `hyprland.conf`
```bash
bind = $mainMod SHIFT, O, exec, hyprscratchpad obs com.obsproject.Studio obs
bind = $mainMod SHIFT, N, exec, hyprscratchpad "$terminal --class network-manager -e nmtui" network-manager nmtui
bind = $mainMod SHIFT, K, exec, hyprscratchpad "$terminal --class calculator -e python3" calculator calculator
```
This command opens an Alacritty terminal window within a scratchpad workspace named "terminal" with the class "my_terminal". If the workspace already exists, it toggles to that workspace. Otherwise, it creates the workspace and then opens the Alacritty terminal window within it.
### Contribution
Feel free to contribute to Hyprscratchpad by forking the repository, making changes, and submitting pull requests. Your contributions are greatly appreciated!
