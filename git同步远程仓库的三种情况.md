当远程仓库是干净的时候：

```shell
echo "# a" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:conversekuang/xx.git
git push -u origin master
```



当远程仓库和本地不是fast-forward时候：

- 用pull

```shell
git remote add origin git@github.com:conversekuang/xx.git
git pull --allow-unrelated-histories origin master 
git push origin master
```



- 先fetch再本地merge, 最后推到远端

```shell
git remote add origin git@github.com:conversekuang/xx.git
git fetch origin master
git branch -av
git checkout master 
git merge --allow-unrelated-histories origin/master 
git push origin
```





