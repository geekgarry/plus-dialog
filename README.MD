# plus-dialog

一个可拖拽的html元素，可以把任何内容放入，变为一个可拖拽的组件，可以是一个div、文本，也可以是任何网页组件，自由拖动，在靠近屏幕边缘时，会自动隐藏为一个小浮标，浮标的内容可以自定义任何图片表示当前组件的类型，没有则提供默认浮标，点击浮标即可再次显示原组件内容

## How to use it?

```
npm install plus-dialog
```

### How to use it in the project!

```
import PlusDialog from 'plus-dialog';


//对话框结构
<div class="plus-dialog-overlay" data-dialog-target="dialogName">
    <div class="plus-dialog-main-body">
        <div class="plus-dialog-header">
        </div>
        <div class="plus-dialog-container"></div>
    </div>
</div>
//如果要在页面中写出对话框，必须要的
<div class="plus-dialog-overlay">
    <div class="plus-dialog-main-body">
    </div>
</div>
//在里面写入任何对话框的内容，另外如果要定义一个关闭对话框的按钮
//在需要添加关闭事件的标签里写一个属性data-cancel="plus-dialog"
//当在页面中没有写对话框的节本标签元素时，需要使用content参数传入对话框内容
//直接使用
PlusDialog.show({
    content: "对话框内容"
});

//全部参数
{
    title: "", //对话框标题
    content: '', // 对话框内容
    dialogTarget: "dialogName", //对话框的目标，表示当前对话框的标签，为对话框设置一个身份识别的标识，并在class="plus-dialog-overlay"标签上添加一个和dialogTarget相同内容的属性data-dialog-target与其匹配使用
    onlyCloseBtn: false, //是否使用关闭按钮，如果有关闭按钮则只能使用关闭按钮
}

//显示对话框
PlusDialog.show({
    //可选择使用上面参数
});

PlusDialog.onShow(() =>  {
    //对话框显示回调函数
});

PlusDialog.onHide(() =>  {
    //对话框隐藏回调函数
});
...
```

## Github

See [plus-dialog](https://github.com/geekgarry/plus-dialog).

## 🖥 浏览器兼容性

- 现代浏览器

| [![edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/edge/edge_48x48.png)](http://godban.github.io/browsers-support-badges/) | [![Edge](https://raw.githubusercontent.com/alrra/browser-logos/master/src/firefox/firefox_48x48.png)](http://godban.github.io/browsers-support-badges/) | [![chrome](https://raw.githubusercontent.com/alrra/browser-logos/master/src/chrome/chrome_48x48.png)](http://godban.github.io/browsers-support-badges/) | [![safari](https://raw.githubusercontent.com/alrra/browser-logos/master/src/safari/safari_48x48.png)](http://godban.github.io/browsers-support-badges/) |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Edge                                                                                                                                              | last 2 versions                                                                                                                                         | last 2 versions                                                                                                                                         | last 2 versions                                                                                                                                         |
  

### npm Docs

#### Documentation for the npm registry, website, and command-line interface

See [npm Docs](https://docs.npmjs.com/).
