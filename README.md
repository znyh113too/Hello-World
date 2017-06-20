
## 引用和无序列表展示 ##

> 
- 1>表示引用
    。。。。。。
- 2-表示无序
- b
- c
- 引用结束
>

----------


## 代码展示 ##
``` java 
public void getList(Long interfaceId, Integer pageBegin, Integer fetchNum, RiskVo risk) throws IOException{
        Object result;
        if(interfaceId != null){
            result = riskService.queryListByInterfaceId(interfaceId);
        }else{
            Page<RiskVo> page = riskService.queryListForPage(pageBegin, fetchNum, risk);
            result = PageResult.newPageResult(page);
        }
        writeSuccessResponse(result);
    }
```


----------


## 展示一些快捷语法 ##


 1. _这是正文斜体_
 2. ***这是粗体***


[这是百度的超链接][1]

> 这是段落引用的格式

    空四个这里展示代码块，不会被转译
    例如：<html><h1>html</h1></html>

<html><h1>html</h1></html>

![这是一个风景图片][2]

> 
- [ ] 支持本地图片
- [ ] 支持导出到印象笔记
- [x] 支持瞎搞
- [x] 支持引用网络图片地址
>


  [1]: http://www.baidu.com
  [2]: http://desk.fd.zol-img.com.cn/t_s960x600c5/g5/M00/0F/09/ChMkJlauze2IPKICABzBh_ueXY0AAH9JAMQ2qUAHMGf334.jpg
