### 操作已存在的dom元素
如果 appendChild/insertBefore 操作已经存在的 dom, 则原来的 dom 会移除。(只有一份实例)。
```
<form>
  <select id="select1">
    <option>1</option>
  </select>
  <select id="select2">
    <option>2</option>
  </select>
</form>
<script>
  var select2 = document.getElementById('select2')
  select2.appendChild(select1.options[0])
</script>
```
如上 demo 中, select1 的 option 就会被转移到 select2 下