# Hello


1. `npm install rescript`
2. Add to `package.json`
```
"scripts": {
    "build": "rescript",
    "start": "rescript build -w"
  },
```
3. `mkdir src`
4. `cd src`
4. `touch Hello.res` (linux)
5. `cd ..`
6. create `bsconfig.json`

bsconfig.json

```
{
    "name": "your-project-name",
    "sources": [
        {
            "dir": "src",
            "subdirs": true
        }
    ],
    "package-specs": [
        {
            "module": "commonjs",
            "in-source": true
        }
    ],
    "suffix": ".bs.js",
    "bs-dependencies": []
}
```

7. Add to src/Hello.res

```
Js.log("hello, world")
```

8. `npm run build`

9. `node src/Hello.bs.js`