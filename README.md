# git-gc-bfg-action

```
name: 🔗 git-gc-bfg-action

on:
  repository_dispatch:
  workflow_dispatch:

jobs:
  test_job:
    runs-on: ubuntu-24.04
    name: TEST
    steps:
      - uses: taophilosophy/git-gc-bfg-action@v1.0.33
	with:
      distribution: oracle # not required, default in oracle. See also 'Supported distributions' for available options in https://github.com/actions/setup-java
	  java-version: 21 # not required, default in 21,  See available options in https://github.com/actions/setup-java
      name: ykla # git user name. not required, default in ykla	  
	  email: yklaxds@gmail.com  # git user email. not required, default in yklaxds@gmail.com
      file-size: 2M # file-size to clean in BFG Repo-Cleaner. not required, default in 2M see available options in https://rtyley.github.io/bfg-repo-cleaner/ 
```

So, The The minimum usable configuration is as follows. He will automatically clean up any target file smaller than 2M and auto Git gc.

```
name: 🔗 git-gc-bfg-action

on:
  repository_dispatch:
  workflow_dispatch:

jobs:
  test_job:
    runs-on: ubuntu-24.04
    name: TEST
    steps:
      - uses: taophilosophy/git-gc-bfg-action@v1.0.33
```