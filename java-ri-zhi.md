---
description: java日志框架结构梳理
---

# Java 日志

在java中, 日志框架分为接口, 适配, 实现三种类型. 其代表性框架如下:

接口框架: Slf4j, JCL...

适配框架: slf4j-log4j12, slf4j-jdk14...

实现框架: log4j, log4j2, logback, JUL...

框架之间的关系如下:

1. 1996年Log4j首先由Ceki开发出来. 解决日志打印需求. 为实现框架
2. 2001年Log4j开源加入Apache, 改名: Apache Log4j. Ceki加入Apache
3. 2002年Sun公司开发JUL(java.util.logging). 对标log4j. 竞争关系.
4. 2002年Apache发布JCL(Jakarta Commons Logging). 解决个日志框架使用复杂问题. 为接口框架
5. 2005年Ceki离开Apache独立开发Slf4j, 为接口框架. 优化JCL. 同时为竞争关系.
6. 2006年Ceki开发Logback, 优化Log4j, 为实现框架. 同时为竞争关系.
7. 2012年Apache发布Log4j2. 对标Logback. 为实现框架, 同时为竞争关系. 重新写的框架与Log4j无关
8. 2015年Apache停止Log4j的开发, 转向Log4j 2
9. 2017年Springboot为了适配市面上主流的日志接口框架加入了spring-jcl.jar, 包装了JCL, 也支持Slf4j.

总结:

日后的框架选择, 可以选择 Slf4j + Logback. 最正宗的日志处理方案.
