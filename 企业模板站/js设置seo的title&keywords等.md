```js
function SeoUpdate(SeoTitle, SeoKeywords, SeoDescription) {
    let _headDom = '',_title = '',_meta = ''; 
    _headDom = document.getElementsByTagName('head')[0]; //获取head节点
    _title = _headDom.getElementsByTagName("title")[0];  //获取head节点下的title节点
    _meta = _headDom.getElementsByTagName("meta"); //获取head节点下的meta节点，它一般是一个数组

    _title.innerText = SeoTitle;
    for (let index = 0; index < _meta.length; index++) { 
        switch (_meta[index].name) {
            case 'keywords':
                _meta[index].content = SeoKeywords;
                break;
            case 'description':
                _meta[index].content = SeoDescription;
                break;

            default:
                break;
        }
    } 
}
SeoUpdate('SeoTitle', 'SeoKeywords', 'SeoDescription');
```