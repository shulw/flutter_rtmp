## 0.1.1

* TODO: release

## 0.1.3
* TODO: 1.修改timer刷新重复绑定问题

## 0.1.4
* 1.修复父节点刷新时重复绑定问题
* 2.当前结构下,PlatformView依赖于RtmpManager,所以建议RtmpManager设置为属性

```
class _MyAppState extends State<MyApp> {
    RtmpManager _manager;

    @override
    void initState(){
        super.initState();
        // e.g 1
        //_manager = RtmpManager();
    }    

    @override
    Widget build(BuildContext context) {
        return RtmpView(
            //e.g 2
            manager:_manager ??= RtmpManager()
      );
  
}
```