### 自定义树形结构
angular版本的树形结构，模仿ng-zooro
#### 安装
```
npm i custom --save
```
#### 使用

```
  <custom-tree [nodeData]="nodes" (treeClick)=""></custom-tree>
```
nodeData 数据      
treeClick 点击节点触发的函数 返回当前的item         
如果需要自定义节点的html，请自定义 item里面的html数据格式，必须是htmlTemplate         
#### 数据结构
```
nodes = [{
    title: '0-0',
    key: '00',
    expanded: true,
    children: [{
      title: '0-0-0',
      key: '000',
      expanded: true,
      children: [
        { title: '0-0-0-0:1111', key: '0000', isLeaf: true },
        { title: '0-0-0-1', key: '0001', isLeaf: true },
        { title: '0-0-0-2', key: '0002', isLeaf: true }
      ]
    }, {
      title: '0-0-1',
      key: '001',
      children: [
        { title: '0-0-1-0', key: '0010', isLeaf: true },
        { title: '0-0-1-1:222222', key: '0011', isLeaf: true },
        { title: '0-0-1-2', key: '0012', isLeaf: true }
      ]
    }, {
      title: '0-0-2',
      key: '002'
    }]
  }, {
    title: '0-1',
    key: '01',
    children: [{
      title: '0-1-0',
      key: '010',
      children: [
        { title: '0-1-0-0', key: '0100', isLeaf: true },
        { title: '0-1-0-1', key: '0101', isLeaf: true },
        { title: '0-1-0-2', key: '0102', isLeaf: true }
      ]
    }, {
      title: '0-1-1',
      key: '011',
      children: [
        { title: '0-1-1-0', key: '0110', isLeaf: true, html: `<h2 class="title">-----</h2>` },
        { title: '0-1-1-1', key: '0111', isLeaf: true },
        { title: '0-1-1-2', key: '0112', isLeaf: true }
      ]
    }]
  }, {
    title: '0-2',
    key: '02',
    isLeaf: true
  }];
```