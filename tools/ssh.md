# Multi-user

Quite often, you'll want to be able to access Github (or a similar site) with multiple users from the same machine. For instance, cloning personal repositories with a personal account, then interacting with work repositories with a work account.

Firstly, you need to make sure you have two _different_ SSH keys - one for each of the accounts that you want to interact with. 

Separating these into `id_work` and `id_personal` makes it easier to differentiate which key is for which account.

Once that's done, edit the SSH configuration file like so to map the work and personal keys accordingly.

```
Host github.com-work
	HostName github.com
	IdentityFile ~/.ssh/id_work

Host github.com-personal 
	HostName github.com
	IdentityFile ~/.ssh/id_personal
```

After this, if you want to clone a repository with your work account, you can simply do `git clone git@github.com-work:org/repo-name.git` (as long as you've added the SSH key to your account beforehand), and you can do `git clone git@github.com-personal:org/repo-name.git` to clone with your personal account.

This can also work if you have multiple work or personal accounts as well, just make sure you have one SSH key per account that you want to use on the machine.