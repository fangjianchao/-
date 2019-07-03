# 踩坑-常见问题
## 1. 内存溢出
       ```js
       FATAL ERROR: CALL_AND_RETRY_LAST Allocation failed - JavaScript heap out of memory
       ```
   vue2的项目修改方法在`package.json`文件加上 `--max_old_space_size=4096`：
   ```js
     "scripts": {
        "build": "node --max_old_space_size=4096 build/build.js",
        "dev": "node --max_old_space_size=4096 build/dev-server.js",
        "fix": "gulp fix",
        "start": "node build/dev-server.js",
        "lint": "eslint src/*.{js,vue} --quiet"
      },
   ```
   
