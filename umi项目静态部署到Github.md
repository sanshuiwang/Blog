# umi 项目部署到 Github

第一步：在自己项目中`yarn add umi-plugin-gh-pages`

第二步：在 package.json 添加：

```
"scripts": {
    "build": "umi build",
    "deploy": "yarn run build && gh-pages -d dist"
  }
```

第四步： .umirc.js 中

```
plugins: [
    // ref: https://umijs.org/plugin/umi-plugin-react.html
    [
      'umi-plugin-react',
      {
        ...
      },
    ], 'umi-plugin-gh-pages',
  ],
base: '/umi-hero/',
publicPath: '/umi-hero/',
```

第五步：在自己的项目中执行 yarn run deploy

项目: https://github.com/sanshuiwang/umi-hero
访问: https://sanshuiwang.github.io/umi-hero/
访问: https://[自己的github名字].github.io/[项目名称]/
