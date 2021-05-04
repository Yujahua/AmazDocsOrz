# `zerone` auto build
auto-buid git repository, zerone means zero to one (0 to 1)

## in steps
1. Baseline branch `chore-dev`, two records

```doc
commit record 1th is: Initial commit
commit record 2th is: chore(basic provied):ver0.9.0
```
used cli commands as below:

```sh
git branch chore-dev
git checkout chore-dev
git add [your basic provied dirs]
git commit -m"chore(README):ver0.9.0"
git push --set-upstream origin chore-dev
```
2. Then, branches been built, by different functions, named `feature-[your function name]`, eg: feature-doc or feature-mongdb
used cli commands as below:

```sh
git branch feature-<your function name>
git checkout feature-<your function name>
git add <your function provied dirs>
git commit -m"feature(<your function name>):add <your function provied dirs names>"
git push --set-upstream origin feature-<your function name>
```

3. Merge
used cli commands as below:

❌<span style="color:red;">**[BAD]**</span>
```sh
git pull --rebase origin feature-blingbling-ideas
```
vs

✅<span style="color:green">**[GOOD]**</span>
```sh
git merge feature-blingbling-ideas
```