## 几个复杂的css实现

#### 一、文字超出隐藏并显示省略号

单行（一定得有宽度)

`
width: 200px;          
white-space: nowrap;        
verflow: hidden;         
text-overflow: ellipsis;         
`

多行

`
word-break: break-all;            
display: -webkit-box;         
-webkit-line-clamp: 2;         
-webkit-box-orient: vertical;         
overflow: hidden;         
`

