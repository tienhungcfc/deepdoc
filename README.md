# DeepDoc
*Chuyển đổi cấu trúc dạng bảng sang cấu trúc json, kèm them các tiện ích*



Trước tiên ta có các bảng mẫu

- **Categories**

ID | Title | Desc
------------ | ------------- | -------------
1001 | Danh mục 1 | Mô tả danh mục 1
1002 | Danh mục 2 | Mô tả danh mục 2

- **Aricles**

ID | Title | Desc | Content
------------ | ------------- | ------------- | ---------
2001 | Bài viết 1 | Mô tả Bài viết 1 | Nội dung 1
2002 | Bài viết 2 | Mô tả Bài viết 2 | Nội dung 2


## Ngữ pháp
Let'go

Trong c#:
```
var dd = new DeepDoc()
dd["**x0**"] = null; //any, bool, string, int, null... 
dd["fnName"]= (int a, int b) => { return a + b;}
dd.Inner = @"
    data = {}
    x = "chuỗi 1"
    data.a = x // kiểu string
";

```

chèn thêm code
```
dd.append = @"
    data.a  = 1 // chuyển thành kiểu số
    data.a += 1 // output: 2
";
```



