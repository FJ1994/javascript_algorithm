> 题目

给你一个有效的 IPv4 地址 address，返回这个 IP 地址的无效化版本。

所谓无效化 IP 地址，其实就是用 "[.]" 代替了每个 "."。

来源：力扣（LeetCode）
链接：https://leetcode-cn.com/problems/defanging-an-ip-address/
著作权归领扣网络所有。商业转载请联系官方授权，非商业转载请注明出处。

> 解题思路（一）

* 使用正则直接replace

> 实现代码（一）

```javascript
/**
 * @param {string} address
 * @return {string}
 */
var defangIPaddr = function(address) {
    return address.replace(/\./g, '[.]');
};
```

> 解题思路（二）

* 利用split和join将`.`替换为`[.]`

> 实现代码（二）
```javascript
/**
 * @param {string} address
 * @return {string}
 */
var defangIPaddr = function(address) {
    return address.split('.').join('[.]');
};
```

> 解题思路（三）

解题方法很多，大家可以思考下怎么解决哦，欢迎分享你的答案。

> 实现代码（三）

```javascript

```
