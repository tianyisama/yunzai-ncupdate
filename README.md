# yunzai-ncupdate
适用于云崽的指令更新nc插件

## 须知
- 本js仅适配1.5.2及以上版本的napcat

- 使用前请添加依赖pnpm add (axios，http-proxy-agent，https-proxy-agent，adm-zip) -w

  `pnpm add axios -w`
  `pnpm add http-proxy-agent -w`
  `pnpm add https-proxy-agent -w`
  `pnpm add adm-zip -w`
  
- 须在34行配置目录，例如：原先的运行目录是`E:\111\NapCat.win32.x64`，则填入`E:\\111`

- 目录的最后一级名称一定要为`NapCat.win32.x64`

- 如果不使用代理，则将代码中的
```javascript
    const client = axios.create({
      /** 不用代理可以将下面这两行注释掉 */
      httpAgent: httpAgent,
      httpsAgent: httpsAgent,
      followRedirect: true
    });
```
  `httpAgent: httpAgent,`与`httpsAgent: httpsAgent,`注释掉，否则会抛出异常
## 使用方法
放入plugins/example文件夹中即可
