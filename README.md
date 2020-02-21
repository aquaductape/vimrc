# The Ultimate vimrc - Addons Edition

Additional mappings and a few modifications. [EasyMotion](https://github.com/easymotion/vim-easymotion) is included in the plugins.

## How to install the Addons Edition?

### Install for your own user only

    git clone --depth=1 https://github.com/aquaductape/vimrc.git ~/.vim_runtime && sh ~/.vim_runtime/install_awesome_vimrc.sh

### Install for multiple users, even root!

To install for multiple users, the repository needs to be cloned to a location accessible for all the intended users.

    git clone --depth=1 https://github.com/aquaductape/vimrc.git /opt/vim_runtime

    # to install for all users with home directories
    bash /opt/vim_runtime/install_awesome_parameterized.sh /opt/vim_runtime --all

    # to install for specific users
    bash /opt/vim_runtime/install_awesome_parameterized.sh /opt/vim_runtime user0 user1 user2

Naturally, `/opt/vim_runtime` can be any directory, as long as all the users specified have read access.

### Update to latest version

Do git rebase!

    cd ~/.vim_runtime
    git pull --rebase

    # If you installed for multiple users
    cd /opt/vim_runtime
    git pull --rebase

## How to include your own stuff?

After you have installed the setup, you can create **~/.vim_runtime/my_configs.vim** to fill in any configurations that are important for you. For instance, my **my_configs.vim** looks like this:

    ~/.vim_runtime (master)> cat my_configs.vim
    map <leader>ct :cd ~/Desktop/Todoist/todoist<cr>
    map <leader>cw :cd ~/Desktop/Wedoist/wedoist<cr>

You can also install your plugins, for instance, via pathogen you can install [vim-rails](https://github.com/tpope/vim-rails):

    cd ~/.vim_runtime
    git clone git://github.com/tpope/vim-rails.git my_plugins/vim-rails

## How to uninstall

Just do following:

- Remove `~/.vim_runtime`
- Remove any lines that reference `.vim_runtime` in your `~/.vimrc`
