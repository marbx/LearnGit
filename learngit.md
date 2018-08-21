

#### Setup salt 

    git clone https://github.com/markuskramerIgitt/salt.git
    git remote add upstream https://github.com/saltstack/salt.git
    git remote -vv


#### Update salt (first local, then Github)

    git fetch --tags --all
    git pull upstream develop
    git push

#### Checkout head branch of salt

    git checkout develop

#### Checkout tag (a fixed point in time) of salt

    git checkout v2016.11.1 


#### Revert changes

    git checkout .    | revert changes on your working copy
    git clean -n      | show delete
    git clean -f      | delete files
    git clean -fd     | delete file and folders

#### Bizarr, Restart fork?

    git remote update
    git reset --hard upstream/develop --
    git push origin develop --force
    git push origin +develop


#### Setup salt-windows-msi
    git clone https://github.com/markuskramerIgitt/salt-windows-msi.git
    git remote add upstream https://github.com/saltstack/salt-windows-msi.git


#### Setup/update libtorrent
    git clone https://github.com/arvidn/libtorrent.git
    git remote add upstream https://github.com/arvidn/libtorrent.git
    git fetch --all
    git pull upstream master
    git push


#### Else


    git checkout -b PIECE_OF_WORK upstream/develop                             | local branch for new things                       |
    git checkout -b PIECE_OF_WORK upstream/2015.8                              | local branch for bug fixes                        |
    git branch -d the_local_branch_you_want_to_delete                          |                                                   |
    git branch setup_py_should_not_print_each_file                             |                                                   |
    git checkout setup_py_should_not_print_each_file                           |                                                   |
    git commit -a                                                              |                                                   |
    git log                                                                    |                                                   |
    git rebase upstream/develop                                                | put my commit back on top after getting all other |
    git push origin nssm_description                                           |                                                   |
    git push origin setup_py_should_not_print_each_file                        |                                                   |
    git rebase upstream/setup_py_should_not_print_each_file                    | put my commit back on top after getting all other |


