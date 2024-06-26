tags : #git
### New repo setup
- ![[Pasted image 20230713133818.png]]

Undo `git add` command
- `git reset .`
- https://stackoverflow.com/questions/4639091/undo-git-add-dir#:~:text=You%20will%20want%20to%20use,files%20manually%20and%20unstage%20them%20%E2%80%A6

If there is conflixt in pull from remote
```bash
git pull origin main --rebase
```
push a local new branch(features) to remote as the same name 
```bash
git push -u origin features
```
tracking a remote branch to local with the same name
```bash
git checkout --track origin/features/downloader
```
deleting local branch(features)
```bash
git branch -d features
```
deleting remote branches (features/downloader)
```bash
git push origin --delete features/downloader
```
Merging branches
```bash
git switch main
git merge features/downloader
```
compare branches main and features/downloader --- in local
- it will show new changes that are present in features/downloader branch which are not present in main
```bash
git log main..features/downloader
```
compare branches main and features/downloader --- in remote
- it will show new changes that are present in local main branch which are not present in origin/main
```bash
git log origin/main..main
```