copy the script to ~/.local/scripts/tmux-sessionizer

bind C-f in kitty.conf
=> map ctrl+f send_text all tmux-sessionizer\n

edit .bashrc
# export PATH="$HOME/.local/scripts:$PATH"
# bind '"\C-f":"./tmux-sessionizer\n"'

bindkey in .tmux.conf
=> bind-key -r f run-shell "tmux neww ~/.local/scripts/tmux-sessionizer"
