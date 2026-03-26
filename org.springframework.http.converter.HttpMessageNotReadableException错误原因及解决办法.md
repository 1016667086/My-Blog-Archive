报错原因：@RequestBody只支持POST请求，GET请求不能使用@RequestBody，修改GET请求为POST即可，如果需要使用GET请求，可以使用@RequestParam和@PathVariable

报错异常为：  
org.springframework.http.converter.HttpMessageNotReadableException: Required request body is missing: public java.lang.Object

原来写法如下：

```
@RequestMapping(value = "/appInfoList",method = RequestMethod.GET)
@ApiOperation(value = "查询app版本信息列表")
public Object appInfoList(@RequestBody @ApiParam("JSON参数") String id) {
    Object object = appInfoService.findAppInfoList(appInfo);
    return toResult(object);
}

```

修改后为：

```
@RequestMapping(value = "/appInfoList",method = RequestMethod.POST)
@ApiOperation(value = "查询信息列表")
public Object appInfoList(@RequestBody @ApiParam("JSON参数") String id) {
    Object object = appInfoService.findAppInfoList(appInfo);
    return toResult(object);
}

```