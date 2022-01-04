## release

1. input publish version
   1. patch/prepatch
   2. minor/preminor
   3. major/premajor
   4. prerelease
   5. custom publish version
2. run tests
3. update package.json version field
4. update package.json dependencies and peerDependencies
5. build package
6. generate changeLog
7. update lockfile
8. commit changes
   1. git add
   2. git commit -m release:vx.x.x
9. publish to npm
10. git push
    1. git tag
    2. git push tag
    3. git push

### debug

* [Debugging Guide](https://nodejs.org/en/docs/guides/debugging-getting-started/)

#### debug rollup.config.js

不知道为什么在`webstorm`中调试，有些变量查看有问题？
1. `rollup.config.js`想要调试的一行输入`debugger`
2. 命令行输入：
   ```shell
   node inspect node_modules/rollup/dist/bin/rollup -c --environment TARGET:reactivity
   ```
3. 浏览器打开 chrome://inspect/#devices
4. 点击浏览器页面`Remote Target`中的`inspect`
