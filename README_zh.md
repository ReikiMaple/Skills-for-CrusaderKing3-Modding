# CK3 MCP Skills

## Overview

- `ck3chat`: CK3 总入口，按任务类型分发到其他 skill
- `ck3reference`: 查 CK3 机制、字段、语法、官方/参考资料
- `ck3code`: 写或改 CK3 脚本、决议、事件、本地化等
- `ck3mod-coding-standards`: CK3 代码规范、兼容性、作用域、安全性、性能
- `ck3moddebug`: Tiger 日志诊断、报错定位、验证修复

## Typical Flow

- 机制问题: `ck3reference`
- 写代码: `ck3reference` -> `ck3code`
- 报错排查: `ck3moddebug` -> `ck3reference` -> `ck3code`
- 非平凡代码任务: `ck3reference` -> `ck3mod-coding-standards` -> `ck3code`

## Notes

- `ck3moddebug` 会读取自身 skill 目录下 `README.md` 中记录的 Tiger 路径
- 这些 skill 是给 CK3 mod 开发用的，不适用于一般编程问题
