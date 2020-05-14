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

#### Khai báo mới trong c#:
```
var dd = new DeepDoc()
dd["x0"] = null; //any, bool, string, int, null... 
dd["fnName"]= (int a, int b) => { return a + b;}
dd.Inner = @"
    data = {}
    x = "chuỗi 1"
    data.a = x // output {"a":"chuỗi 1"}
";

```

#### Chèn thêm code
```
dd.Append = @"
    data.a  = 1 // chuyển thành kiểu số
    data.a += 1 // output: {"a":2}
    
    a = 0
    
    x = 0 //output: 0
    x.z = 0 //output: {"z":0}
";
```

#### Chạy
```
dd.Run();
```

#### Truy vấn kết quả
```
var data = dd["data"]; //data kiểu dictionary
var a = dd["a"]; // a kiểu int






