# 演示如何进行持续集成和静态分析 [![build status](http://gitlab.ztgame.com/tech/public/demo-how-to-use-ci-and-code-analysis/badges/master/build.svg)](http://gitlab.ztgame.com/tech/public/demo-how-to-use-ci-and-code-analysis/commits/master) [![coverage report](http://gitlab.ztgame.com/tech/public/demo-how-to-use-ci-and-code-analysis/badges/master/coverage.svg)](http://gitlab.ztgame.com/tech/public/demo-how-to-use-ci-and-code-analysis/commits/master)

这个项目演示了如何使用CI以及对项目进行静态代码分析，同时获取项目的测试覆盖率。

该项目在每天下午5点会自动进行`Daily build`.

## 关于

```
- src
- - Demo.HelloWorld        // net standard 2.0 演示项目
- - Demo.HelloWorld.Tests  // net core 2.0 单元测试项目
- - analysis.ruleset       // 静态分析器规则文件
- - analysis.test.ruleset  // 静态分析器规则文件(单元测试项目)
- - settings.runsettings   // 单元测试运行时配置
- - stylecop.json          // StyleCop.Analyzers 分析器的配置
- - Directory.Build.props  // 配置文件
```

## 复杂开始

复杂开始介绍了完全全新创建一个项目，该怎么实现这一套流程。

首先，创建一个空的项目。

复制src目录下指定的到您的项目：

- analysis.ruleset
- analysis.test.ruleset
- settings.runsettings
- stylecop.json
- Directory.Build.props

最后增加CI文件，连通持续集成（请参考当前项目的ci配置）。