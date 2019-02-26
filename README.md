#微信小程序第五周总结  
map  
```
<map
  longitude="104.202750"
  latitude="30.569340"
  style='width: 375px; height:200px'
  markers='{{markers}}'
  
></map>
<button bindtap='getPos'>获取我的位置</button>  

getPos:function(){
        wx.getLocation({
            type: 'gcj02', // 返回可以用于wx.openLocation的经纬度
            success(res) {
                const latitude = res.latitude
                const longitude = res.longitude
                wx.openLocation({
                    latitude,
                    longitude,
                    scale: 18
                })
            }
        })
    },
    getLocation需要在app.json中声明permission字段？
    
```
操作反馈
```

