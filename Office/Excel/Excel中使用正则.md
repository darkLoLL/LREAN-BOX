在`Excel`中使用正则表达式

```vb
Function Re(OriText As String, ReRule As String, ReplaceYesOrNo As Boolean)
'''
'OriText：待匹配的字符串
'ReRule：正则表达式
'ReplaceYesOrNo：是否采用替换方法，1表示替换，0表示不替换，默认为不替换
'''
'创建一个正则表达式实例对象
Set ReObject = CreateObject("vbscript.regexp")
With ReObject
    '是否区分大小写，一般需求是不用区分大小写，因此这里为True
    .IgnoreCase = True
    '是否匹配所有，一般需求也都是匹配所有，这里也就默认是True,如果为False表示只匹配第一次出现的
    .Global = True
    '匹配时所用到的正则表达式
    .Pattern = ReRule
    If ReplaceYesOrNo Then
        '如果使用替换方法，则将正则表达式匹配到的项替换为空
        Re = .Replace(OriText, "")
    Else
        '否则，返回可迭代对象的第一项
        Re = .Execute(OriText)(0)
    End If
End With
End Function
```

