## links

### mkdoc

> https://squidfunk.github.io/mkdocs-material/getting-started/
>
> https://github.com/squidfunk/mkdocs-material
>
> https://fonts.google.com/specimen/Cormorant

### nav

> https://nav.ops-coffee.cn
>
> https://github.com/ops-coffee/

## install

1. folder: /d/github/tydjwork/notes

2. git: https://github.com/tydjwork/notes.git

   ```
   git init
   git add .
   git commit -m "init"
   git remote add origin https://github.com/tydjwork/notes.git
   git push -u origin master
   
   git push --set-upstream origin master
   ```

3. start a container

   ```
   docker build . -t mkdocs:tydj
   docker run -it --name mkdocs -p 8080:8000 -v /d/github/tydj.work/notes:/docs -v ~/.ssh:/root/.ssh mkdocs:tydj
   
   docker run -d --name mkdocs-tw --always restart -p 8080:8000 -v /c/users/vtian/onedrive/github/tydjwork/notes:/docs -v ~/.ssh:/root/.ssh mkdocs:tydj
   
   docker run -d --name mkdocs-sl --always restart -p 8081:8000 -v /c/users/vtian/onedrive/github/stocklifelearn/learn:/docs -v ~/.ssh:/root/.ssh mkdocs:tydj
   ```

4. 

### publish to github 

#### inside container

```
mkdocs gh-deploy
```

#### outside container

>https://gist.github.com/cobyism/4730490

```
git subtree push --prefix site origin gh-pages
```

