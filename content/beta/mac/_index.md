+++
title = "Mac"
date = 2020-12-29T19:33:11+10:00
weight = 1
+++

## Beta Status

The Mac version of v2 is the most complete and it is possible right now to build apps with it. There are some non-critical features missing.

### CLI

|    Command     | Status | Notes                                   |
|:-------------- |:------:|------------------------------------------
| init           | ✓      |                                         |
| build          | ✓      |                                         |
| doctor         | ✓      |                                         |
| generate       | ✗      | Typescript generation is kinda broken   |
| dev            | ✓      |                                         |
| issue          | ✗      | TBD                                     |
| update         | ✗      | TBD                                     |

### Runtime

|    Feature     |  Go  | Javascript | Notes                      |
|:-------------- |:----:|:----------:|-----------------------------
| Menu           | ✓    | ✗          | JS TBD                     |
| Window         | ✓    | ✓          |                            |
| Logging        | ✓    | ✓          |                            |
| Browser        | ✓    | ✓          |                            |
| Events         | ✓    | ✓          |                            |
| Tray           | ✓    | ✗          | JS Menu TBD                |
| System         | ✓    | ✓          |                            |
| Dialog         | ✓    | ✓          |                            |


## MacOS Version Support

One of the best way to test platform support is to try running the Kitchen Sink application located in `v2/test`. This is a comprehensive test application covering all parts of the Wails runtime (both Go and Javascript). 

| MacOS Version  | CLI  | Runtime | Notes                                                     |
|:-------------- |:----:|:-------:|-----------------------------------------------------------|
| v11.1 beta     | ✓    | ✗       | Menu / Context Menus not implemented in JS                |
|                |      |         |                                                           |
|                |      |         |                                                           |
